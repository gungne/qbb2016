# QBB2016 - Day 2 - Evening Exercise

Frequently when dealing with annotation data we will need to translate
identifiers according to a mapping. For example, mapping gene identifiers
to protein identifiers for searching a protein database, or identifying
orthologs using an existing orthology database (e.g. Homologene).

Here you will implement a python program to perform such a mapping. First you
will generate a mapping file in a simplified format, and then perform the
mapping.

## 1. Mapping FlyBase genes to UniProt

We want to build a mapping from FlyBase gene IDs to UniProt IDs.

Uniprot provides a mapping from FlyBase genes here:

  http://www.uniprot.org/docs/fly.txt

This looks difficult to parse. It has a free form header and footer, and
has rows with different numbers of fields and no clear delimiter. One could
certainly parse this file by determining field widths, and tracking when
the header ends, etc.

However, if you look at the data the fields we need are only on the lines
containing the string "DROME". This should make it much easier for you to
parse.

Parse this file, and output a new file with two tab separated columns, the
first containg the FlyBase ID and the second the Uniprot ID (AC).

## 2. Identifier mapping

Write a python script for identifier mapping. Your script should take as input
the mapping file (as above) and a c_tab file from StringTie and find the
corresponding translation from the mapping file. If found, it should print the
line from the c_tab file with the identifier. If not found, it should do
one of two things depending on a command line argument:

  1. Print nothing (ignore the line)
  2. Print and fill the field with a default value

## Submit

Submit your two Python scripts, with any instructions needed to run them in
a documentation comment, and the first 100 lines of your output using each
of the two options.
