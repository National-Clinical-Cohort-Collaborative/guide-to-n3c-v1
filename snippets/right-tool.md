Choosing the Right Tool for each part of the Project
--------------

*likely chapter: ?*

As described in the N3C Ecosystem chapter, a single pipeline can easily integrate SQL, Python, and R code.  This flexibility allows your team to mix and match the tools to best suit the team's needs and abilities.

We recommend that typical projects use SQL Transforms for the data manipulation and use Python or Spark Transforms for the analysis.

For the past 30 years, SQL has been the de facto language for large datasets like the N3C. It is well-suited for efficiently (a) selecting patients following exacting selection criteria, (b) joining a variety of predictor and outcome variables from multiple tables, and (c) producing a dataset better suited for analyses.  Consequently it is a common ability for people in data science and IT.

To capitalize on the well-established SQL base, Spark and other data-centric applications expose a SQL-like API.  Spark stores and manipulates data very differently than traditional relational database engines, however Hive and Spark SQL allow developers to transform data following familiar concepts and syntax.

Our rule of thumb is to transform it in SQL if SQL can comfortable transform it.  Otherwise use R or Python to transform it.
