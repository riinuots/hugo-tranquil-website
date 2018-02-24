---
title: Your first Shiny app
author: Riinu Ots
date: '2017-10-20'
categories:
  - R
tags:
  - shiny
slug: your-first-shiny-app
---

_**What is Shiny?**_

Shiny is an R package (`install.packages("shiny")`) for making your outputs interactive. Furthermore, Shiny creates web apps meaning your work can be shared online with people who don't use R. In other words: with Shiny, R people can make websites without ever learning Javascript etc.

I am completely obsessed with Shiny and these days I end up presenting most of my work in a Shiny app.

## If it's not worth putting in a Shiny app it's not worth doing.

_Your first Shiny app_

Getting started with Shiny is actually a lot easier than a lot of people make it out to be. So I created a very short (9 slides) presentation outlining my 5-step programme for your first Shiny app.

This is the app: <https://riinu.shinyapps.io/shiny_testing/>

This is the presentation: <http://rpubs.com/riinu/shiny>

And here are the steps (also included in the presentation):

**STEP 0**: `install.packages("shiny")`. Use RStudio.

**STEP 1**: Create a script called `app.R` using this skeleton:

https://gist.github.com/riinuots/c6ec0691633df2929adc7de90bdbc792

**STEP 2**: Copy your plot code into the renderPlot function.

**STEP 3**: Add a `sliderInput` to your User Interface (`ui`). A slider is just one of the many Shiny widgets you could be using: https://shiny.rstudio.com/gallery/widget-gallery.html

**STEP 4**: Tell your Server you wish the `dplyr::filter()` to use the value from the slider. All inputs from the User Interface (`ui`) are stored in `input$variable_name`: replace the `2007` with `input$year`.

**STEP 5 (optional)**: Add `animate = TRUE.`

Press `Control+Shift+Enter` or the "Run App" button. You now have a Shiny app running on your computer. To deploy it to the internet, e.g. like I've done in the link above, see [this.](http://docs.rstudio.com/shinyapps.io/getting-started.html#deploying-applications)