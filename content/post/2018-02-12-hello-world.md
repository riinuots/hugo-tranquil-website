---
title: "Hello world: blogdown loves Hugo"
author: Riinu Ots
date: '2018-02-12'
slug: hello-world
categories:
  - scripting
tags:
  - blogdown
  - hugo
  - r
  - github
  - netlify
---




# We are live!

I wrote my last blog post on Wordpress on 20-October 2017. I've been blogging on Wordpress since 2014 and the more I used the more painful it got! This is most likely caused by the fact that I have been thrifting further and further away from point-and-click interfaces...oh and discovering MARKDOWN.




### My two rules:

* text is written in Markdown (usually R Markdown/knitr/bookdown, e.g. see how easy it is to create a book: ["HealthyR: the eBook"](https://surgicalinformatics.github.io/healthyr_book/))
* data analysis needs to end up in a Shiny app (e.g., see ["If it’s not worth putting in a Shiny app it’s not worth doing."](https://riinu.me/2017/10/20/your-first-shiny-app/))


## So I finally got round to creating a blogdown-Hugo site:

[Hugo](https://gohugo.io/) is a website generator that is code-based (no more dragging around those pesky Wordpress elements); [blogdown](https://bookdown.org/yihui/blogdown/) is an R package that will help you generate Hugo, Jekyll, or Hexo sites, especially if you will be including R Markdown in it.

### Steps on 12-February 2018 

* Created new blogdown project on RStudio, set `kakawait/hugo-tranquilpeak-theme` as the theme
* edited name, email etc. information in the `config.toml`
* absolutely could not figure out how to use the `coverImage = "cover.jpg"`: tried putting my cover image (my pug Hildegard being judgemental over the stranded oil rig on the Isle of Lewis August 2016)
* used an unquoted semicolon in the title, broke everything and spent 2 h trying to figure out what went wrong. These were the errors I was getting and that no-one else in the world (Google) seemed to have reported:
   - edits to the new post not happening, but the site isn't breaking either
   - `clean_site()` error with `rmarkdown::clean_site() Error in file.exists(files) : invalid 'file' argument`
   -  after spending 2h on github/rstudio/rmarkdown, blogdown book, blogdown repo, I finally came across `hugo -v` that prints more warnings. Notice `yaml: line 1: mapping values are not allowed in this context` (which I had indeed seen before at some point during these 2 hours but not sure where). Anyway, seeing it for the second time it clicked - markdown thinks I'm mapping something that shouldn't be mapped (mapping usually means defining variables). My title was (second line of the markdown file, really) `title: Hello world: blogdown loves Hugo`, but if using a semicolon you need quotes: `title: "Hello world: blogdown loves Hugo"`.

# Still better than Wordpress.

![](https://riinudata.files.wordpress.com/2018/02/pandas.gif)



