---
title: "template"
date: 2024-03-08T00:00:00+01:00
draft: false
---

## preliminary draft for compiler design {#preliminary-draft-for-compiler-design}


### scope {#scope}

This is a continuation of Stands CICL (Compiler in Common
Lisp). Although most of the compiler can itself be written in Common
Lisp  to be a compliant Compiler it must eventually compile  to
machine code. Today this is done by the SBCL compiler. To make the
compiler work standalone this will need to be implemented and it is
this task that has fallen on me. Remember mush of the heavy lifting is
done by the macro processors so by the time the code reaches the
compiler there are only 26 special forms left. It is these 26 special
forms that must the  be translated to a Immediate Representation IR the
optimized before generation machine code. It is criteria that the
compiler need to be fast and good. A speed goal for the generated
code would be to be within a factor of 3 of a C compiler. The compiler
itself must compile fast similarly to the SBCL compiler today or
better. This is a preliminary draft of my ideas of how this can be
accomplished, subject to approved by Dr Strand.


## The 26 special forms of common lisp {#the-26-special-forms-of-common-lisp}


## Structure {#structure}

[Structure](/images/Structure.svg)


## Optimization {#optimization}


### The IR language {#the-ir-language}


### peephole optimizations {#peephole-optimizations}


### Constant propagation {#constant-propagation}


### Code inlining {#code-inlining}


### loop unrolling {#loop-unrolling}


### register optimization {#register-optimization}


### typecheck optimizations {#typecheck-optimizations}


## Memory handling {#memory-handling}


## Machine code translation {#machine-code-translation}

Mind you a SSA form (single static assignment) mentioned in the above
paper should be replaced with a CPS form (continuation passing style) for CL
