# Latex GitHub Actions For ACHD weather report

This repository is forked from the GitHub action for [compiling a LaTeX document](https://github.com/xu-cheng/latex-action).
Thanks a lot to [Cheng Xu](https://github.com/xu-cheng) for his repo https://github.com/xu-cheng/latex-action and thanks a lot to the instruction written by [David Haberthür](https://github.com/habi).

This by commit and push, you can compile the main.tex, the pdf report is in the [gh-pages](https://github.com/Yuchengyw6/latex-test/tree/gh-pages) branch, it is generated automatically. 

The daily data in the report is from [ACHD-data](https://github.com/Yuchengyw6/latex-test/tree/master/data-raw), which is also automatically scraped from different sources daily.

## General Logic

Generally, this report is generated in two steps:

1, Data Collection

[job.R](https://github.com/Yuchengyw6/latex-test/blob/master/R/job.R) is the data scraping part of this project, the daily data we need is scraped from 6 different sources and automatically generate a .tex file in the [data-raw](https://github.com/Yuchengyw6/latex-test/tree/master/data-raw) folder.

2, Generate Latex report

[main.tex](https://github.com/Yuchengyw6/latex-test/blob/master/main.tex) is the main part of the report, it will be generated automatically everyday. 

## Workflow files

The workflow files here is controlling the schedules of the tasks. 

[main.yaml](https://github.com/Yuchengyw6/latex-test/blob/master/.github/workflows/main.yaml) is the workflow file for compiling the LaTeX file automatically.

[schedule-commit.yaml](https://github.com/Yuchengyw6/latex-test/blob/master/.github/workflows/schedule-commit.yaml) is the workflow file for the data scraping process.

Ideally you do not need to change anything inside these files.


## Possible Errors

1, Some websites source we are using might be unfunctional in some specific days. If you receive an error message via email, and find that the file [data_X07.tex](https://github.com/Yuchengyw6/latex-test/blob/master/data-raw/data_X07.tex) did not update itself or some data is wrong, you may need to modify this file manually, details please refer to [example.tex](https://github.com/Yuchengyw6/latex-test/blob/master/data-raw/example.tex).
