
<!-- README.md is generated from README.Rmd. Please edit that file -->

# notregexcite

<!-- badges: start -->
<!-- badges: end -->

notregexcite is a demo R package created for DATA 303, @ Calvin University

## Installation

You can install the development version of notregexcite from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("bensteves/notregexcite")
```

## Example

str_split_one() allows for splitting string based on some delimiter and
returns the elements from the list, not an actual list (which
stringr::str_split() does. )

``` r
library(notregexcite)

#new list object
l1 <- "Torkelson, Greene, Mize, Cabrera"

#split every element of list up
str_split_one(l1, pattern = ",")
#> [1] "Torkelson" " Greene"   " Mize"     " Cabrera"

#split into a set number of elements
str_split_one(l1, pattern = ", ", n=2)
#> [1] "Torkelson"             "Greene, Mize, Cabrera"

#using stringr::fixed() works as well for a pattern
y <- "192.168.0.1"
str_split_one(y, pattern = stringr::fixed("."))
#> [1] "192" "168" "0"   "1"
```
