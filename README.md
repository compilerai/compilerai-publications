# Publications in chronological order

## [Automatic Generation of Peephole Superoptimizers](https://sorav.compiler.ai/pubs/asplos06.pdf) - ASPLOS 2006
This [paper](https://sorav.compiler.ai/pubs/asplos06.pdf) demonstrates the automatic construction of a peephole optimizer
through superoptimization techniques.  The peephole optimizer optimizes
x86 binary code.  Our [current research](http://compiler.ai) involves
extending this work to code generation within a compiler.  This work
has received significant attention since it was published, and is sometimes
referred to as the *first modern superoptimizer*.

## [Binary Translation Using Peephole Superoptimizers](https://sorav.compiler.ai/pubs/osdi08.pdf) - OSDI 2008
This [paper](https://sorav.compiler.ai/pubs/osdi08.pdf)
extends the work on automatic generation of peephole optimizations to
binary translation across two different ISAs. A superoptimizer is employed
to automatically infer translations from one ISA to another.  A dynamic
programming formulation is used to choose the optimal code generation
strategy based on the available (automatically inferred) cross-ISA translations.

## [Fast Dynamic Binary Translation for the Kernel](https://sorav.compiler.ai/pubs/btkernel.pdf) - SOSP 2013
This [paper](https://sorav.compiler.ai/pubs/btkernel.pdf)
presents an architecture for Dynamic Binary Translation for the Operating System kernel (virtualizes the OS kernel through DBT). The code generator used in this work is based on our [ASPLOS 2006 paper on automatic generation of peephole optimizers](https://raw.githubusercontent.com/compilerai/compilerai-publications/master/asplos06.pdf).

## [Black-box Equivalence Checking across Compiler Optimizations](https://sorav.compiler.ai/pubs/aplas17.pdf) - APLAS 2017
This [paper](https://sorav.compiler.ai/pubs/aplas17.pdf)
presents an algorithm to automatically generate proofs of equivalence between
an unoptimized x86 assembly program and an optimized x86 assembly program.
The equivalence checker was used to identify equivalence proofs across
functions in the programs belonging to the SPEC CPU2006 benchmarks. This was
perhaps the first effort at performing equivalence checking at scale. The paper
also discusses experiments involving the use of the blackbox equivalence checker
for superoptimization. The term *blackbox equivalence checking* was coined in
this work, and has since caught on.

## [Modeling Undefined Behaviour Semantics for Checking Equivalence across Compiler Optimizations](https://sorav.compiler.ai/pubs/hvc17.pdf) - HVC 2017
This [paper](https://sorav.compiler.ai/pubs/hvc17.pdf)
contributes an algorithm to model Undefined Behaviour (UB) while generating an
equivalence proof across two programs. The paper also discusses experiences with
the application of this algorithm to programs belonging to SPEC CPU2006
benchmarks. Based on these experiences, we could roughly quantify the relevance
of different types of UB on compiler optimization.

## [Effective Use of SMT Solvers for Program Equivalence Checking through Invariant Sketching and Query Decomposition](https://sorav.compiler.ai/pubs/sat18.pdf) - SAT 2018
This [paper](https://sorav.compiler.ai/pubs/sat18.pdf)
contributes algorithms for Invariant Inference and Avoiding SMT solver timeouts
during the execution of a program equivalence checker. The *Query Decomposition*
technique used to avoid SMT solver timeouts is especially useful as it
addresses one of the most important challenges in automatic equivalence
checking --- scalability and tractability.  We have been using
query decomposition rather successfully in all our subsequent work on automatic
equivalence checking and verification.

## [OOElala: Order-Of-Evaluation based Alias Analysis for Compiler Optimization](https://sorav.compiler.ai/pubs/ooelala.pdf) - PLDI 2020
It is well known that if you write an expression in your C
program like "a+b", the evaluation of this expression can proceed in
either order (e.g., either first 'a' then 'b', or first 'b' then 'a').
We show that this has interesting implications on the way a compiler
can optimize the implementation, which can result in up to 2.6x
speedups on real-world code. Read this
[paper](https://sorav.compiler.ai/pubs/ooelala.pdf) for more details.

## [Counterexample-Guided Correlation Algorithm for Translation Validation](https://sorav.compiler.ai/pubs/counter.pdf) - OOPSLA 2020
This [paper](https://sorav.compiler.ai/pubs/counter.pdf) presents an
algorithm to automatically construct a lockstep correlation between two
programs in the presence of aggressive vectorization transformations including
loop inversion, loop unrolling, loop splitting, loop peeling, loop unswitching,
loop invariant code motion, and more.  The algorithm is blackbox in nature, i.e.,
it makes almost no assumptions on the transformations performed by the compiler.
Evaluations over O3 transformations produced by three compilers (GCC, Clang/LLVM, and
ICC) for the Testsuite of Vectorizing Compilers (TSVC) demonstrate a significant
improvement over the state of the art.
