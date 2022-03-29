# Latex GitHub Actions For ACHD

This repository is forked from the GitHub action for [compiling a LaTeX document](https://github.com/xu-cheng/latex-action).
Thanks a lot to [Cheng Xu](https://github.com/xu-cheng) for his repo https://github.com/xu-cheng/latex-action and thanks a lot to the instruction written by [David Haberthür](https://github.com/habi).

This by commit and push, you can compile the main.tex, the pdf report is in the [gh-pages](https://github.com/Yuchengyw6/latex-test/tree/gh-pages) branch, it is generated automatically. 

The daily data in the report is from [ACHD-data](https://github.com/Yuchengyw6/latex-test/tree/master/data-raw), which is also automatically scraped from different sources daily.

## job.R
[job.R](https://github.com/Yuchengyw6/latex-test/blob/master/R/job.R) contains the web-scraping part of this project, the daily data we need is scraped from 6 different sources and automatically generate a .tex file in the [data-raw](https://github.com/Yuchengyw6/latex-test/tree/master/data-raw) folder.

## main.tex
[main.tex](https://github.com/Yuchengyw6/latex-test/blob/master/main.tex) is the main part of the report, it will be generated automatically everyday.
