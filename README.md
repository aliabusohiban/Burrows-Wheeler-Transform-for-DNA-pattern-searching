# Burrows-Wheeler Transform for DNA pattern searching

A Python notebook that implements the Burrows-Wheeler Transform (BWT) and its inverse, then uses backward search on the BWT to count a DNA pattern and its reverse complement in a short reference sequence.

## What it does
- Builds the BWT of a DNA sequence by sorting all rotations, and reverses it to recover the original
- Tests both on a small worked example (GAT) and on a 1,989-base reference
- Counts AGATA and its reverse complement TATCT with backward search on the BWT
- Checks the BWT counts against a direct string search

## Results
- AGATA: 5 occurrences
- TATCT (reverse complement): 3 occurrences
- Both BWT counts match the direct search

## Running it
The reference FASTA file is provided by the course and is not included here, so the notebook cannot be run without it. The notebook needs only standard Python.

## Limitations
This was tested on one small reference only. The BWT is built by sorting every rotation, which uses memory proportional to the length squared, so it is not suitable for large genomes. Backward search here returns counts only, not positions.

## Use of AI
I used Claude to help me understand the algorithm and to write and debug parts of the code. I tested everything and checked the counts against a direct search.

Written as an exercise for my MSc in Bioinformatics at the University of Bath.
