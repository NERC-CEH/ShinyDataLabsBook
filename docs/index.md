--- 
title: "A Bookdown Book Template"
author: "Peter Levy"
date: "2020-05-13"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib]
biblio-style: apalike
link-citations: yes
github-repo: NERC-CEH/bookdown-template
description: "A template for a bookdown book."
---

# Preface {-}

This is the preface to the book.


# Instructions
This is a template to help you start a [bookdown](https://bookdown.org/yihui/bookdown/) book. It is based on this book at http://seankross.com/bookdown-start/

To use this, create a new repository using this as a template, or just download it if you do not want to use GitHub. Install the bookdown package in R, and render (compile) the book in R with:

<!--- { rendering -->

```r
#install.packages("bookdown")
library(bookdown)
# The book is rendered thus:
bookdown::render_book("index.Rmd")
```
<!--- } -->

The minimal changes you will want to make are:

1. Edit the title and author in index.Rmd
2. Edit the title in _output.yml
3. The files to be complied are specified in _bookdown.yml:
  rmd_files: ["index.Rmd", "Introduction.Rmd", "MoreStuff.Rmd", "EvenMoreStuff.Rmd"].  
  Edit these or just replace them with your own R markdown files, and list them in the correct order
4. Render it as above.


All of the content of this repository is licensed 
[CC0](https://creativecommons.org/publicdomain/zero/1.0/).

