---
title: Adding space between rows in LaTex tables
author: Riinu Ots
date: '2016-04-11'
categories:
  - LaTex
tags:
  - latex
slug: adding-space-between-rows-in-latex-tables
---

By default, LaTex tables are very tight:

    \usepackage{booktabs}

    \begin{table}[]
    \centering
    \caption{My caption}
    \label{my-label}
    \begin{tabular}{@{}lll@{}}
    \toprule
    Rows  & Column 1 & Column 2 \\ \midrule
    Row 1 & 1234     & 2345     \\
    Row 2 & 3456     & 4567     \\
    Row 3 & 5678     & 6789     \\
    Row 4 & 7890     & 8901     \\
    Row 5 & 9012     & 10000    \\ \bottomrule
    \end{tabular}
    \end{table}

    <img src="https://riinudata.files.wordpress.com/2016/04/screen-shot-2016-04-11-at-11-28-54.png" alt="Screen Shot 2016-04-11 at 11.28.54" height="260" class="alignnone size-full wp-image-278" width="319" />

Adding this to the document preamble will add space between the rows:

    \renewcommand{\arraystretch}{1.7}

    <img src="https://riinudata.files.wordpress.com/2016/04/screen-shot-2016-04-11-at-11-24-26.png" alt="Screen Shot 2016-04-11 at 11.24.26" height="358" class="alignnone size-full wp-image-270" width="321" />

And this command can be used to add space between rows manually:

    \vspace{1cm}

    <img src="https://riinudata.files.wordpress.com/2016/04/screen-shot-2016-04-11-at-11-25-38.png" alt="Screen Shot 2016-04-11 at 11.25.38" height="437" class="alignnone size-full wp-image-274" width="351" />
