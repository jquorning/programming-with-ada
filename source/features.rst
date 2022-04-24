Feature Overview
==============================================================================

    Based on its feature set, I'd describe Ada as a mirror of C++ in the Pascal family,
    with many features of Rust.

Covering every Ada feature would be dilute the conceptual overview of Ada, so
related Ada-specific terminology is quoted in parentheses for those wanting to
do their own targeted research.

Ada supports:

- Forced namespacing ("packages").
- Function overloading.
- Sum types ("variants", "discriminants").
- Static polymorphism (monomorphism, "generics");
- Dynamic polymorphism (dynamic dispatch, virtual functions).
- Compiler and runtime checked constraints on ranges of numerical types ("ranges", "constraints").
- User-specified runtime type invariant checking on assignment and usage as parameters ("Type_Invariant", "Static_Predicate", "Dynamic_Predicate").
- Semantic types, saying two things are the same backing type, but not the same
  type of "thing", think of "Miles" vs "Kilometers" both stored as floats, which
  cannot be assigned to each other without a cast ("derived types").
- Deterministic construction and destruction of objects (RAII, a term from C++, "controlled types")
- Design-by-contract ("precondition" and "postcondition" "aspects").
- Lifetime checks ("accessibility" of "access types", very similar to, but not as extensive as Rust).
- Task definition with defined synchronization and queueing strategies.
  ("rendezvous", "entry", "select", "accept", "abort", "Ravenscar")
- Concurrency types ("protected", which provides mutual exclusion, and "task").
- Exceptions.
- Deterministic and configurable static initialization order ("preelaborate",
  "elaborate", "elaborate_body", "elaborate_all")
- ML-style signatures ("packages", "generics")
- Formal verification, by enabling `Spark_Mode` for parts of the program and
  writing in SPARK, a language which is an Ada subset.  Think of this along the
  lines of using `extern "C"`, except for "provable" parts of your code base.

Ada is missing:

- A preprocessor (GNAT has one, but it's not standard).
- A sanitary macro system.
- Reflection.
- A concept of "move".
- Variadic functions. (coming in Ada 202x)
- Variadic templates.
- Async/Await (it has tasks instead)
- Mixed-mode arithmetic and the related implicit numerical casts.
- An equivalent of template parameter pack
- Default generic arguments (coming in Ada 202x)
