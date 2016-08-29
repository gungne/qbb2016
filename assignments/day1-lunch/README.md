QBB2016 - Day 1 - Lunch Exercise
================================

Summarize genome annotation (BDGP6.Ensembl.85.gtf) using Unix tools. Skim over [.GTF format](http://www.ensembl.org/info/website/upload/gff.html) specification. 

**Unix References**

- [Shorter](http://bxlab.github.io/cmdb-bootcamp/cheatsheet/unix.html) and [longer](https://github.com/0nn0/terminal-mac-cheatsheet) Unix cheat sheet
- Wikipedia list of [Unix commands](https://en.wikipedia.org/wiki/List_of_Unix_commands)
- Software Carpentry "[The Unix Shell](http://swcarpentry.github.io/shell-novice/)"

**Git References**

- [Short](http://bxlab.github.io/cmdb-bootcamp/cheatsheet/git.html) Git cheat sheet
- Software Carpentry "[Version Control with Git](http://swcarpentry.github.io/git-novice/)"

**Submitting Answers**

Use ```>>``` to append output of your final commands onto the ```answers``` file in your ```day1-lunch``` directory.  Push each updated answer to your GitHub ```qbb2016-answers``` repo e.g.

```shell
$ echo "output1" >> answers
$ git add answers
$ git commit -m "Did first one"
$ git push

$ echo "output2" >> answers
$ git add answers
$ git commit -m "Did second one"
$ git push
```

**Basic Exercises**

1. How many lines are there?

    - HINT: ```wc```

2. How many lines deal with the gene ```Sxl```?

    - HINT: ```grep``` option

3. What types of features are there?

    - HINT: ```cut``` column 3 ```sort``` ```uniq```

4. How many of each feature type are there?

    - HINT: ```uniq``` option


**Advanced Exercises**

Here are some example AWK commands:

```shell
$ awk '{print $1 "\t" $2 "\t" $3}' BDGP6.Ensembl.85.gtf
$ awk '{print "Upstream region: " $4 - 1000}' BDGP6.Ensembl.85.gtf
$ awk '{if ($4 < 20000) {print}}' BDGP6.Ensembl.85.gtf
```

1. For the first 100 features, report the chromosome, strand, start, end, and length

    - HINT: grymoire.com/Unix/Awk.html

2. Calculate the average length of all the features

    - HINT: END NR

3. Filter for features on the plus strand with a length greater than the average length

    - HINT: &&

4. For each feature, print ecah attribute on a separate line with tag and value separated by a tab

    - HINT: split for loop
