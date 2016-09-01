# QBB2016 - Day 4 - Homework Exercise

Submit your four Python scripts, with instructions needed to run them in a documentation comment, and the plots that they generate.

## 1. Time Course w/ Replicates

* add timecourse of male Sxl abundance to the **same** plot
* style it similarly to [Lott et al., 2011 PLoS Biology](http://www.ncbi.nlm.nih.gov/pubmed/21346796) (i.e. x-axis tick labels, color, legend, etc.)
* add stage 14 replicates to the same plot (```~/data/fastq/replicates.csv```)

  * HINT: since there are only replicates for 14A/B/C/D, you will need to "skip" plotting 10/11/12/13
  * HINT: ```plt.plot( x, y, 'o' )```

## 2. Histogram

Create a histogram of the FPKM values for SRR072893.

* filter out zero-values
* log values 

## 3. MA-Plot

Instead of plotting FPKM values for SRR072893 and SRR072915 directly, transform the data to make an [MA-plot](https://en.wikipedia.org/wiki/MA_plot).  This time do **not** drop rows with 0 FPKM.  ```plt.scale( 'log' )``` is not enough so you will have to log etc your values first.

## 4. Density Plot

Create a density plot of the FPKM values for SRR072893.  Google pyplot kernel density and follow gaussian_kde.

