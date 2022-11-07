# Analyzing the Data {#sec-data-analysis}

:::{.callout-note}
This chapter is being drafted in Google Docs at
<https://drive.google.com/drive/u/0/folders/1RefwFn6mIitASq9IfPccN-T33iMohUEb>

See a draft of the chapter outline at
<https://docs.google.com/document/d/1ttUKgwVcIZHM87elrlUNV6Qi9thzOwKBg8GegKObEtg/>
:::

:::{.callout-warning}
At this point, any edits to this chapter should be made in Google Docs.  The current Markdown is for testing only.  It is NOT the source of truth (yet).
:::

**Chapter Leads: Amy Olex, Andrea Zhou**

**Chapter Contributors: Johanna Loomba, Evan French, etc…**


## Identifying Concept Sets

As data is ingested from the ever-growing list of data partners, the electronic health information coded in the various vocabularies used across the country are mapped to a single vocabulary of SNOMED CT. This is the core terminology for the OMOP common data model used within the enclave and a designated standard used to represent clinical meanings in a hierarchical structure. By leveraging the hierarchical structure, parent codes and descendants can be captured with ease to create intentional concept sets for use in analysis. For more details around the process of concept set creation, read the [authoring concept sets]#Authoring-Concept-Sets section.

The Concept Set Browser is an N3C specific tool that allows researchers to explore and modify existing concept sets as well as create new concept sets to fit their exact study needs. New researchers can start their search for a concept set with the list of N3C Recommended concept sets. These concept sets have been frozen in their validated state by the Logic Liaisons and the Data Liaisons after obtaining clinician and informatic reviews. These concept sets are the ones used to identify common comorbidities and other facts on the Phenotype Explorer and in the Logic Liaison Fact Table templates. The other method of finding commonly used concept sets is by exploring bundles within the Concept Set Browser. These are sets of concept sets that are often used together in a group. These are created by *** and used when ***.


## Using Concept Sets

Once concept sets have been identified for use in an analysis through the concept set browser, the concept set members table becomes the link between concepts and the encompassing concept set. Researchers can use concept sets by referencing the concept set name or the concept set version id also known as the codeset id. When searching for a concept set by name, it is recommended to also use most_recent_version = true to obtain the most up to date list of concept ids at any point in the analysis. This method is highly favored if the concept set is marked as N3C Recommended since these concept sets can only be updated by a small number of approved users after they have gone through re-validation, if necessary, following updates such as vocabulary changes. Researchers may choose to look up concept sets in the concept set members table by their codeset id if they wish to use the current most recent version of a concept set that is not N3C Recommended as any user can make edits to these concept sets. This will allow researchers to perform their analysis from start to finish without worry that someone has modified their concept set midstream without their knowledge. The other instance in which a researcher may choose to reference a concept set by codeset id is when choosing to use a specific prior version of an existing concept set.


## Using the Knowledge Store

The N3C Knowledge Store is an application where Enclave users can discover shared Code Templates, External Datasets, Reports, Cohorts, and Python Libraries (all also known as Knowledge Objects) and share similarly re-usable Knowledge Objects of their own with other Enclave users, regardless of the specific DUR from which the resource originated. Majority of Knowledge Store objects come about as core contributors and researchers alike develop resources they believe may be useful for others either within or outside of their research project team and wish to share them with the broader community. If you find yourself in this situation, you can easily create a KS resource that can be shared using Palantir’s documentation around templatization and submitting to the Knowledge Store. Otherwise, more specifics on how to navigate the Knowledge Store can be found in this [guide]#Knowledge-Store-Guide within the Enclave. Of the many types of Knowledge Objects, the most common are code templates and datasets.

Datasets in the Knowledge Store can be internal or external datasets. Internal datasets are generated from data inside the enclave, typically by researchers as part of their project, and are often of patient level granularity. External datasets found in the Knowledge Store provide a wealth of information from public datasets that have been brought into the Enclave along with the crosswalks necessary for joining these aggregate data to person level data at various levels of granularity. Either type of dataset can be imported into a workbook or code repository to be used as a starting point for further transformation or analysis.

Depending on the author’s intended use, some code templates can be applied to a researcher’s custom input dataset while other code templates produce a dataset that can be joined with a researcher’s study cohort. The code templates can also be imported and customized to produce a dataset for study analysis or simply used as example logic for Enclave users who are newer to coding. A few helpful starter templates are those produced by the [Logic Liaisons]#N3C-Logic-Liaisons. Through surveying the Domain Team Leads to establish a list of commonly derived variables and continuous feedback from the N3C Community to refine and update this list, the Logic Liaisons have developed, disseminated, and continue to maintain two master fact templates. These two master fact templates each produce visit-level and person-level data frames of commonly used derived variables for [all N3C patients]#All-Patients-Template as well as a subset who have an index date for their acute COVID-19 infection, the [confirmed COVID-19 Positive patients]#Confirmed-Covid-Pts-Template (PCR/AG positive or U07.1 COVID-19 diagnosed).

The Logic Liaisons have also developed, disseminated, and continue to maintain a handful of sister fact templates and data quality templates in the Knowledge Store. The sister templates utilize the visit-level and person-level datasets of the master fact template to efficiently generate additional derived variables based on broadly requested and applicable logic such as study-specific fact indexing, co-occurrence, and CCI score calculations. The data quality templates provide a variety of visualizations for looking at [data density of the OMOP domain tables]#Data-Density. When looking to assess study specific variables, the [Systematic Missingness template]#Systematic-Missingness provides an all or nothing fact density indicator while the [Fact Density by Site template]#Fact-Density provides relative densities of a fact across sites. [Training materials]#Logic-Liaison-Tutorials for getting started with Logic Liaison templates are available within the Enclave.

While it is not necessary to utilize Knowledge Store resources when conducting your research project, it does allow you to get a jumpstart on gathering and understanding the data by avoiding effort duplication and providing a general starting point. The Logic Liaison fact templates are specifically designed to provide a validated and community agreed-upon method for calculating particular facts at the encounter level and/or the patient level. The Logic Liaison data quality templates provide the same structure for analyzing data missingness, density, and contribution quality by site.


## Enclave Applications

This section will cover the usage of various applications made available in the N3C Enclave, including Contour, Code Workbooks, Reports, and more (a complete list of Foundry applications can be found here).  However, before designing and running an analysis utilizing data in the Enclave, it helps to understand the concept of a “data transformation” and how the data is stored and accessed via SPARK on a distributed file system.


### 10,000 foot view of distributed file systems, SPARK, and data transformations

Data in the N3C Enclave is so large it cannot be stored all in one giant table.  Instead it is stored on multiple servers in what is called a “distributed file system” where sets of rows in a table may be stored across multiple physical servers (Figure 1). Accessing these multiple servers to get data from one table requires a lot of coordination behind the scenes.  SPARK is the program coordinating the fetching, writing, and analysis of data.  You, as an Enclave user, can interface with SPARK through familiar Python, R, and SQL commands in order to retrieve data and run your analysis.  You don’t necessarily need to know all of the details in how SPARK operates to run basic code; however, when working with data in the N3C Enclave it is highly recommended to get more acquainted with how SPARK operates in order to optimize your code to make it run faster (like WAY faster).  You can reference Chapter X of this book, or Palatir’s SPARK Fundamentals and SPARK Optimization modules for more details on SPARK and how to optimize your code.  For the rest of this chapter we are just going to focus on how SPARK uses “data transformations''.

The basics of a data transformation are illustrated in Figure 2A. _<span style="text-decoration:underline;">One or more tables are specified as the input</span>_ and are transformed into a single output table.  Multiple transformations can be strung together (Figure 2B) to create an analysis pipeline (see Palatir’s Anatomy of a Data Pipeline module for more detailed information, as well as Best Practices in Chapter X).  _<span style="text-decoration:underline;">The primary and required output is always a single table</span>_; however, visualizations such as graphs and charts can also be generated and saved along the way.  You, the user, define the transformations using Enclave applications like Contour and Code Workbooks. Fusion sheets can be utilized to manually create tables for input into an analysis (e.g. to hold configuration options or frequently used codesets), and Reports are used to compile and display analysis results such as summary tables, graphs, and charts.  In the following sections, each of these applications is discussed in more detail.


### Contour

Foundry’s Contour application is a programming-free interface to the N3C Enclave that allows those with limited knowledge of Python, R, and SQL to create top-down analysis pipelines in a point-and-click fashion, as well as interactive dashboards for sharing results.  It is best used to quickly summarize and visualize data, and usage of Contour’s expression language allows for more complex querying and data aggregation.  One of the advantages of Contour is the ability to quickly and easily create summary figures with various complexity from source tables without having to code.  Contour has a variety of figure options, including bar charts, histograms and heatmaps. A detailed orientation to Contour can be found in the Foundry Documentation here.


### Fusion

Palantir Documentation: [Fusion Sheet Overview](https://unite.nih.gov/docs/foundry/fusion/overview/)



* Useful for writing back datasets for use within the Enclave
* Leverage cell references and spreadsheet functions
* Index datasets
* Sync tables to a dataset to use in other Foundry applications
* Import xls data
* Create charts
* Allows customization and flexibility
*

Fusion is a spreadsheet application within the Enclave analogous to Excel or Google Sheets. Palantir has curated [extensive documentation](https://unite.nih.gov/docs/foundry/fusion/overview/usion/overview) describing its core functionality as well as providing select how-to tutorials. The primary utility of Fusion is to allow users to sync specific cell ranges of values within a spreadsheet to datasets, which can subsequently be [imported]#Importing-and-Viewing-Data into any other Enclave application. This tool is an excellent option for use cases which require manual data entry, such as curating lists of [concept sets]#Concept-Set-Section to configure the [Logic Liaison Fact Templates]#LL-Fact-Templates. Unlike many other Enclave applications, Fusion is not suitable for large datasets; it has a maximum size restriction of 50 MB per document. Similar to Google Sheets, Fusion allows users to simultaneously edit the same document and view other users’ changes in real time.

As any Excel super user knows, a spreadsheet is not merely a mechanism for storing data, but also a powerful tool for analyzing, visualizing, and applying complex logical operations on data in its own right. Fusion provides many features familiar to other spreadsheet applications such as cell-referencing formulas, formatting, and a charting library to name a few. External .xls/.xlsx formatted files (up to 4 MB) can be directly imported into the Enclave as Fusion sheets with all cell references, formulas, and formatting preserved. [caveat].

In addition to standard spreadsheet functionality, Fusion has additional features which allow it to bi-directionally integrate with the rest of your Enclave environment. The first such feature is the ability to import other Enclave datasets into Fusion. Prior to using any dataset in Fusion (including datasets synced from Fusion sheets), it must first be indexed into a non-distributed format using the _Data _tab in the top menu. You can view available indexed datasets using the _Data>Datasets available_ menu option. Objects created within Fusion, such as formatted tables can be embedded in [reports]#Reports. Finally, Fusion sheets can be templatized to facilitate replication of similar functionality.


### Code Workbooks

Tutorial: [Intro to Code Workbook](https://unite.nih.gov/workspace/module/view/latest/ri.workshop.main.module.e7b83a8c-545e-49ac-8714-f34bfa7f7767?view=focus&Id=22)

Palantir Documentation: [Code Workbook Overview](https://unite.nih.gov/workspace/documentation/product/code-workbook/overview)



* graphical organization of logic
* Simplification of code
* easy reuse of pre-authored logic
* Add visualizations from here to reports
* Supports Python, R, and SQL
* Branching facilitates collaboration
* Workspace to reuse templatized logic

Code Workbook is a GUI-based application for users to apply code-based transformations to datasets for the purpose of creating new datasets and visualizations. The explicit goals of the application are to facilitate a collaborative environment in which users can quickly iterate over logic to produce artifacts interoperable with the suite of Enclave applications. The default Code Workbook interface is structured as a directed graph in which nodes represent either datasets or transformations which can output datasets. Edges represent the flow of data through the graph such that upstream datasets are inputs for logical operations performed by downstream code transforms (see Figure). Any dataset which a user has access to within the workspace where the Code Workbook is located can be imported as an input to the various types of transform.


#### Types of Transform



* **Manual Entry** transforms allow users to manually curate non-persisted datasets directly in the Code Workbook as a “quick and dirty” alternative to manually curating persisted datasets with [Fusion]#Fusion.
* **Python Code** transforms let users write a Python function with input datasets as input parameters.
* **R Code** transforms let users write an R function with input datasets as input parameters.
* **SQL Code** transforms let users write a SparkSQL query to create a new dataset from the available inputs
* **Template **transforms are parameterized blocks of reusable code which users can configure from a point-and-click interface. Many code templates are available in the [Knowledge Store]#Knowledge-Store, but users can also create their own templates scoped to their DUR workspace. Multiple single-node templates can be combined to create a multi-node template to allow reuse of entire configurable pipelines.
* **Visualize **transforms offer a point-and-click interface for users to create charts, distributions, histograms, and pivot tables. Note this transform is only available for saved datasets.

Both Python and R transforms can optionally return a single dataset and produce visualizations using Python libraries/R packages. Any visualization produced in a Code Workbook and subsequently be embedded in a [Reports]#Reports document. Datasets returned by a transform are ephemeral by default, that is, the transform must be recomputed each time the dataset is used as a downstream input, but options exist to conserve compute power by either caching or saving the output. Caching stores the output temporarily, while saving the dataset stores it permanently in the Enclave. It is recommended that transforms in a pipeline requiring significant compute be saved as datasets to reduce iteration time during development. Once a dataset is saved, users can set triggers and schedules for it to be automatically updated when certain input datasets are updated or at regular temporal intervals.

Tooling is available within Code Workbooks to facilitate the application objective of quick iteration. The console feature, located in the top right, allows users to interactively explore logic and syntax in Python, R, or SQL outside of a transform node. Also in the top right, is the Global Code section where users can globally import Python libraries and R packages or define custom functions to be used in any transform in the Code Workbook. Code transforms include a Logs feature for users to view console output generated by code and to view detailed stack traces when transforms fail due to an error.

Many Python and R transforms rely on external libraries and packages which can be made available via the Environment Configuration. The Enclave provides a number of default configurations tailored to common use cases, for instance, the _default_ profile, which includes common packages like pandas and tidyverse is suitable for routine analysis, whereas the _profile-high-memory_ profile includes packages like founder_ml to facilitate machine learning. Users can create their own Environment Configurations which include packages meeting their specific needs. Not all libraries and packages are included in the list of options, but users can [submit a ticket]#Tickets to request additional packages be made available. The Enclave maintains instances of the non-custom configurations on warm standby, allowing them to be quickly initialized when a user requests a new environment. Custom configurations require more time for initialization as instances of these must be started from scratch rather than merely assigned. For this reason, it is recommended to use non-custom configurations when possible.

Following best practices for collaborative software development, Code Workbook allows for branching of the logic within a workbook. As with other popular source control technologies (i.e. git), branching allows users to make copies of a workbook which they can develop independently of the source workbook. Once the development in a particular branch is deemed complete, it can be merged back into the originating branch. Prior to the merge, users can preview both line-level differences within each node, as well as node-level differences of nodes that have been added/removed. Good practice dictates that individual users perform all development on individual branches, which are then merged back into a common _master_ branch. Because the _master_ branch can change in the interval between a user cutting a branch and merging it back in, previewing merge changes is an important step for ensuring that the individual’s changes are both correct and compatible with the current state of the _master_ branch. Another prime use case for code branching is to ensure the reproducibility of a given dataset used in a research project. Because the OMOP and N3C-curated datasets are also versioned, teams can create a code branch in which all input datasets are set to the same version release to effectively freeze a dataset used in a specific analysis for later reproducibility while still allowing the possibility of adding additional features. User generated datasets are set to the same branch as the Code Workbook in which they were created.

Palantir has created extensive [documentation](https://unite.nih.gov/workspace/documentation/product/code-workbook/overview) of the Code Workbook application including tutorials. N3C has also published [training materials](https://unite.nih.gov/workspace/module/view/latest/ri.workshop.main.module.e7b83a8c-545e-49ac-8714-f34bfa7f7767?view=focus&Id=22).


### Reports

Palantir Documentation: [Reports Overview](https://unite.nih.gov/workspace/documentation/product/reports/overview)



* display charts and visualizations in combination with text descriptions about the analysis
* Collaborate with others through comments on the reports
* Add context by attaching images and other files
* Create a story around analysis results
* Useful when sharing results or even just putting together preliminary look at the progress

Many research projects in the Enclave are complex, involving multiple summary datasets, statistical analyses, and visualizations scattered across multiple applications and documents. Reports is a tool for consolidating various research artifacts from multiple sources within the Enclave into a single coherent document. Formatted [Fusion]#Fusion tables, [Contour]#Contour charts, Python/R-generated images from [Code Workbooks]#Code-Workbooks, and more are all embeddable in a Reports document, with the option to add a title and/or caption for each embedded artifact. Users can also create sections and provide narrative structure to their documents using MarkDown blocks. All components of a Reports document can be arranged and configured using a point-and-click interface.

All embedded objects can be configured to refresh automatically when the underlying data sources update, allowing Reports to function effectively as dashboards. Reports are also useful for presenting an executive summary of results for internal stakeholders as well as external presentations. [Logic Liaison Templates]#LL-Templates in the [Knowledge Store]#Knowledge-Store generally includes a README which is created using Reports. Reports can be requested for download using the Download Request Form. Palantir has curated [documentation](https://unite.nih.gov/workspace/documentation/product/reports) for creating and editing Reports.


### Object Explorer

Palantir Documentation: [Object Explorer](https://unite.nih.gov/workspace/documentation/product/object-explorer/overview)

Tutorial: [Exploring N3C Projects and Collaborators with Object Explorer](https://unite.nih.gov/workspace/module/view/latest/ri.workshop.main.module.e7b83a8c-545e-49ac-8714-f34bfa7f7767?view=focus&Id=27)



* Easily find objects of interest
* Compare and contrast items

A step upstream of the Knowledge Store is Palantir’s Object Explorer which allows users to explore and analyze objects of interest through a point and click interface. Detailed information around how to use this feature can be found in [Palantir’s documentation here]#Object-Explorer. Researchers can find unpublished Knowledge Objects, [explore N3C Projects and Collaborators]#Object-Explorer-Tutorial, view object usage statistics, etc. using this application.


### Data Lineage (aka Monocle)

Whether you’re creating a pipeline for data analysis specific to your research project or investigating one you came across in the Knowledge Store to determine if it will be useful to your study, you’ll likely want the capability to holistically assess how that dataset came about. The Data Lineage tool within the Foundry platform allows users to do just that - easily explore data pipelines from start to finish. With upstream on the left and downstream on the right, this tool makes for an intuitive way to visualize the relationships between datasets and their ancestors or descendants with enhanced views made possible through color-coding and grouping based on a dataset’s details. This application is particularly useful if a researcher needs to schedule a build for a dataset to update with the weekly refresh of data in the enclave. Palantir Documentation provides [a short tutorial](https://unite.nih.gov/workspace/documentation/product/foundry-training-portal/tutorial-data-lineage-basics) and [additional descriptions](https://unite.nih.gov/workspace/documentation/product/foundry-training-portal/introduction-to-data-lineage) of this tool’s functionality.


### Code Repositories


### Protocol Pad

[Quick Guide](https://unite.nih.gov/workspace/notepad/view/ri.notepad.main.notepad.8e97750f-d764-4df9-bb25-42ab32fcaa26)

[Detailed Guide](https://unite.nih.gov/workspace/notepad/view/ri.notepad.main.notepad.9d509aa3-7c76-42b3-a891-076a6f450f37)

Research studies can span many months and pass through the hands of many team members before reaching a stage where the researcher may want to share the results through publication or other approved means. The Protocol Pad serves as an electronic lab notebook to help organize tasks, track progress, and document results in a cohesive format throughout the process of reaching a study’s final state.


## DRAFT Language

To demonstrate the use of Contour we will work through a simple use-case using the SynPuf Synthetic dataset to summarize patient demographics as a bar chart, filter a table, join in additional information from another table, and calculate a patient’s age.


#### Interface Overview

Before we get started, let’s get oriented to the interface for the Contour application.  To create a new Contour analysis click on the “+ New” button (Figure &lt;new_button>) and select the “Analysis” option (Figure &lt;analysis_option>).  A new Contour analysis will open, and you will see a window similar to that in Figure &lt;contour_interface>.  To change the name of this analysis, click on the last entry in the path (Figure &lt;contour_interface>, A).  This path can also be used to navigate back to previous parent directories in the Enclave.  To the right of the analysis name is a drop-down indicating you are in “Editing mode” (Figure &lt;contour_interface>, B). Note that if more than one person has the same workbook open only one person will be given Editing privileges while the other will be in Viewing Mode.

The center of the screen is your working space.  Currently it is empty because we have not added any datasets for analysis.  To add a new data set for analysis, click on the “+ Create new path” button in the center of the screen (Figure &lt;contour_interface>, C), or the plus “+” button towards the top of the window ((Figure &lt;contour_interface>, D).  The term “path” in Contour is used to indicate the location of a data set.  Each time you “Create a Path” you are telling the application which data set to start with, whether it be a source OMOP table or the output from another Contour analysis.


#### Importing and Viewing Data

As discussed in the introduction to this chapter, all analyses work through transformations, and Contour is no exception.  Analyses in Contour are built as a pipeline working from top to bottom.  To start an analysis we need to import a starting dataset (i.e. create a new path).  Click on the “+ Create new path” button, then navigate to the OMOP “person” table in the Synpuf Dataset by going to “All” > “Data Catalog” > SynPuf Synthetic Data” > “person” (Figure &lt;create_path>).  Your window should now look similar to Figure &lt;analysis_start>.

In this view there are 3 sections to be aware of:



1. Starting dataset
2. Transformations (currently there are none)
3. Resulting dataset (can be saved as a table or imported into another analysis as the starting path)

To add a transformation (a.k.a. board), just click on one of the suggestions (Figure &lt;analysis_start>, B), or you can hover over one of the arrows before or after the suggestions and select “Insert Board” (Figure &lt;insert_board>).  These arrows will also appear before and after each transformation so you insert a transformation anywhere in the pipeline.  Just be aware it will change all results downstream!

Notice at the top where the “+” button is (Figure &lt;analysis_Start>, red box) there is a new tab named “person”.  You can create multiple analysis workflows within the same Contour analysis and navigate through them using the tabs.

Now we have imported our first data set, however notice it is not displaying the table for a preview.  Within Contour, to see the data you specifically have to tell it to create a table as one of the transformations. To preview the data in the “person” table, click on the “Visualize” button and scroll down to “Table” (Figure &lt;table_viz>).  Your screen should look like Figure &lt;table_preview>.


#### Creating Summary Figures

One of the advantageous things about Contour is that it is easy to quickly create summary figures of various complexity from source tables without having to code.  Contour has a variety of figure options, including bar charts, histograms and heatmaps.

To create a bar chart of our example data, look through the table preview to identify the column name that has the variable you want to plot.  In our instance it will be “race_concept_name”.  Create a new transformation below the table preview for a bar chart (named “Chart” in the list, Figure &lt;bar_chart_options>).  Initially the chart is empty because we have to tell it which columns to use.  In the “Data” tab on the right, set the X-Axis to be “race_concept_name”, and the Y-Axis to be “person_id” and “Unique count” (Figure &lt;bar_char_options_set>), then click on  \
Compute & save” to view the chart (Figure &lt;bar_chart_figure>).  You can utilize the “segment by” option to segment your primary column by a secondary column (Figure &lt;bar_chart_segmented>), as well as explore some of the other options available.  Note that each visualization option will have its own parameters.  You can review Foundry’s documentation for more details on each of these.
