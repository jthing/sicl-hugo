---
title: "Bibliography"
date: 2024-03-10T00:00:00+01:00
draft: false
---

## Bibliography {#bibliography}

```picture-mode

@book{allenOptimizingCompilersModern2001,
  title = {Optimizing Compilers for Modern Architectures: A Dependence-Based Approach},
  shorttitle = {Optimizing Compilers for Modern Architectures},
  author = {Allen, Randy and Kennedy, Ken},
  date = {2001},
  edition = {1st ed},
  publisher = {{Morgan Kaufmann Publishers}},
  location = {{San Francisco}},
  isbn = {978-1-55860-286-1},
  pagetotal = {790},
  keywords = {Computer architecture,Optimizing compilers}
}

@article{appelSSAFunctionalProgramming1998,
  title = {{{SSA}} Is Functional Programming},
  author = {Appel, Andrew W.},
  date = {1998-04},
  journaltitle = {ACM SIGPLAN Notices},
  shortjournal = {SIGPLAN Not.},
  volume = {33},
  number = {4},
  pages = {17--20},
  issn = {0362-1340, 1558-1160},
  doi = {10.1145/278283.278285},
  url = {https://dl.acm.org/doi/10.1145/278283.278285},
  urldate = {2024-03-09},
  langid = {english},
  file = {/home/john/Zotero/storage/RNTL2HK5/Appel - 1998 - SSA is functional programming.pdf}
}

@book{barendregtLambdaCalculusIts1984,
  title = {The Lambda Calculus: Its Syntax and Semantics},
  shorttitle = {The Lambda Calculus},
  author = {Barendregt, H. P.},
  date = {1984},
  series = {Studies in Logic and the Foundations of Mathematics},
  edition = {Rev. ed},
  number = {v. 103},
  publisher = {{North-Holland ; Sole distributors for the U.S.A. and Canada, Elsevier Science Pub. Co}},
  location = {{Amsterdam ; New York : New York, N.Y}},
  isbn = {978-0-444-86748-3 978-0-444-87508-2},
  pagetotal = {621},
  keywords = {Lambda calculus}
}

@book{biereHandbookSatisfiability2009,
  title = {Handbook of Satisfiability},
  editor = {Biere, Armin},
  date = {2009},
  series = {Frontiers in Artificial Intelligence and Applications},
  number = {v. 185},
  publisher = {{IOS Press}},
  location = {{Amsterdam, The Netherlands ; Washington, DC}},
  isbn = {978-1-58603-929-5},
  pagetotal = {966},
  keywords = {Algebra Boolean,Algorithmus,Anwendung,Berechnungskomplexität,Computer algorithms,Congresses,Decision making,Erfüllbarkeitsproblem,Propositional calculus},
  annotation = {OCLC: ocn290492523}
}

@article{clickSimpleGraphBasedIntermediate,
  title = {A {{Simple Graph-Based Intermediate Representation}}},
  author = {Click, Cliff and Paleczny, Michael},
  abstract = {We present a graph-based intermediate representation (IR) with simple semantics and a low-memory-cost C++ implementation. The IR uses a directed graph with labeled vertices and ordered inputs but unordered outputs. Vertices are labeled with opcodes, edges are unlabeled. We represent the CFG and basic blocks with the same vertex and edge structures. Each opcode is defined by a C++ class that encapsulates opcode-specific data and behavior. We use inheritance to abstract common opcode behavior, allowing new opcodes to be easily defined from old ones. The resulting IR is simple, fast and easy to use.},
  langid = {english},
  file = {/home/john/Zotero/storage/685NSKUM/Click og Paleczny - A Simple Graph-Based Intermediate Representation.pdf}
}

@inreference{ContinuationpassingStyle2023,
  title = {Continuation-Passing Style},
  booktitle = {Wikipedia},
  date = {2023-11-02T15:32:49Z},
  url = {https://en.wikipedia.org/w/index.php?title=Continuation-passing_style&oldid=1183163457},
  urldate = {2024-03-03},
  abstract = {In functional programming, continuation-passing style (CPS) is a style of programming in which control is passed explicitly in the form of a continuation. This is contrasted with direct style, which is the usual style of programming. Gerald Jay Sussman and Guy L. Steele, Jr. coined the phrase in AI Memo 349 (1975), which sets out the first version of the Scheme programming language.John C. Reynolds gives a detailed account of the numerous discoveries of continuations.A function written in continuation-passing style takes an extra argument: an explicit "continuation"; i.e., a function of one argument.  When the CPS function has computed its result value, it "returns" it by calling the continuation function with this value as the argument. That means that when invoking a CPS function, the calling function is required to supply a procedure to be invoked with the subroutine's "return" value.  Expressing code in this form makes a number of things explicit which are implicit in direct style.  These include: procedure returns, which become apparent as calls to a continuation; intermediate values, which are all given names; order of argument evaluation, which is made explicit; and tail calls, which simply call a procedure with the same continuation, unmodified, that was passed to the caller. Programs can be automatically transformed from direct style to CPS. Functional and logic compilers often use CPS as an intermediate representation where a compiler for an imperative or procedural programming language would use static single assignment form (SSA). SSA is formally equivalent to a subset of CPS (excluding non-local control flow, which does not occur when CPS is used as intermediate representation). Functional compilers can also use A-normal form (ANF) (but only for languages requiring eager evaluation), rather than with 'thunks' (described in the examples below) in CPS.  CPS is used more frequently by compilers than by programmers as a local or global style.},
  langid = {english},
  annotation = {Page Version ID: 1183163457},
  file = {/home/john/Zotero/storage/44YKD49Q/Continuation-passing_style.html}
}

@video{CrashCourseModern,
  entrysubtype = {video},
  title = {A Crash Course in Modern Hardware by Cliff Click},
  url = {https://www.youtube.com/watch?v=OFgxAFdxYAQ},
  urldate = {2024-02-26},
  abstract = {I walk through a tiny performance example on a modern out-of-order CPU, and basically show that (1) single-threaded performance is tapped out, (2) all the ac...},
  langid = {norwegianbokmal},
  file = {/home/john/Zotero/storage/72W3PQHJ/watch.html}
}

@article{durandRemovingRedundantTests,
  title = {Removing Redundant Tests by Replicating Control Paths},
  author = {Durand, Irène and Strandh, Robert},
  abstract = {We describe a technique for removing redundant tests in intermediate code by replicating the control paths between two identical tests, the second of which is dominated by the first. The two replicas encode different outcomes of the test, making it possible to remove the second of the two. Our technique uses local graph rewriting, making its correctness easy to prove. We also present a proof that the rewriting always terminates. This technique can be used to eliminate multiple tests that occur naturally such as the test for consness when both car and cdr are applied to the same object, but we also show how this technique can be used to automatically create specialized versions of general code, for example in order to create fast specialized versions of sequence functions such as find depending on the type of the sequence and the values of the keyword arguments supplied.},
  langid = {english},
  file = {/home/john/Zotero/storage/G6RUD3V3/Durand og Strandh - Removing redundant tests by replicating control pa.pdf}
}

@article{flanaganEssenceCompilingContinuations,
  title = {The {{Essence}} of {{Compiling}} with {{Continuations}}},
  author = {Flanagan, Cormac and Sabry, Amr and Duba, Bruce F and Felleisen, Matthias},
  abstract = {In order to simplify the compilation process, many compilers for higher-order languages use the continuationpassing style (CPS) transformation in a rst phase to generate an intermediate representation of the source program. The salient aspect of this intermediate form is that all procedures take an argument that represents the rest of the computation (the \textbackslash continuation"). Since the na ve CPS transformation considerably increases the size of programs, CPS compilers perform reductions to produce a more compact intermediate representation. Although often implemented as a part of the CPS transformation, this step is conceptually a second phase. Finally, code generators for typical CPS compilers treat continuations specially in order to optimize the interpretation of continuation parameters.},
  langid = {english},
  file = {/home/john/Zotero/storage/69GCBY46/Flanagan et al. - The Essence of Compiling with Continuations.pdf}
}

@book{hennessyComputerArchitectureQuantitative2012,
  title = {Computer Architecture: A Quantitative Approach},
  shorttitle = {Computer Architecture},
  author = {Hennessy, John L. and Patterson, David A. and Asanović, Krste},
  date = {2012},
  edition = {5. ed},
  publisher = {{Elsevier, Morgan Kaufmann}},
  location = {{Amsterdam Heidelberg}},
  isbn = {978-0-12-383872-8 978-93-81269-22-0},
  langid = {english},
  file = {/home/john/Zotero/storage/6UVS69MQ/Hennessy et al. - 2012 - Computer architecture a quantitative approach.pdf}
}

@book{jacobsCategoricalLogicType1999,
  title = {Categorical Logic and Type Theory},
  author = {Jacobs, Bart},
  date = {1999},
  series = {Studies in Logic and the Foundations of Mathematics},
  edition = {1st ed},
  number = {v. 141},
  publisher = {{Elsevier Science}},
  location = {{Amsterdam ; New York}},
  isbn = {978-0-444-50170-7},
  pagetotal = {760},
  keywords = {Categories (Mathematics),Type theory}
}

@book{jonesGarbageCollectionAlgorithms2007,
  title = {Garbage Collection: Algorithms for Automatic Dynamic Memory Management},
  shorttitle = {Garbage Collection},
  author = {Jones, Richard and Lins, Rafael},
  date = {2007},
  edition = {Reprinted October 2007},
  publisher = {{Wiley}},
  location = {{Chichester}},
  isbn = {978-0-471-94148-4},
  langid = {english},
  pagetotal = {379}
}

@article{kelseyCorrespondenceContinuationPassing,
  title = {A {{Correspondence}} between {{Continuation Passing Style}} and {{Static Single Assignment Form}}},
  author = {Kelsey, Richard A},
  langid = {english},
  file = {/home/john/Zotero/storage/I24WPJWX/Kelsey - A Correspondence between Continuation Passing Styl.pdf}
}

@book{khedkerDataFlowAnalysis2009,
  title = {Data Flow Analysis: Theory and Practice},
  shorttitle = {Data Flow Analysis},
  author = {Khedker, Uday and Sanyal, Amitabha and Karkare, Bageshri},
  date = {2009},
  publisher = {{CRC Press/Taylor \& Francis}},
  location = {{Boca Raton, FL}},
  isbn = {978-0-8493-2880-0},
  pagetotal = {386},
  keywords = {Compilers (Computer programs),Computer software,Data flow computing,Software engineering,Verification},
  annotation = {OCLC: ocn300030552}
}

@book{nipkowConcreteSemanticsIsabelle2014,
  title = {Concrete {{Semantics}}: {{With Isabelle}}/{{HOL}}},
  shorttitle = {Concrete {{Semantics}}},
  author = {Nipkow, Tobias and Klein, Gerwin},
  date = {2014},
  publisher = {{Springer International Publishing}},
  location = {{Cham}},
  doi = {10.1007/978-3-319-10542-0},
  url = {https://link.springer.com/10.1007/978-3-319-10542-0},
  urldate = {2024-03-11},
  isbn = {978-3-319-10541-3 978-3-319-10542-0},
  langid = {english},
  file = {/home/john/Zotero/storage/W9MJL6F9/Nipkow og Klein - 2014 - Concrete Semantics With IsabelleHOL.pdf}
}

@book{pierceAdvancedTopicsTypes2005,
  title = {Advanced Topics in Types and Programming Languages},
  editor = {Pierce, Benjamin C.},
  date = {2005},
  publisher = {{MIT Press}},
  location = {{Cambridge, Mass.}},
  abstract = {Substructural type systems / David Walker -- Dependent types / David Aspinall and Martin Hofmann -- Effect types and region-based memory management / Fritz Henglein, Henning Makholm, and Henning Niss -- Typed assembly language / Greg Morrisett -- Proof-carrying code / George Necula -- Logical relations and a case study in equivalence checking / Karl Crary -- Typed operational reasoning / Andrew Pitts -- Design considerations for ML-style module systems / Robert Harper and Benjamin C. Pierce -- Type definitions / Christopher A. Stone -- The essence of ML type inference / Fran(c)ʹois Pottier and Didier R(c)♭my.y},
  isbn = {978-0-262-16228-9},
  langid = {english},
  pagetotal = {574},
  file = {/home/john/Zotero/storage/MMH8AGBM/Pierce - 2005 - Advanced topics in types and programming languages.pdf}
}

@book{pierceTypesProgrammingLanguages2002,
  title = {Types and Programming Languages},
  author = {Pierce, Benjamin C.},
  date = {2002},
  publisher = {{MIT Press}},
  location = {{Cambridge, Mass}},
  isbn = {978-0-262-16209-8},
  pagetotal = {623},
  keywords = {Programming languages (Electronic computers)}
}

@book{queinnecLispSmallPieces2003,
  title = {Lisp in Small Pieces},
  author = {Queinnec, Christian and Callaway, Kathleen and Queinnec, Christian and Queinnec, Christian},
  date = {2003},
  edition = {1. paperback ed},
  publisher = {{Cambridge Univ. Press}},
  location = {{Cambridge}},
  isbn = {978-0-521-54566-2 978-0-521-56247-8},
  langid = {english},
  pagetotal = {514}
}

@online{RegisterAllocationAlgorithms2020,
  title = {Register {{Allocation Algorithms}} in {{Compiler Design}}},
  date = {2020-12-25T11:23:23+00:00},
  url = {https://www.geeksforgeeks.org/register-allocation-algorithms-in-compiler-design/},
  urldate = {2024-03-03},
  abstract = {A Computer Science portal for geeks. It contains well written, well thought and well explained computer science and programming articles, quizzes and practice/competitive programming/company interview Questions.},
  langid = {american},
  organization = {{GeeksforGeeks}},
  file = {/home/john/Zotero/storage/CZH6EUFP/register-allocation-algorithms-in-compiler-design.html}
}

@book{warrenHackerDelight2003,
  title = {Hacker's Delight},
  author = {Warren, Henry S.},
  date = {2003},
  publisher = {{Addison-Wesley}},
  location = {{Boston}},
  isbn = {978-0-201-91465-8},
  pagetotal = {306},
  keywords = {Computer programming}
}

```
