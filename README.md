# EpiForecasts Package Repository


![Build packages](https://github.com/epiforecasts/drat/workflows/Build%20packages/badge.svg)


To install EpiForecast packages, you should use the {drat} package:

```r
install.packages("drat")
```

Now you can use {drat} to register the EpiForecast repository as a valid repository:

```r
drat:::add("epiforecasts")
```

Now you can install any of the EpiForecast packages:

```r
install.packages("EpiSoon")
install.packages("EpiNow")
install.packages("NoCoVUtils")
install.packages("qra")
```

**This repository was adapted from [here](https://github.com/R4EPI/drat). We would like to thank @zkamvar for their work implementing this approach along with the authors of [`{drat}`](https://github.com/eddelbuettel/drat) and [`{drat.builder}`](https://github.com/richfitz/drat.builder).**

# Maintaining this page

The packages included in this drat repository are maintained in the
[packages.txt], which contains the github accounts and names of
the packages.

The data and metadata associated with this page are built with the
[{drat.builder}](https://github.com/richfitz/drat.builder) package. 

## Automated builds

This page is maintained under a [GitHub Action] that will check if the packages
updated and build them to this repo. If you want to update a package (e.g.
change its version number), edit the [packages.txt] file and the [GitHub
Action] will update the packages automagically. 

## Manual builds

Assuming the above works just fine, you shouldn't have to use this, but it is
here for posterity.

Install {drat.builder} via {remotes}:

```r
remotes::install_github("richfitz/drat.builder")
```

Steps for updating this page:

1. Pull from the remote to make sure you have the entire history
2. Open R from this directory
3. Run `drat.builder::build()`
4. push the changes

[packages.txt]: ./packages.txt
[GitHub Action]: https://github.com/epiforecasts/drat/actions?query=workflow%3A%22Build+packages%22
