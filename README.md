#Warning
*This repository is still in development, please check back soon*

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