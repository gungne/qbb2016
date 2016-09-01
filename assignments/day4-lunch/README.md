# QBB2016 - Day 4 - Lunch Exercise

Submit your two Python scripts, with instructions needed to run them in a documentation comment, and the plots that they generate.

## 1. Use a boxplot to visualize the distribution of abundance measurements for all Sxl isoforms.

Create a boxplot for all the Sxl transcripts that have an FPKM >0 in SRR072893 and SRR072915.  ```log()``` the values, add a title, label the y-axis, and label each sample on the x-axis.

* Python [bitwise operators](http://wiki.python.org/moin/BitwiseOperators)
* Summary of most [matplotlib commands](http://matplotlib.org/api/pyplot_summary.html)
*	Full [matplotlib documentation](http://matplotlib.org/api/pyplot_api.html)
* CMDB Bootcamp [matplotlib gallery](http://bxlab.github.io/cmdb-bootcamp/gallery/README.html)

## 2. Plot the rolling mean FPKM from two samples for the main chromosomes

Create a script that plots the rolling mean FPKM for any two .ctab files.  Design the script such that it:

* creates a separate image for 2L 2R 3L 3R 4 and X
* has a title stating what chromosome is displayed using what window size
    * e.g. "Rolling mean (size = 200) for 3R"
* can be invoked from the command line as ```./plotFPKMbyPosition.py sample_1 sample_2 window_size```
    * e.g. ```./plotFPKMbyPosition.py 893/t_data.ctab 915/t_data.ctab 200```
* has minimal redundancy
    * HINT: functions and loops

