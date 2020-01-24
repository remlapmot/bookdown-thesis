# An example thesis using R Markdown and bookdown

[![Build Status](https://github.com/remlapmot/bookdown-thesis/workflows/bookdown/badge.svg)](https://github.com/remlapmot/bookdown-thesis/actions?workflow=bookdown)

This repository provides the skeleton code needed to write a thesis using Rmarkdown and the bookdown package in R.

Helpful links are:

* Yihui Xie's book: https://yihui.name/en/2018/08/bookdown-crc/
* the github repo for which is here: https://github.com/yihui/bookdown-crc 
* The full bookdown guide is here: https://bookdown.org/yihui/bookdown/
* The R Markdown guide is here: https://bookdown.org/yihui/rmarkdown/

Update:

* The thesisdown package provides a richer implementation of using bookdown to create a thesis: https://github.com/ismayc/thesisdown

To open the thesis double click the `.Rproj` (RStudio project) file. This will open the project in a new instance of RStudio.

To build the thesis, either

* In RStudio navigate to the Build pane and either click `Build Book` or select the downwards arrow to the right to choose the output format/s you require.
* To build the html output from the R Console run:
```r
rmarkdown::render_site(output_format = 'bookdown::gitbook', encoding = 'UTF-8')
```
* To build the pdf output you need LaTeX installed. It is easiest to use the `tinytex` package as follows:
```r
install.packages('tinytex')
tinytex::install_tinytex()
```
Then build the pdf output with
```r
rmarkdown::render_site(output_format = 'bookdown::pdf_book', encoding = 'UTF-8')
```
* To build all outputs with a single command run:
```r
rmarkdown::render_site(encoding = 'UTF-8')
```
* To keep the intermediate `.md` file run:
```r
bookdown::render_book('index.Rmd', clean = FALSE)
```
