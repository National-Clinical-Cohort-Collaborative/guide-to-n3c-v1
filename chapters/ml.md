---
author:
  - name: Peter Robinson
    affiliation: The Jackson Laboratory
    affiliation-url: https://robinsongroup.github.io/
    # email: Peter.Robinson@jax.org
    # orcid:
    attributes:
      corresponding: true

  - name: Justin Reese
    affiliation: Lawrence Berkeley National Lab
    affiliation-url: https://www.lbl.gov/
    # email: justaddcoffee@gmail.com
    # orcid:

csl: ../assets/csl/apa-7e.csl
---

# Special Topic: Machine Learning {#sec-ml}

**Chapter Leads:** Peter Robinson, Justin Reese, Blessy Antony, T.M. Murali, Elena Casiraghi, Hannah Blau

## Introduction {#sec-ml-introduction}

Machine learning (ML) is a method of teaching computers to learn a classification or regression function from data, or detect patterns (e.g., clusters) in data, without explicitly programming the model. Machine learning is a powerful tool for solving complex problems, and it is widely used in biomedicine and many other fields.

For biomedical applications, two main types of ML algorithms are generally used: supervised and unsupervised.  In supervised learning, the labels (i.e., true classifications) for the input data used to train the model (e.g. which patients have a disease of interest, or develop an outcome of interest) are known. The goal of supervised learning is to learn a mapping function that can accurately predict the label for new, unseen input examples. A practical example of classification is reported in one of the first publications by the [ML Domain Team](onboarding.md#dt), in which the aim was to classify COVID-patients based on their prognosis [@casiraghi_2020].

In unsupervised ML, models are trained on input data without labels. In this case, the algorithm aims to discover structure within the data in order to facilitate the assignment of labels. One of the most widely known unsupervised ML techniques is clustering, which aims at partitioning the input cases into classes, where each class corresponds to similar cases according to a similarity/dissimilarity metric. In the clinical/medical field, clustering is often used to identify subtypes of a disease of interest. A practical example of clustering was also recently published by our ML group on the identification of long-COVID subtypes [@reese_2023].

The intention of this chapter is to demonstrate how to perform ML in N3C by walking the reader through a specific ML use case with working code. 

## Good Algorithmic Practice (GAP) {#sec-ml-gap}

Knowledge of GAP is crucial to the successful application of machine learning to biomedical data. We intend to demonstrate GAP in this chapter by example. A full discussion of this is beyond the scope of this document, but a partial list of important considerations, with references for further reading, is as follows:

* **Generalizability** - models trained on one set of data often do not perform well on data originating from other places (e.g. other hospital systems) or other times (e.g. in a different period of time in the COVID pandemic) [@roberts_2021]. Since the goal of supervised machine learning is to develop generalizable algorithms that perform well on completely unseen (i.e., independent) test data, practitioners must be familiar with various techniques and considerations that mitigate the risk of failure to generalize (i.e., model overfitting) in the appropriate context, such as regularization, dimensionality reduction, feature extraction, cross-validation, and use of a model type that is appropriate given the amount of available data (e.g., deep learning algorithms may require relatively large training sets) [@chollet_2021, @geron_2022]. The machine learning practitioner should thoroughly understand the potential trade-off between under-fitting and overfitting a predictive model [@hastie_2009]. In addition, N3C data is not a random sample, and it worth familiarizing yourself with the data as described in Chapters [-@sec-understanding] and [-@sec-cycle].
* **Social bias** - scientific literature abounds with ML models and results that contain bias with respect to factors such as gender, ethnicity, and race. It is critical to realize that the choice of data or ML model may reinforce harmful bias in scientific literature [@roberts_2021]. This can happen even if you do not intend to introduce such a bias.
* ...