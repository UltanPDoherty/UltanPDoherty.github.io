---
permalink: /software/
title: "Software"
---

# gateTree

gateTree is a semi-supervised decision tree algorithm for user-informed cell population identification for flow cytometry data and other single-cell analysis data.

It allows users to describe the populations they wish to identify and these descriptions guide / constrain the tree construction algorithm.

The data is partitioned via branching sequences of univariate splits. These univariate splits are based on kernel density estimate valleys or two-component Gaussian mixture model boundaries.

The cell population descriptions must take the form of a table with an entry for each cell population - protein marker (variable) pair. These entries must be either +1, -1, or 0, corresponding to a positive (high), negative (low), or undefined protein marker expression level.

```r
remotes::install_github("UltanPDoherty/gateTree")
```
