
<!-- README.md is generated from README.Rmd. Please edit that file -->

# wavesurfer

<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/wavesurfer)](https://CRAN.R-project.org/package=wavesurfer)
[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
<!-- badges: end -->

<img src = 'inst/img/ggwave.png'>

An interactive soundwave player and visualizer with rich set of plugins.
It works well with pipe (%\>%) and can be used in Shiny. It is an
interface of [‘wavesurfer.js’](https://wavesurfer-js.org) JavaScript
library and it is based on [‘htmlwidgets’](http://www.htmlwidgets.org/)
R package.

## Installation

``` r
# install.packages("remotes")
remotes::install_github("lingechun/wavesurfer@master")
```

## Using in Shiny


## annotator\_app()

The goal of `annotator_app()` is to provide an quick way to one start
annotating their audio. It requires two inputs:

  - `wavs_folder` a string with the path to the wave files folder.
  - `annotations_folder` a string with where to store the annotations
    (as a `.rds` contaning a `tibble`)

<!-- end list -->

``` r
# This is a working code!
library(wavesurfer)
annotator_app(
  wavs_folder = system.file("wav", package = "wavesurfer"), 
  annotations_folder = tempdir()
)
```

## Live examples

### Annotator

live app:
[athos.shinyapps.io/wavesurfer\_annotator/](https://athos.shinyapps.io/wavesurfer_annotator/)

``` r
wavesurfer::runExample("annotator")
```

<img src="inst/img/annotator.gif">

## Acknowledgement

The main actors that made this package possible were:

  - [htmlwidgets](http://www.htmlwidgets.org/) package;
  - [This tutorial](https://deanattali.com/blog/htmlwidgets-tips/) by
    [Dean Attali](https://deanattali.com/) and his
    [timevis](https://github.com/daattali/timevis) package from which I
    copy pasted massively.
  - [wavesurfer.js](https://wavesurfer-js.org/) library by
    [katspaugh](https://github.com/katspaugh).
  - [This annotator](https://github.com/CrowdCurio/audio-annotator) that
    inspired me for make the spectrogram visualization for wavesurfer.js
    3.0.0. A lot of ctr+C/ctr+V too.
  - [wikiaves.com.br](https://wikiaves.com.br) from where I took audio
    examples for the showcases.

Thank you very much for your work.
