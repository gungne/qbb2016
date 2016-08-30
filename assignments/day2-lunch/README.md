# QBB2016 - Day 2 - Lunch Exercise

Explore the [.SAM file](https://samtools.github.io/hts-specs/SAMv1.pdf) you generated during last night's homework.

For each question, submit **two** files to your GitHub repository:

- Python code that produces the answer (`day2-exercise-#.py`)
- Your output (`day2-exercise-#.out`)

Here's one way to catch the output:

```shell
/Users/cmdb/qbb2016-answers/day2-lunch $ ./day2-exercise2.py > day2-exercise2.out
```

**Basic Exercises**

1. Count number of alignments
2. Count number of alignments that match perfectly to the genome
  - HINT: This is encoded in one of the sam format's optional fields
3. Count number of reads that map to exactly one location in the genome
  - HINT: number of hits
4. For the first 10 alignments, print just the column indicating which chromosome a given read aligns to
  - HINT: .split()
5. Calculate average MAPQ score
  - HINT: think about string and numeric type conversions
6. Count the number of spliced reads aligning to the forward strand, reverse strand, and how many are unspliced
7. Count number of reads that start their alignment on chromosome 2L between base 10000 and 20000 (inclusive)

**Advanced Exercises**

1. How many reads map to the reverse strand?
  - HINT 1: sam flag 0x10 bit
  - HINT 2: stackoverflow.com/questions/2591483/getting-a-specific-bit-value-in-a-byte-string
2. Determine how many reads have an average quality score >30
  - HINT 1: fastq wiki phred+33
  - HINT 2: stackoverflow.com/questions/227459/ascii-value-of-a-character-in-python
3. Count the number of indels of length 1, 2, 3, 4, greater than 4
  - HINT: This is encoded in the "CIGAR" field
