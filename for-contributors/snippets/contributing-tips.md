(This text was in the welcome/preface page.  It may still be useful later.)

Platform
------------------

<!-- The section is manually duplicated between index.qmd and README.md. -->

As the chapters are being written, talk to the chapter's Lead Author to learn if it's being written in GitHub or Google Docs.  Eventually all Google Docs chapters will be translated to Markdown.  Once a chapter has been finally converted to Markdown...

### Minor Changes

To make small changes like spelling corrections, we recommend editing the source directly in GitHub.  It handles the details without your knowledge (like starting a fork and prompting your pull request).  From the appropriate page of [the book](https://national-covid-cohort-collaborative.github.io/guide-to-n3c-v1/), click on the "Edit this page <i class="fab fa-github" aria-hidden="true"></i>" button and type your change in the [GitHub editor](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

### Larger Changes and Additions

Substantial edits and writing are better accommodated by a text editor on your local machine that can preview the rendered content as you type.  We suggest [Visual Studio Code](https://code.visualstudio.com/) or [RStudio](https://www.rstudio.com/products/rstudio/).

### Details

You don't have to understand the rest to contribute, but for those interested:

* The majority of this book is written in a collection of [Markdown](https://guides.github.com/features/mastering-markdown/) documents and assembled by the [Quarto](https://quarto.org/).

* After your change is pushed to GitHub, a [GitHub Action](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) spawns a small VM that (a) collects all the Markdown documents, (b) calls [Quarto](https://quarto.org/)/[Pandoc](https://pandoc.org/) to convert them to html, and (c) moves the rendered html files to the "gh-pages" branch.

* GitHub Pages serves the contents of the [`gh-pages` branch](https://github.com/National-COVID-Cohort-Collaborative/guide-to-n3c-v1/tree/gh-pages) to anyone with a browser.
