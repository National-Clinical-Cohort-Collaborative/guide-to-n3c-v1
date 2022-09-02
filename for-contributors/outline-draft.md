<!-- ---- Getting Started ------------------------------------------------------ -->

# Part: Getting Started

## Chapter: Welcome

## Chapter: N3C Patients

> The 1.5 million patients are collected from 60 US institutions

### Section: Covid-Positive Patients

### Section: Covid-Negative Patients

## Chapter: For Individual Researchers

### Section: User Registration

### Section: Data Use Request

#### Subsection: Privacy Level

> Level 0, 1, & 2 ...

### Section: Domain Teams

## Chapter: For Institutions

### Subsection: Data Use Agreement

<!-- ---- Personnel ------------------------------------------------------ -->

# Part: Personnel

> Each section in this chapter/part has two goals: (a) describe the roles needed for a typical N3C investigation and (b) help Site PIs understand and hire the appropriate skills and experience.
>
> Each role is described how they fit into a project.  Then an example description is provided that can be customized by an institution hiring for the position.

## Chapter: Personnel Verticals

### Section: Lead Investigator

### Section: Subject Matter Expert

### Section: Project Manager

### Section: Statistician

### Section: Administrator

## Chapter: Expertise Levels

### Section: Grad Students

### Section: Site PI

<!-- ---- Data Structure ------------------------------------------------------ -->

# Part: Data Structure

## Chapter: OMOP

> The OMOP Common Data Model is developed and maintained by OHDSI

### Section: Need for a Common Data Model

### Section: Upstream Sources

> An EMR does not store data in an OMOP-compliant format.  Transaction vs Warehouse architecture.  Translated to OMOP from EMR or PCoreNet or...

### Section: Common N3C-OMOP Gotchas

## Chapter: Codesets

## Chapter: N3C-Specific Tables

## Chapter: Checklist for Analysis/Submission

Curated list of recommendations that should be considered before taking an analysis too seriously. Similar to R's [Checklist for CRAN submissions](https://cran.r-project.org/web/packages/submission_checklist.html).  David Sahner suggested to organize it by OMOP domain (or maybe source table).  Maybe there's a priority icon that identicates if this is potentially a huge problem if ignored (*eg*, the hypothesis direction could be flipped) or a minor problem (*eg*, the coefficients might be a little off).

* List of open issues to be addressed:

* List of "Persistent Data Issues": https://unite.nih.gov/workspace/documentation/product/n3c-info/data-issues


<!-- ---- N3C Ecosystem ------------------------------------------------------ -->

# Part: N3C Ecosystem

## Chapter: Palantir Enclave

### Section: Code Workbook

### Section: Code Repository

### Section: Fusion

### Section: Other Enclave Applications

> Quick overview of the less-important & less-frequent parts of the Enclave.

## Chapter: Architecture

### Section: Choosing the Right Tool for each part of the Project

> As described in the N3C Ecosystem chapter, a single pipeline can easily integrate SQL, Python, and R code.  This flexibility allows your team to mix and match the tools to best suit the team's needs and abilities.
>
> We recommend that typical projects use SQL Transforms for the data manipulation and use Python or Spark Transforms for the analysis.
>
> For the past 30 years, SQL has been the de facto language for large datasets like the N3C. It is well-suited for efficiently (a) selecting patients following exacting selection criteria, (b) joining a variety of predictor and outcome variables from multiple tables, and (c) producing a dataset better suited for analyses.  Consequently it is a common ability for people in data science and IT.
>
> To capitalize on the well-established SQL base, Spark and other data-centric applications expose a SQL-like API.  Spark stores and manipulates data very differently than traditional relational database engines, however Hive and Spark SQL allow developers to transform data following familiar concepts and syntax.
>
> Our rule of thumb is to transform it in SQL if SQL can comfortable transform it.  Otherwise use R or Python to transform it.
>
> When decided whether to

### Section: Dataset Caching

### Section: Dataset Visibility

### Section: Template

## Chapter: Study Design for Secondary Use of Electronic Health Data

<!-- ---- Enclave Transforms ------------------------------------------------------ -->

# Part: Enclave Transforms

## Chapter: SQL Transforms

## Chapter: Python Transforms

## Chapter: R Transforms

> {SQL|Python|R} has many books for all levels of experience.  This chapter doesn't try to reproduce that body of work.  We first introduce the basics of {SQL|Python|R} needed to complete a basic N3C example.  We then emphasize the differences between using {SQL|Python|R} in Enclave vs in a more conventional environment.  Finally we suggest sources to further your {SQL|Python|R} education.

## Chapter: Spark Transforms

> Compared to SQL, Python, and R,

<!-- ---- Analysis III ------------------------------------------------------ -->

# Part: Analysis III

## Chapter: Tool Grab Bag

### Section: Site Selection

### Section: Parallel Collaboration

### Section: Incorporating External Datasets

> The N3C patients are collected

## Chapter: Reproducibility

> Like most empirical investigations using patient data, tradeoffs must be considered tha balance the competing priorities of transparency of the researcher vs protection of the patient.

### Section: Permission to Download

## Chapter: Publication Process

<!-- ---- Style Guide ------------------------------------------------------ -->

# Part: Style Guide

> Using a consistent style across your projects can decrease the overhead as your data science team discusses options, decides on a good choice, and develops in compliant code. But like in most themes in this document, the cost is worth the effort. Unforced code errors are reduced when code is consistent, because mistake-prone styles are more apparent.
>
> {Copied from <https://ouhscbbmc.github.io/data-science-practices-1/style.html>}

## Chapter: Naming

## Chapter: Sandbox to Production Code

<!-- ---- Start-to-Finish Examples ------------------------------------------------------ -->

# Part: Start-to-Finish Examples

## Chapter: Investigation - Rural Health Disparities

Pieces:

1. Primary Goals
2. DUR
3. Funding
4. Personnel
5. Coding
6. Analysis
7. Manuscript Development
8. Biggest Challenges
9. What we'd do differently if starting from scratch

## Chapter: Graduate School Summer Course - Simpson's Paradox

> An N3C project has many appealing characteristics to instructors developing a two-month course: (a) the data are already collected, documented, and available, (b) the hardware requirements are negligible because the NIH Spark Cluster...


## Chapter: Peter Robinson's ML Pipeline Group

{They already have existing examples that David Sahner thinks would be a great fit for the book.}

