QBB2016 - Day 1 - Homework
==========================

Perform an RNA-seq analysis on the male stage 10 embryo (SRR072893) using HISAT/StringTie.

**'New Tuxedo' Package Reference**

[Transcript-level expression analysis of RNA-seq experiments with HISAT, StringTie and Ballgown](http://www.ncbi.nlm.nih.gov/pubmed/27560171) Pertea, et al., 2016 Nature Protocols

**Submitting Answers** 

- For the Basic Exercises
    - Do the four exercises inside ```~/data/day1-homework``` to keep your result files organized
    - Submit **only** your commands by using ```nano``` to create a file ```commands``` in ```~/qbb2016-answers/day1-homework```
- For the Advanced Exercises
    - Submit output as ```answers``` in ```~/qbb2016-answers/day1-homework```


**Basic Exercises**

1. Generate a quality control report for the reads in ```SRR072893.fastq``` using [FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/)

    - HINT: ```fastqc -help```

    **NOTE:** If you are encountering errors, you may still have a truncated version of SRR072893.fastq.  Try making a fresh copy from /Users/cmdb/rawdata.

2. Map reads to ```BDGP6``` using [HISAT2](http://ccb.jhu.edu/software/hisat2/index.shtml)

    - HINT: use options ```-p``` ```-S```
    
3. Convert .sam to a sorted .bam and index using [SAMtools](http://www.htslib.org/doc/samtools.html)

    - HINT: ```samtools sort```, ```samtools index```

4. Quantitate sorted .bam file using [StringTie](http://ccb.jhu.edu/software/stringtie/)

    - HINT: use options ```-p``` ```-e``` ```-G``` ```-o``` ```-B```


**Advanced Exercises**

Skim over [.SAM format](https://github.com/samtools/hts-specs) specification. 

1. Calculate how many alignments are on each chromosome in your .sam file

    - HINT: ```cut``` ```sort``` ```uniq```

2. Find the chromosome position in your .sam file at which the most reads start their alignment

    - HINT: ```cut``` ```sort``` ```uniq``` ```sort```

3. Calculate the mean FPKM and standard deviation for Sxl transcript ```FBtr0331261``` across all 24 samples in ```/Users/cmdb/data/results/stringtie```.  You'll first have to ```tar xf SRP004442.stringtie.tar.gz```.

    - HINT: ```grep SRR072*/t_data.ctab``` | ```awk```

4. Which transcripts have an FPKM > 1000 in all 24 samples?

    - HINT: ```paste SRR072*/t_data.ctab``` | ```cut``` | ```awk```
