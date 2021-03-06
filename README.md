# CrossDecomposition

[![Build Status](https://travis-ci.org/simonster/CrossDecomposition.jl.png)](https://travis-ci.org/simonster/CrossDecomposition.jl)

## Introduction

This package implements canonical correlation in Julia. Someday it will also implement partial least squares. (If you'd like to contribute, please let me know!)

## Usage

To perform canonical correlation analysis between matrices `X` and `Y`:

```julia
using CrossDecomposition
cc = canoncor(X, Y)
```

`cc` is a `CanonicalCorrelation` object that implements the following methods:

- `coef(cc)` returns the canonical coefficients (loadings) of `X` and `Y` as a tuple of two matrices. The coefficients are scaled so that the scores have identity covariance.
- `cor(cc)` returns the vector of canonical correlations.
- `scores(cc)` returns the canonical variables (component scores) of `X` and `Y` as a tuple of two matrices.
