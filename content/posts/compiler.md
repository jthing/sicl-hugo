---
title: "Compiler"
date: 2024-03-08T00:00:00+01:00
draft: false
---

## preliminary draft for compiler design {#preliminary-draft-for-compiler-design}


### scope {#scope}

This is a continuation of Stands CICL (Compiler in Common
Lisp). Although most of the compiler can itself be written in Common
Lisp  to be a compliant Compiler it must eventually compile  to
machine code. Today this is done by the SBCL compiler. To make the
compiler work standalone this will need to be implemented and thus I have drafted this
proposal. It is criteria that the compiler need to be fast and good. A speed
goal for the generated code would be to be within a factor of 3 of a C compiler. The
compiler itself must compile fast similarly to the SBCL compiler today or
better. This is a preliminary draft of my ideas of how this can be
accomplished, subject to approved by Dr Strand.


## The 26 special forms of common lisp {#the-26-special-forms-of-common-lisp}

By the time the code gets to the compiler the macro-expander has already run and all that
is left are the 26 special forms that need to be compiled.

| block              | if                   | progv           |
|--------------------|----------------------|-----------------|
| catch              | labels               | quote           |
| load-time-eval     | let                  | return-from     |
| declare            | let\*                | setq            |
| eval-when          | macrolet             | tagbody         |
| flet               | multiple-value-call  | the             |
| function           | multiple-value-prog1 | throw           |
| go                 | progn                | unwind-protect  |
| generic-flet       | generic-labels       | symbol-macrolet |
| with-added-methods |                      |                 |


## Structure {#structure}

{{< figure src="/images/Structure.svg" >}}


## Optimization {#optimization}


### The IR language {#the-ir-language}

Mind you a SSA form (single static assignment) mentioned in the above
paper should be replaced with a CPS form (continuation passing style) for CL


### peephole optimizations {#peephole-optimizations}

-   Null sequences – Delete useless operations.
-   Combine operations – Replace several operations with one equivalent.
-   Algebraic laws – Use algebraic laws to simplify or reorder instructions.
-   Special case instructions – Use instructions designed for special operand cases.
-   Address mode operations – Use address modes to simplify code.

...


### typecheck optimization {#typecheck-optimization}

Remove unnecessary type checks. Move type checks out of loops.


### Invariant lifter {#invariant-lifter}

Lifts invariants (also called constant expressions) out of loops.


### loop unrolling {#loop-unrolling}

Unrolls loops giving more opportunity of for parallelism. See Instruction Fusion below.


## Machine code translation {#machine-code-translation}

More than just translating the Universal Assembly to machine code there are also
architecture specific optimizations.


### Register optimization {#register-optimization}

I suggest Linear scan for speed.

Linear Scan is a algorithm suggested by Poletto in 1999. I this
approach the code is not turned into a graph. Instead, all the
variables are linearly scanned to determine the live range,
represented as a interval. Once all the live ranges have been
determined, the intervals are traversed chronologically. Although this
traversal could help identifying which variables whose live ranges
interfere, no graph is being built and the variable are allocate din
a greedy way.


### Instruction fusion {#instruction-fusion}

Instruction fusion is the process of grouping arithmetic instructions together to form
vector instructions.


### jmp elimination {#jmp-elimination}

The assembly of then include instructions for things like conditional add which don't require
jumping. Substitute there if possible.


## Runtime {#runtime}

Finally the compiler has finished ad the binary blob is passed to the run-time for
execution. A dialog is also necessary to find variables, functions and like referenced from
the expression being evaluated.
