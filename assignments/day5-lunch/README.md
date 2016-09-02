# QBB2016 - Day 5 - Lunch Exercise

## Learning gene expression from chromatin marks

Quantify the extent to which histone marks around the transcription start site
are predictive of gene expression.

1. Obtain bigwig files for four different histone modifications:

  - http://10.99.134.11:9090/outgoing/H3K27me3.bw
  - http://10.99.134.11:9090/outgoing/H3K36me3.bw
  - http://10.99.134.11:9090/outgoing/H3K4me3.bw
  - http://10.99.134.11:9090/outgoing/H3K9me3.bw

  Either click on the links, or use `$ wget "http://put/the/url/in/quotes"` 
  to download them directly to your current directory.

2. Determine an approximation of the promoter region for each of the transcripts
   present in your `SRR072893/t_data.ctab` file. Do so by finding the
   region +/- 500bp from the transcription start site of each transcript. Save
   as a **tab separated** file with the extension `.bed` and columns *chromosome*,
   *start*, *end*, *t_name*.
  - __*Hint:*__ Look at strand information
  
3. Average the signal over each region using `bigWigAverageOverBed`. To get it, run this from the command line.
   
   ```$ brew install homebrew/science/kent-tools```
   
  - Remember: Running with no options will usually display usage

4. Perform ordinary linear regression for each of the four marks to determine
   how predictive each is of gene expression.
  - __*Hint:*__ For regression, use `ols` from `statsmodels`


### Submit:

* Code for #2 and #4
* Output from #4
