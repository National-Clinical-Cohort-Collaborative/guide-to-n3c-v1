Book of N3C
==================

*[The Book of N3C](https://national-covid-cohort-collaborative.github.io/book-of-n3c-v1/)* is designed to guide research with the [National COVID Cohort Collaborative](https://ncats.nih.gov/n3c) (N3C).

The draft of the [draft outline](for-contributors/outline-draft.md) is available for viewing and editing.

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

<!-- badges: start -->
[![Build Book](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/actions/workflows/build-book.yaml/badge.svg)](https://github.com/National-COVID-Cohort-Collaborative/book-of-n3c-v1/actions/workflows/build-book.yaml)
<!-- badges: end -->

Funding
------------------

The N3C is supported by [NIH](https://www.nih.gov/) National Center for Advancing Translational Sciences ([NCATS](https://ncats.nih.gov/)).
