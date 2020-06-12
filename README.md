# Sorav Bansal : Representative Publications
(in order of relevance)

## Automatic Generation of Peephole Superoptimizers
This [paper](https://raw.githubusercontent.com/bsorav/publications/master/asplos06.pdf) demonstrates the automatic construction of a peephole optimizer
through superoptimization techniques.  The peephole optimizer optimizes
x86 binary code.  Our [current research](http://compiler.ai) involves
extending this work to code generation within a compiler.  This work
has received significant attention since it was published, and is sometimes
referred to as the *first modern superoptimizer*.

## [Binary Translation Using Peephole Superoptimizers](https://raw.githubusercontent.com/bsorav/publications/master/osdi08.pdf)
This [paper](https://raw.githubusercontent.com/bsorav/publications/master/osdi08.pdf)
extends the work on automatic generation of peephole optimizations to
binary translation across two different ISAs. A superoptimizer is employed
to automatically infer translations from one ISA to another.  A dynamic
programming formulation is used to choose the optimal code generation
strategy based on the available (automatically inferred) cross-ISA translations.
