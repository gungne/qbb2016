# QBB2016 - Day 3 - Evening Exercise

## Heuristic sequence alignment

The first step in alignment algorithms like BLAST and FASTA is to find
candidate alignment "seeds" using a dictionary-like index. Here we will
implement the two first steps of such a matcher. 

### Data

Use **[this file](http://taylorlab.org/outgoing/droYak2_seq.fa)** as your query sequence

Use `subset.fa` from this morning as your target sequence

### 1. Extend k-mer counter to k-mer matcher

Implement a script that finds matching k-mers between a single query 
sequence and a database of targets. The matcher should take three 
arguments:

```kmer_matcher.py <target.fa> <query.fa> <k>```

Where `target.fa` is the database, potentially multiple sequences, 
`query.fa` is the sequence to align (assume just one sequnce), and
`k` is the k-mer size (an integer).

The script should find k-mer matches and for each write:

```
target_sequence_name    target_start    query_start k-mer
```

Run the program for k=11 and submit the first 1000 lines.

### 2. Extend matches 

Based on your kmer matcher, create `kmer_match_extender.py` which for each
matched kmer will extend on either end to find the longest exact match. 
For each target sequence, print the matches ordered from longest to
shortest. 

## Hints

1. You can consider each query k-mer (position in the query) independently
   and in order.
2. You can track the position in the query using enumerate. 
