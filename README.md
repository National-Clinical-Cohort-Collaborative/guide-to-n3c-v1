The Researcher's Guide to N3C
==================

*[The Researcher's Guide to N3C: A National Resource for Analyzing Real-World Health Data](https://national-clinical-cohort-collaborative.github.io/guide-to-n3c-v1/)* is designed to guide research with the [National COVID Cohort Collaborative](https://ncats.nih.gov/n3c) (N3C).

The rendered booked is accessible through either of these urls:
* [covid.cd2h.org/guide-to-n3c](https://covid.cd2h.org/guide-to-n3c) and
* [national-clinical-cohort-collaborative.github.io/guide-to-n3c-v1](https://national-clinical-cohort-collaborative.github.io/guide-to-n3c-v1).

Contributing Content
------------------

The N3C and its [domain teams](https://covid.cd2h.org/domain-teams) are healthiest when assimilating contributions from reseachers of different skills (e.g., clinicians & informaticians), specialties (e.g., endocrinology & gerontology), programming languages (e.g., Python, R, & SQL) and experiences (e.g., students & PIs).

Accordingly, the [guide-to-n3c-v1](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1) repository welcomes input from you.

If you see a small mistake or unclear language, we invite you to inform us in a [new issue](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/issues) or to edit the source and submitting a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).
When an editor reviews and accepts your change, the website will be updated within minutes.

If you have an idea for something more substantial such as a chapter or section, please start a [new issue](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/issues) and the N3C Educational Committee will coordinate with you where it fits best.

Platform
------------------

<!-- The section is manually duplicated between index.qmd and README.md. -->

As the chapters are being written, talk to the chapter's Lead Author to learn if it's being written in GitHub or Google Docs.
Eventually all Google Docs chapters will be translated to Markdown.
Once a chapter has been finally converted to Markdown...

To make small changes like spelling corrections, we recommend editing the source directly in GitHub.
It handles the details without your knowledge (like starting a fork and prompting your pull request).
From the appropriate page of [the book](https://national-clinical-cohort-collaborative.github.io/guide-to-n3c-v1/), click on the "Edit this page <i class="fab fa-github" aria-hidden="true"></i>" button and type your change in the [GitHub editor](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

Substantial edits and writing are better accommodated by a text editor on your local machine that can preview the rendered content as you type.
We suggest [Visual Studio Code](https://code.visualstudio.com/) or [RStudio](https://www.rstudio.com/products/rstudio/).

You don't have to understand the rest to contribute, but for those interested:

* The majority of this book is written in a collection of [Markdown](https://guides.github.com/features/mastering-markdown/) documents and assembled by the [Quarto](https://quarto.org/).

* After your change is pushed to GitHub, a [GitHub Action](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) spawns a small VM that (a) collects all the Markdown documents, (b) calls [Quarto](https://quarto.org/)/[Pandoc](https://pandoc.org/) to convert them to html, and (c) moves the rendered html files to the "gh-pages" branch.

* GitHub Pages serves the contents of the [`gh-pages` branch](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/tree/gh-pages) to anyone with a browser.

* The book can be previewed or locally rendered from the command line, avoiding complexities of RStudio if/when they get in the way. The commands are simply "quarto preview" and "quarto render". The first creates a server for the HTML and the second just generates the html files. Detail in the [Quarto docs on books](https://quarto.org/docs/books/) under "Publishing".
    * individual chapters can be rendered with: $ quarto render <chapter file> --to html


Assets
------------------

* [Directory on N3C Google Drive ](https://drive.google.com/drive/u/0/folders/1ZFxcvLvJUqMF_RbnQLo8rW7DTMTtahfY)

    ```sh
    //N3C allhands National COVID Cohort Collaborative (n3c-allhands@ctsa.io)/WORKSTREAMS & SUBGROUPS/Collaborative Analytics/Clinical Scenarios & Data Analytics subgroup/Clinical Domain Teams/Education and Training DT/Projects/Guide to N3C (Previously Book of N3C)/
    ```

* [Status Tracker of Chapters](https://docs.google.com/spreadsheets/d/18FWdK1jJXZxhB4t_CKyAHPWkSWIfg5kVcR0vF4_iqlI/edit#gid=0)

* [Ed Committee Notes](https://docs.google.com/document/d/1CmAKLcMQcVV_M1OV0zcIxfjiu0xiEWrfKkMMw8zRp6w/edit)
* [Topics Brainstorm](https://docs.google.com/drawings/d/1Z2k0UaukCNsmc8lcxB2lp9ZmOCqrszCWdtntwS4MpQE/edit)
* [Outline (current)](https://docs.google.com/document/d/1ttUKgwVcIZHM87elrlUNV6Qi9thzOwKBg8GegKObEtg/edit)
* [Outline (old)](for-contributors/outline-draft.md)

Funding
------------------

The N3C is supported by [NIH](https://www.nih.gov/) National Center for Advancing Translational Sciences ([NCATS](https://ncats.nih.gov/)).

Versioning and Build Status
------------------

Zenodo releases: [![DOI](https://zenodo.org/badge/415068439.svg)](https://zenodo.org/badge/latestdoi/415068439)

<!-- badges: start -->
GitHub Actions: [![Build Book](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/actions/workflows/build-book.yaml/badge.svg)](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/actions/workflows/build-book.yaml)
<!-- badges: end -->
