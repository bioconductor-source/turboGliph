# turboGliph

GLIPH (Grouping of Lymphocyte Interactions by Paratope Hotspots) is an algorithm developed by Glanville&nbsp;*et&nbsp;al.* to identify specificity groups in the T cell receptor repertoire based on local (motif sharing) and global (hamming distance) similarities.\(^1\)\(^,\)\(^2\)<br>

The authors of the paper published a version of GLIPH written in Perl\(^2\), but its disadvantage is a long runtime, especially for larger sample sizes. Recently, with a new version of the package, GLIPH2, they introduced an improved algorithm that speeds up the analysis by substituting repeated sampling by Fisher's exact test to assess the statistical significance of a given motif.\(^3\)\(^,\)\(^4\)<br>

In this R implementation of GLIPH we followed their Perl script and we tried to include all the options of the original algorithm, but with a constant look on the analysis speed. With an input size of ~ $10^4$, this R implementation is about 50 times faster and for an input size of ~ $10^5$ sequences it is about 500 times faster than the Perl script. In addition, we implemented a function for visualizing the clusters generated by GLIPH, which enables graphical processing and analysis of GLIPH results through numerous customization options. The implementation of GLIPH2 as well as the function **gliph_combined**, which combines the different features of GLIPH and GLIPH2 in a customizable way, complete this package and allow the user to use the different GLIPH algorithms according to his own needs.<br>

For more information about the functions included in this package see the included vignette.<br>

For more details about the method we recommend reading the original papers and the GLIPH/GLIPH2 documentation on github.\(^1\)\(^,\)\(^2\)\(^,\)\(^3\)\(^,\)\(^4\) 

**1**: Glanville, Jacob, et al. "Identifying specificity groups in the T cell receptor repertoire." Nature 547.7661 (2017): 94.<br>
**2**: [https://github.com/immunoengineer/gliph](https://github.com/immunoengineer/gliph)<br>
**3**: Huang, Huang, et al. "Analyzing the Mycobacterium tuberculosis immune response by T-cell receptor clustering with GLIPH2 and genome-wide antigen screening." Nature Biotechnology 38.10 (2020): 1194-1202.<br>
**4**: http://50.255.35.37:8080/tools<br>
