# Overview
This repository hosts code (MatLab(R)) that allows for an analysis of Viral Genomic Sequences that are provided by the GISAID organization.  It allows for the usage of the Discrete Fourier Transform Distance in terms of genomic signals, and also explores how well the Power Spectra of the genomic sequences allows for the clustering/classification of sequences on geographic location of submission.  The software hosted in this repository was designed using, and implemented using the MatLab2020a(R) release.  It was initially run on a x64 Windows 10 Laptop (Intel(R) Core(TM) i7-8750H CPU @ 2.21 GHz) with 16.0 GB of RAM, with 6 cores. The code does use a parralell pool for computing the Jukes-Cantor Distances in the resampling portion of the code, which allows for substantial speedup of the computation, and allows scalability to larger devices if it is desired to run for larger samples. The code contained in this repository makes use of several of the in-built functions across various MatLab(R) Toolboxes(c) including the Bioinformatics Toolbox (seqpdist - for Jukes-Cantor), Signal Processing Toolbox (for FFT), and more. 

# Software Provided
There are several different files provided in this repository, which provide both a general way of computing the Fourier-Transform Distance between all of the organisms listed in a FASTA file supplied by the user in addition to the required sub-procedures, and a machine learning script that implements various models for prediction of geographic information, after pulling location/timing information from the initial data labels provided (in this case from the GISAID standard naming procedure). 

## DFT-Distance Calculation Codes 
This repository provides a MatLab(R) implementation of the technique for computing the DFT distances between multiple sequences of possible different lengths that was first discussed in *A measure of DNA sequence similarity by Fourier Transform with applications on hierarchical clustering* by **Changchuan Yina, Ying Chenb, Stephen S.-T. Yau** in the 2014 *Journal of Theoretical Biology 359* pages 18-28, and the following year (2015) refined and further examined in *An improved model for whole genome phylogenetic analysis by Fourier transform* by **Changchuan Yin, Stephen S.-T.Yau** also in the *Journal of Theoretical Biology 382* pages 99-110. The primary file structure and dependencies for running the DFTD (Discrete Fourier Transform Distance) procedure on any generic FASTA file containing multiple entries for each of several sequences that are thought to be similar (whether they be full viral genomes, or pre-extracted genes/genetic regions) is available via the DFTDistance.m file provided. It's dependency structure, in terms of the other provided files is: 

* DFTDistance.m 
  * fftGenSeq.m 
  * es2.m 
  
 The fftGenSeq.m 

## SARS-CoV-2 Fourier Spectra Analysis Script

