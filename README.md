# An example thesis using Rmarkdown and bookdown

This repository provides the skeleton code needed to write a thesis using Rmarkdown and the bookdown package in R.

Helpful links are:

* Yihui Xie's book: https://yihui.name/en/2018/08/bookdown-crc/
* the github repo for which is here: https://github.com/yihui/bookdown-crc 
* The full bookdown guide is here: https://bookdown.org/yihui/bookdown/
* The Rmarkdown guide is here: https://bookdown.org/yihui/rmarkdown/

Update:

* The thesisdown package provides a richer implementation of using bookdown to create a thesis: https://github.com/ismayc/thesisdown

To open the thesis double click the `.Rproj` (RStudio project) file. This will open the project in a new instance of RStudio.

To build the thesis, either

* in RStudio navigate to the Build pane and either click `Build Book` or select the downwards arrow to the right to choose the output format/s you require.
* or, run the commands below:
```r
rmarkdown::render_site(encoding = 'UTF-8')
```
* or, if you prefer to build one output run either of the following commands.
```r
rmarkdown::render_site(output_format = 'bookdown::gitbook', encoding = 'UTF-8')
rmarkdown::render_site(output_format = 'bookdown::pdf_book', encoding = 'UTF-8')
```
