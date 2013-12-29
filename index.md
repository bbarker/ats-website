---
layout: default
---

# What is ATS?

ATS is a statically typed programming language that unifies
implementation with formal specification. It is equipped with a highly
expressive type system rooted in the framework Applied Type System,
which gives the language its name. In particular, both dependent types
and linear types are available in ATS.

The current implementation of ATS2 (ATS/Postiats) is written in ATS1
(ATS/Anairiats). ATS can be as efficient as C/C++ both time-wise and
memory-wise (see [The Computer Language Benchmarks Game][1] for concrete
evidence) and supports a variety of programming paradigms that include:

- Functional programming. The core of ATS is a functional language based
  on eager (aka. call-by-value) evaluation, which can also accommodate
  lazy (aka. call-by-need) evaluation. The availability of linear types in
  ATS often makes functional programs written in it run not only with
  surprisingly high efficiency (when compared to C) but also with
  surprisingly small (memory) footprint (when compared to C as well).

- Imperative programming. The novel and unique approach to imperative
  programming in ATS is firmly rooted in the paradigm of programming
  with theorem-proving. The type system of ATS allows many features
  considered dangerous in other languages (e.g., explicit pointer
  arithmetic and explicit memory allocation/deallocation) to be safely
  supported in ATS, making ATS a viable programming language for low-level
  systems programming. 

- Concurrent programming. ATS, equipped with a multicore-safe
  implementation of garbage collection, can support multithreaded
  programming through the use of pthreads. The availability of linear
  types for tracking and safely manipulating resources provides an
  effective means to constructing reliable programs that can take
  advantage of multicore architectures.

- Modular programming. The module system of ATS is largely infuenced by
  that of Modula-3, which is both simple and general as well as effective
  in supporting large scale programming.

In addition, ATS contains a subsystem ATS/LF that supports a form of
(interactive) theorem-proving, where proofs are constructed as total
functions. With this component, ATS advocates a programmer-centric
approach to program verification that combines programming with
theorem-proving in a syntactically intertwined manner. Furthermore, this
component can serve as a logical framework for encoding deduction
systems and their (meta-)properties. 

# What is ATS good for?

- ATS can enforce great precision in practical programming.
- ATS allows the programmer to write efficient functional programs
  that directly manipulate native unboxed data representation.
- ATS allows the programmer to reduce the memory footprint of a
program by making use of linear types.
- ATS allows the programmer to enhance the safety (and efficiency) of
a program by making use of theorem-proving.
- ATS allows the programmer to write safe low-level code that runs in
OS kernels.
- ATS can help teach type theory, demonstrating concretely the power
and potential of types in constructing high-quality software.

# Acknowledgements

The development of ATS has been funded in part by
[National Science Foundation][2] (NSF) under the grants no.
CCR-0081316/CCR-0224244, no. CCR-0092703/0229480, no. CNS-0202067, no.
CCF-0702665 and no CCF-1018601. As always, any opinions, findings,
and conclusions or recommendations expressed here are those of the author(s) and do not
necessarily reflect the views of the NSF.
 
[1]: http://shootout.alioth.debian.org/
[2]: http://www.nsf.gov/
