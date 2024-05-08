---
permalink: /software/
title: "Software"
---

## gateTree

gateTree is a semi-supervised decision tree algorithm for user-informed cell population identification for flow cytometry data and other single-cell analysis data.

It allows users to describe the populations they wish to identify and these descriptions guide / constrain the tree construction algorithm.

The data is partitioned via branching sequences of univariate splits. These univariate splits are based on kernel density estimate valleys or two-component Gaussian mixture model boundaries.

The cell population descriptions must take the form of a table with an entry for each cell population - protein marker (variable) pair. These entries must be either +1, -1, or 0, corresponding to a positive (high), negative (low), or undefined protein marker expression level.

A demonstration of gateTree can be found as a blog post on this website. It is implemented as an open-source package in the R programming language and available to install from GitHub using the code below.

```r
remotes::install_github("UltanPDoherty/gateTree")
```


## mustlinkMix

mustlinkMix implements a must-link constrained Gaussian mixture model (Melnykov et al., 2016).
 
It is as an open-source package in the R programming language and available to install from GitHub using the code below.

```r
remotes::install_github("UltanPDoherty/mustlinkMix")
```

