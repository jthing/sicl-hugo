---
title: "Cleavir"
date: 2024-08-16T00:00:00+02:00
draft: false
---

## Cleavir {#cleavir}

This is a continuation of Strands SICL (SICL implements Common
Lisp). Although most of the compiler can itself be written in Common
Lisp  to be a compliant Compiler it must eventually compile  to
machine code. Today this is done by the SBCL compiler. To make the
compiler work standalone this will need to be implemented and thus I have drafted this
proposal. It is criteria that the compiler need to be fast and good. A speed
goal for the generated code would be to be within a factor of 3 of a C compiler. The
compiler itself must compile fast similarly to the SBCL compiler today or
better. As SICL itself it is written in Common lisp.This is a preliminary draft of my
ideas of how this can be accomplished, subject approval by Dr Strand.

-   Clostrum
    [First class global environment in common lisp](http://metamodular.com/SICL/environments.pdf)
-   Eclector
    Portable reader
-   Cleavir
    Framework for common Lisp compilers
-   Cluster
    Assembler that accepts input as objects


## The 25 special forms of common lisp {#the-25-special-forms-of-common-lisp}

By the time the code gets to the compiler the macro-expander has already run and all that
is left are the 25 special forms that need to be compiled.

| block     | let\*                | return-from     |
|-----------|----------------------|-----------------|
| catch     | load-time-value      | setq            |
| eval-when | locally              | symbol-macrolet |
| flet      | macrolet             | tagbody         |
| function  | multiple-value-call  | the             |
| go        | multiple-value-prog1 | throw           |
| if        | progn                | unwind-protect  |
| labels    | progv                |                 |
| let       | quote                |                 |


## Structure {#structure}

{{< figure src="/images/SICL-compiler.svg" >}}
