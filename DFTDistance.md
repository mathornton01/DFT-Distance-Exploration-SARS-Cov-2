# DFTDistance Calculation with the DFTDistance.m file

It is fairly simple to use the DFTDistance procedure in order to compute the pairwise distances between, you must simply have a FASTA file containing all of the
sequences that you wish to compare with the procedure.  It is important to recall the header information from the file, as all that is returned is the completed set
of pairwise distances, which when arranged in a matrix appear in the same order as their appearance in the FASTA file. 

## Example Fasta input file

Suppose the example file, ex.fasta contains:

```
> Sequence A 
ACCAACACCATTAATATACCATATTAGAAC 
> Sequence B 
ACCAACGCCATTAATTAACCATATTAGAAC 
> Sequence C
GACCAGACCGAGAGTTAGAGCAGATAGACG 
```

## Example run in matlab 

In order to compute the pairwise distances among the three genetice sequences in the ex.fasta file, make sure that the DFTDistance.m, fftGenSeq.m, and es2.m files are all contained within the same working directory as your fasta file, and you are producing a MatLab file within the same file, or are running from a MatLab command prompt focused on that directory, then simply run the following command: 

```
DFTD = DFTDistance('ex.fasta');
```
