# DFTDistance Calculation with the DFTDistance.m file

It is fairly simple to use the DFTDistance procedure in order to compute the pairwise distances between, you must simply have a FASTA file containing all of the
sequences that you wish to compare with the procedure.  It is important to recall the header information from the file, as all that is returned is the completed set
of pairwise distances, which when arranged in a matrix appear in the same order as their appearance in the FASTA file. 

## Example Fasta input file

Suppose the example file, ex.fasta contains:

> Sequence A 
ACCAACACCATTAATATACCATATTAGAAC
> Sequence B 
ACCAACGCCATTAATTAACCATATTAGAAC
> Sequence C
GACCAGACCGAGAGTTAGAGCAGATAGACG


