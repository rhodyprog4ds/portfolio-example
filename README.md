# Getting Started


Portfolio template for CSC and DSP 310

_this is designed to be used by accepting an assignment on github classroom, if you are viewing the source repository, you will have to fork first_  

## Setup Publishing

- move a Github actions `.yml` file to have github compile for you
  - use `publish.yml` to generate html and pdf and post them on the `gh-pages` branch
  - use `pdf.yml` to generate only the pdf on the `gh-pages` branch
- follow the [Jupyter Book Setup Instructions](https://jupyterbook.org/start/overview.html) in order to build offline
- follow the [Jupyter Book PDF Instructions](https://jupyterbook.org/advanced/pdf.html) in order to build to pdf offline

## Make it yours

- edit `_config.yml` to set your name as author
- edit `intro.md` to be the introduction of your portfolio and a biography of yourself


## Preparing a Submission

- add files with your contents to the repository
- edit the appropriate `submission_x_intro.md` for
- edit `_toc.yml` as follows to include each file you've added following the example below
```
- file: submission_1_intro
  sections:
    - file: markdown
    - file: notebooks
```

## Check and download

- if you're publishing html, go to the settings tab and turn on GitHub pages to view online
- if pdf only, change to the `gh-pages` branch, view `portfolio.pdf` and download
