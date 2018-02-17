## stm: An R Package for the Structural Topic Model

Website: www.structuraltopicmodel.com

Vignette: [Here](https://github.com/bstewart/stm/blob/master/inst/doc/stmVignette.pdf?raw=true)

Authors: [Molly Roberts](http://margaretroberts.net), [Brandon Stewart](http://brandonstewart.org) and [Dustin Tingley](http://scholar.harvard.edu/dtingley)

Please email all comments/questions to bms4 [AT] princeton.edu

[![CRAN Version](http://www.r-pkg.org/badges/version/stm)](https://CRAN.R-project.org/package=stm)
[![Build Status](https://travis-ci.org/bstewart/stm.png?branch=master)](https://travis-ci.org/bstewart/stm)
[![Downloads](http://cranlogs.r-pkg.org/badges/stm)](http://cran.rstudio.com/web/packages/stm/index.html)
[![Total Downloads](http://cranlogs.r-pkg.org/badges/grand-total/stm?color=orange)](http://cran.rstudio.com/web/packages/stm/index.html)

### Summary

This repository will host the development version of the package.  It is also available on CRAN. It implements variational EM algorithms for estimating topic models with covariates in a framework we call the Structural Topic Model (stm). 

The package currently includes functionality to:
* ingest and manipulate text data
* estimate Structural Topic Models
* calculate covariate effects on latent topics with uncertainty
* estimate a graph of topic correlations
* create all the plots used in our various papers

### Other Resources

Have a large text corpus or need a language we don't provide support for?  See our sister project [txtorg](http://txtorg.org)

See other materials at www.structuraltopicmodel.com

### Installation Instructions
Assuming you already have R installed (if not see http://www.r-project.org/),
to install the CRAN version, simply use:
```
install.packages("stm")
```
You can install the most recent development version using the devtools package.  First you have 
to install devtools using the following code.  Note that you only have to do this once
```  
if(!require(devtools)) install.packages("devtools")
```   
Then you can load the package and use the function `install_github`

```
library(devtools)
install_github("bstewart/stm",dependencies=TRUE)
```

Note that this will install all the packages suggested and required to run our package.  It may take a few minutes the first time, but this only needs to be done on the first use.  In the future you can update to the most recent development version using the same code. 

### Getting Started
See the vignette for several example analyses.  The main function to estimate the model is `stm()` but there are a host of other useful functions.  If you have your documents already converted to term-document matrices you can ingest them using `readCorpus()`.  If you just have raw texts you will want to start with `textProcessor()`.

### To Developers
Up until September 2016 we've primarily been doing development in private in a separate github repository.  As we have gotten several great pull requests from the community, we are in the process of shifting development over here- primarily in the development branch.
