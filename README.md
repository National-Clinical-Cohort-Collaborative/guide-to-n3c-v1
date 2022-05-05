Book of N3C
==================

*[The Book of N3C](https://national-covid-cohort-collaborative.github.io/book-of-n3c-v1/)* is designed to guide research with the [National COVID Cohort Collaborative](https://ncats.nih.gov/n3c) (N3C).

Contributing Content
------------------

The N3C and its [domain teams](https://covid.cd2h.org/domain-teams) are healthiest when assimilating contributions from reseachers of different skills (*e.g.*, clinicians & informaticians), specialties (*e.g.*, endocrinology & gerontology), programming languages (*e.g.*, Python, R, & SQL) and experiences (*e.g.*, students & PIs).

Accordingly, the [book-of-n3c-v1](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1) repository welcomes input from you.

If you see a small mistake or unclear language, we invite you to inform us in a [new issue](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/issues) or to edit the source and submitting a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).  When an editor reviews and accepts your change, the website will be updated within minutes.

If you have an idea for something more substantial such as a chapter or section, please start a [new issue](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/issues) and the N3C Educational Committee will coordinate with you where it fits best.

Platform
------------------

To make small changes like spelling corrections, we recommend editing the source directly in GitHub.  It handles the details without your knowledge (like starting a fork and prompting your pull request).  From the appropriate page of [the book](https://national-covid-cohort-collaborative.github.io/book-of-n3c-v1/), click on the "Edit this page <i class="fab fa-github" aria-hidden="true"></i>" button and type your change in the [GitHub editor](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

Substantial edits and writing are better accommodated by a text editor on your local machine that can preview the rendered content as you type.  We suggest [RStudio](https://www.rstudio.com/products/rstudio/) or [Visual Studio Code](https://code.visualstudio.com/).

You don't have to understand the rest to contribute, but for those interested:

* The majority of this book is written in a collection of [markdown](https://guides.github.com/features/mastering-markdown/) documents and assembled by the [bookdown](https://bookdown.org/) package.  See [Yihui's book](https://bookdown.org/yihui/bookdown/) for the authoritative details.

* After your change is pushed to GitHub, a [GitHub Action](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) spawns a small VM that (a) collects all the markdown documents, (b) calls bookdown to convert them to html, and (c) moves the compiled products to the "gh-pages" branch.

* GitHub Pages serves the contents of the ["docs/" directory](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/tree/gh-pages/docs) (in the "gh-pages" branch) to anyone with a browser.

Assets
------------------

* [Directory on N3C Google Drive ](https://drive.google.com/drive/u/0/folders/1ZFxcvLvJUqMF_RbnQLo8rW7DTMTtahfY):

    ```sh
    //N3C allhands National COVID Cohort Collaborative (n3c-allhands@ctsa.io)/WORKSTREAMS & SUBGROUPS/Collaborative Analytics/Clinical Scenarios & Data Analytics subgroup/Clinical Domain Teams/Education and Training DT/Projects/Book of N3C/
    ```

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
GitHub Actions: [![Build Book](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/actions/workflows/build-book.yaml/badge.svg)](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/actions/workflows/build-book.yaml)
<!-- badges: end -->
