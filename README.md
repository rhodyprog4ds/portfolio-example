# Getting Started


Portfolio template for CSC and DSP 310

_this is designed to be used by accepting an assignment on github classroom, if you are viewing the source repository, you will have to fork first_  

## Setup Publishing

- set up a GitHub Actions for publishing by merging (see below on how to merge) a branch to add a `.yml` file to the `.github/workflows/` folder.
  - merge `publish_html` to generate html and pdf and post them on the `gh-pages` branch.
  - merge `publish_pdf` to generate only the pdf on the `gh-pages` branch
- follow the [Jupyter Book Setup Instructions](https://jupyterbook.org/start/overview.html) in order to build offline
- follow the [Jupyter Book PDF Instructions](https://jupyterbook.org/advanced/pdf.html) in order to build to pdf offline

## Make it yours

- edit `_config.yml` to set your name as author
- edit `intro.md` to be the introduction of your portfolio and a biography of yourself



## Check and download

- if you're publishing html, go to the settings tab and turn on GitHub pages to view online
- if pdf only, change to the `gh-pages` branch, view `portfolio.pdf` and download


## Preparing for Portfolio Checks

- add files with your contents to the repository, commit all changes directly to the `main` branch
- edit the appropriate `submission_x_intro.md`
- edit `_toc.yml` as follows to include each file you've added following the example below, but with your own file names.
```
- file: submission_1_intro
  sections:
    - file: check1/notesonx
    - file: check1/reflectionb
```
- when you're ready to submit, [create a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) with `feedback` as the base branch and `main` as the head branch (labeled "compare")


# GitHub References

## Merging a branch

On web interface:
1. Above, click on the compare and create pull request button for the branch you wish to merge
1. scroll down and click merge

Offline:
1. clone the repository: (copy url from above)
1. navigate into that directory
1. merge
1. then you'll be asked to write a merge message and vim (or possibly another command line text editor will launch). Escape to
```
git clone <url>
cd portfolio
git merge origin/publish_html
```

## Make your portfolio publicly visible

To make your html site publicly visible got to the 'Settings' tab at the top, scroll down to the 'GitHub Pages' section and set the `gh-pages` branch and `root` to the source. Then that page will show you the url of your rendered portfolio. For the semester, please keep it in the `rhodyprog4ds` organization. In December, if you wish you will be able to transfer ownership of your portfolio to your GitHub account to move it from `rhodyprog4ds.github.io/portfolio-username` to `username.github.io/whatever-you-want`.
