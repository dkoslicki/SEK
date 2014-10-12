#SEK

SEK is a sparsity exploiting k-mer-based estimation of bacterial community composition estimation tool.

#What does this repository contain?

This repository is a Julia implementation of the SEK algorithm. For a Matlab implementation, see [this website](http://www.kth.se/en/ees/omskolan/organisation/avdelningar/commth/research/software).


## Requirements ##
+ Mac OS X 10.6.8 or GNU/Linux
+ 4Gb of RAM minimum. Absolutely necessary.
+ gcc that supports OpenMP
+ [dna\_utils](http://github.com/EESI/dna-utils/) *must* be installed

### Mac Requirements ###
+ Mac OS X 10.6.8 (what we have tested)
+ GCC 4.7 or newer. (gcc 4.2 did not work, and is the default installation)
+ OpenMP libraries (libgomp, usually comes with gcc)

### Linux Requirements ###
+ GCC 4.7 or newer
+ OpenMP libraries (libgomp, usually comes with gcc)

## Installation ##
After cloning and installing the [dna\_utils](http://github.com/EESI/dna-utils/) repository, just clone this repository. As the code contained herein are Julia scripts, no compilation is necessary.


## Usage ##
The code only works on FASTA files (not FASTQ or any other format).
Here's an example:
```
julia SEK -i /path/to/FASTA.fa -o /path/to/Output.tsv
```

Other options are available, see `julia SEK.jl -h`.

The output format is consistent with the [CAMI challenge](http://www.cami-challenge.org/) and is similar to the output produced by [MetaPhlAn](http://huttenhower.sph.harvard.edu/metaphlan).

## Further Notes ##
If your installation of dna_utils results in the executable being located in a non-standard location, specify this location using the option ` -k /path/to/./kmer_counts_per_sequence `

It is very important that your installation of BLAS matches the architecture of your hardware (if not, significant increases in computation time might be observed). We recommend using OpenBLAS.