---
title: 'R: Replacing NAs in all factors with ''Missing'''
author: Riinu Ots
date: '2017-07-19'
categories:
  - R
slug: r-replacing-nas-in-all-factors-with-missing
---

With a simple combination of `mutate_if` and `fct_explicit_na, `you can replace all NAs in all factors with "Missing":

If some of the words/symbols appear in white font, see the example here: [Gist: factor_NA_levels.R](https://gist.github.com/riinuots/e517c36b1feb480df981721a00e0e24a)

https://gist.github.com/riinuots/b362b1aad497bb7480b0dae18beeb087

`dplyr` reference: <http://dplyr.tidyverse.org/reference/index.html>

`forcats` reference: <http://dplyr.tidyverse.org/reference/index.html>
