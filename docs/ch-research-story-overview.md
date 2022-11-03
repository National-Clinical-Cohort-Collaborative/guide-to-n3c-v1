A Research Story {#story}
=========================

> 50,000-foot view of a research project, from onboarding to publishing

Now that we have introduced N3C and described its motivation and importance, we'll walk through the lifecycle of an example project from onboarding to publishing.  This path typically takes at least 6 months and 6 collaborators.  It is difficult to do by yourself, but fortunately the N3C has attracted a large and diverse set of researchers.  Coupled with a large and diverse set of patients, it is possible to complete a research project within a year.

If you are starting a project by yourself, you'll likely be able to recruit collaborators with a complementary set of skills (in addition to the resources such as [instructional material]() and [office hours]()).  If you would like to join an existing project, there are [domain teams](https://covid.cd2h.org/domain-teams) and ongoing projects that likely will fit your interests and benefit from your abilities.

Onboarding {#story-person}
----------------------------------------------

Before the first data point is viewed, three things should be established by you and your institution:

* {A person's paperwork.  Include ORCiD}
* {DUA coverage & An institution's paperwork.}
* {DUR & a project's paperwork.}

The startup costs are more expensive for an N3C investigation compared to most, but the incremental costs are cheaper.  Even with strong institutional support, the DUA will take several months in legal and administrative channels.  Yet after clearing that first (tall) hurdle for your site, each specific project takes only a few days to be processed by the N3C staff.  That's a remarkably short time for scale of available data.  It's likely quicker than initiating a project based on a single EMR from your site --much less EMRs from 70+ sites.

Team building & collaborating
----------------------------------------------

The next step is to build a team.  In a prototypical (non-N3C) single-site investigation with retrospective medical records, (a) a project manager and principle investigator interact with a single IRB, (b) a single person extracts the desired dataset from the EMR/warehouse, (c) a statistician models the predictors and outcomes, and (d) the principle investigator writes and submits the manuscript.

Personnel decisions with N3C research resembles most contemporary medical research in some ways, and differ in others.  The similarities include:

* Heterogenous skills are required.  Ideally team has (a) a subject matter expert who knows the literature and is able to form testable hypotheses, (b) a data engineer who understands the challenges of EMRs and is able to extract and transform OMOP tables, (c) a statistician who understands the limitations of observational data and is able to model retrospective data, and (d) a navigator who has learned the administrative requirements and is able to facilitate the investigation.

* Retrospective medical records are extracted from a larger dataset.  An investigation can use only a fraction of the terabytes in an EMR.  Many decisions are involve to include only the relevant variables among the qualifying patients.

The differences include:

* Most teams have researchers from at least three institutions.  In the experience of the chapter authors and the editors, this encourages more diverse opinions and more willingness to express constructive criticism.  Researchers from the same institution/lab are sometimes are more reluctant to express contrary views.

* The role of "navigator" is even more important.  Your local EMR investigations are likely guided by someone with years experience with the institutional safeguards and the personnel who can help when something stalls.  N3C is bigger and likely younger than your site's EMR research team, so an N3C project will benefit when guided by a bright, patient, and persistent navigator.

If your team needs someone, consider asking a relevant [domain team](https://covid.cd2h.org/domain-teams) for helping identifying and approaching a potential collaborator.

Protocol, variables, & definitions
----------------------------------------------

This aspect of the scientific process is probably both the most familiar and most vague.  Most researchers have several years of graduate-level courses and real-world experience.

{Mention CD2H's [Informatics Playbook](https://playbook.cd2h.org/en/latest/index.html)}

Creating an analysis-ready dataset
----------------------------------------------

{Conventional data engineer role.  Dataset is created with input from the analyst.}

Learning and using OMOP (e.g. concept sets)
----------------------------------------------

OMOP originated around 20qq to facilitate the detection of small but significant side effects from new pharmaceuticals.  Detecting a small signal requires a large datasets --larger than any single health care database. [Add footnote to Book of OHDSI]().  Since then, the foundation has supported many other research goals.  It is well-suited for N3C because:

* It has evolved from 10? years and accommodates a wide range of data sources
* It has an established community and documentation to help institutions convert their EMR to OMOP and to help researchers analyze their hypotheses.

{3-4 sentence description of the original OMOP motivation.  It standardizes (a) tables & columns and (b) vocabulary.  Spend 1-2 paragraphs on concept set, focusing more on motivations than the mechanics.}

Analyses
----------------------------------------------

* Developing the Analyses
* finalizing analysis
  * Pinning to a release
  * DRR
  * figures

Draft paper, pub committee
----------------------------------------------
