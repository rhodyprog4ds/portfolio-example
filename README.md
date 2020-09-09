# Getting Started


Portfolio template for CSC and DSP 310

_this is designed to be used by accepting an assignment on github classroom(the url is like: `https://github.com/rhodyprog4ds/portfolio-username`), if you are viewing the source repository(the name url is `https://github.com/rhodyprog4ds/portfolio`), you will have to fork first_  

## Setup Publishing

#### On GitHub

GitHub Actions are setup for publishing your Jupyter book on GitHub, you can view the rendered website by:
  - go to the 'Settings' tab at the top, scroll down to the 'GitHub Pages' section and set the `gh-pages` branch and `root` to the source. Then that page will show you the url of your rendered portfolio.Once you turn this on once, you'll be able to view your updates whenever you push changes to the `main` branch
  - Change to the `gh-pages` branch above and view `portfolio.pdf` to see your contents as a pdf, that you can download
  - Offline: switch to the `gh-pages` branch with `git checkout gh-pages` and pull that branch after you push to main.

_If you make your html public, for the semester, please keep it in the `rhodyprog4ds` organization. In December, if you wish you will be able to transfer ownership of your portfolio to your GitHub account to move it from `rhodyprog4ds.github.io/portfolio-username` to `username.github.io/whatever-you-want`._


#### You can build locally by:
  - follow the [Jupyter Book Setup Instructions](https://jupyterbook.org/start/overview.html) in order to build offline
  - follow the [Jupyter Book PDF Instructions](https://jupyterbook.org/advanced/pdf.html) in order to build to pdf offline

## Make it yours

- edit `_config.yml` to set your name as author
- edit `about/index.md` to be the introduction of your portfolio and a biography of yourself
- - change the logo if you wish


## Preparing for Portfolio Checks
_(not assignment 1, only portfolio checks)_

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
