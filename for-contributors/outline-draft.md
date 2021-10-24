# Part: Getting Started

## Chapter: Welcome

### Chapter: N3C Patients

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

# Part: Data Structure

## Chapter: OMOP

> The OMOP Common Data Model is developed and maintained by OHDSI

### Section: Need for a Common Data Model

### Section: Upstream Sources

> An EMR does not store data in an OMOP-compliant format.  Transaction vs Warehouse architecture.  Translated to OMOP from EMR or PCoreNet or...

### Section: Common N3C-OMOP Gotchas

## Chapter: Codesets

## Chapter: N3C-Specific Tables

# Part: Analysis

## Chapter: Palintir Enclave

### Code Workbook

### Code Repository

## Chapter: Architecture

### Section: Choosing the Right Tool for each part of the Project

> We recommend that typical projects use SQL Transforms for the data manipulation and use Python or Spark Transforms for the analysis.  
>
>For the past 30 years, SQL has been the defacto language for large datasets like the N3C. It is well-suited for efficiently (a) selecting patients following exacting selection criteria, (b) joining a variety of predictor and outcome variables from multiple tables, and (c) producing a cache

consequently many people

### Section: Dataset Caching

### Section: Dataset Visibility

### Section: Template

## Chapter: SQL Transforms

## Chapter: Python Transforms

## Chapter: R Transforms

> This a rich library of {SQL|Python|R} books for all experience levels.  This chapter doesn't try to reproduce that body of work.  It first introduces the basics of {SQL|Python|R} needed to complete a basic example.  It then provides a list of references to further your {SQL|Python|R} education.  Finally, we emphasize the differences between using {SQL|Python|R} in Enclave vs in more conventional environments.

## Chapter: Spark Transforms

## Chapter: Tool Grab Bag

### Section: Site Selection

### Section: Parallel Collaboration

### Section: Incorporating External Datasets

> The N3C patients are collected

## Chapter: Reproducibility

> Like most empirical investigations using patient data, tradeoffs must be considered tha balance the competing priorities of transparency of the researcher vs protection of the patient.

### Section: Permission to Download

## Chapter: Publication Process

# Part: Style Guide

> Using a consistent style across your projects can decrease the overhead as your data science team discusses options, decides on a good choice, and develops in compliant code. But like in most themes in this document, the cost is worth the effort. Unforced code errors are reduced when code is consistent, because mistake-prone styles are more apparent.
>
> {Copied from <https://ouhscbbmc.github.io/data-science-practices-1/style.html>}

## Chapter: Naming

## Chapter: Sandbox to Production Code

# Part Start-to-Finish Examples

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

