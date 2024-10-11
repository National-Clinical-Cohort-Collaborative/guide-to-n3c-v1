(This text was in the welcome/preface page.  It may still be useful later.)

Platform
------------------

<!-- The section is manually duplicated between index.qmd and README.md. -->

As the chapters are being written, talk to the chapter's Lead Author to learn if it's being written in GitHub or Google Docs.  Eventually all Google Docs chapters will be translated to Markdown.  Once a chapter has been finally converted to Markdown...

### Minor Changes

To make small changes like spelling corrections, we recommend editing the source directly in GitHub.  It handles the details without your knowledge (like starting a fork and prompting your pull request).  From the appropriate page of [the book](https://national-clinical-cohort-collaborative.github.io/guide-to-n3c-v1/), click on the "Edit this page <i class="fab fa-github" aria-hidden="true"></i>" button and type your change in the [GitHub editor](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

### Larger Changes and Additions

Substantial edits and writing are better accommodated by a text editor on your local machine that can preview the rendered content as you type.  We suggest [Visual Studio Code](https://code.visualstudio.com/) or [RStudio](https://www.rstudio.com/products/rstudio/).

### Details

You don't have to understand the rest to contribute, but for those interested:

* The majority of this book is written in a collection of [Markdown](https://guides.github.com/features/mastering-markdown/) documents and assembled by the [Quarto](https://quarto.org/).

* After your change is pushed to GitHub, a [GitHub Action](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) spawns a small VM that (a) collects all the Markdown documents, (b) calls [Quarto](https://quarto.org/)/[Pandoc](https://pandoc.org/) to convert them to html, and (c) moves the rendered html files to the "gh-pages" branch.

* GitHub Pages serves the contents of the [`gh-pages` branch](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/tree/gh-pages) to anyone with a browser.


Contributing Content
------------------

The N3C and its [domain teams](https://covid.cd2h.org/domain-teams) are healthiest when assimilating contributions from reseachers of different skills (e.g., clinicians & informaticians), specialties (e.g., endocrinology & gerontology), programming languages (e.g., Python, R, & SQL) and experiences (e.g., students & PIs).

Accordingly, the [guide-to-n3c-v1](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1) repository welcomes input from you.

If you see a small mistake or unclear language, we invite you to inform us in a [new issue](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/issues) or to edit the source and submitting a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).  When an editor reviews and accepts your change, the website will be updated within minutes.

If you have an idea for something more substantial such as a chapter or section, please start a [new issue](https://github.com/national-clinical-cohort-collaborative/guide-to-n3c-v1/issues) and the N3C Educational Committee will coordinate with you where it fits best.