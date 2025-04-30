---
permalink: /software/
title: "Software"
---

## outlierMBC

outlierMBC is a model-based clustering and outlier identification method that repeatedly fits a Gaussian mixture model to data and removes the data point with the lowest mixture density.

It retrospectively chooses the optimal number of data points to remove based on the distribution of the scaled squared sample Mahalanobis distances.

In particular, it utilises a sample approximation of the Wasserstein distance (p = 1) between their empirical distribution and their theoretical Beta distribution.

It is implemented as an open-source package in the R programming language and available to install from GitHub using the code below.

```r
remotes::install_github("UltanPDoherty/outlierMBC")
```

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
 
A demonstration of gateTree can be found as a blog post on this website. It is as an open-source package in the R programming language and available to install from GitHub using the code below.

```r
remotes::install_github("UltanPDoherty/mustlinkMix")
```


## outcast

outcast (OUTlier Classification And Sequential Trimming) is a spin-off which arose during the development of outlierMBC, when we observed that if we plotted the mixture density of the data point being removed at each iteration, the resulting curve often showed a distinct elbow at the correct number of outliers.

To exploit this, outcast iteratively removes the data point with the lowest mixture density and re-fits a Gaussian mixture model, similarly to outlierMBC, but chooses its optimal number of outliers by detecting a changepoint / elbow in the 'removal density' curve.

It is implemented as an open-source package in the R programming language and available to install from GitHub using the code below.

```r
remotes::install_github("UltanPDoherty/outcast")
```

