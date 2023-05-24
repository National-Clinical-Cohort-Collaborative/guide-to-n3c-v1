---
abstract: 40,000-foot view of a research project, from onboarding to publishing

author:
  - name: William H Beasley
    affiliation: University of Oklahoma Health Sciences Center
    affiliation-url: https://ouhsc.edu/bbmc/
    email: wibeasley@hotmail.com
    orcid: 0000-0002-5613-5006
    attributes:
      corresponding: true

  - name: A Jerrod Anzalone
    affiliation: University of Nebraska Medical Center
    affiliation-url: https://gpctr.unmc.edu/
    email: alfred.anzalone@unmc.edu
    orcid: 0000-0002-3212-7845

  - name: Sharon Patrick
    affiliation: West Virginia Clinical and Translational Science Institute
    affiliation-url: https://www.wvctsi.org/
    email: patricks@hsc.wvu.edu
    orcid: 0000-0001-6535-2013

  - name: Shawn O'Neil
    affiliation: University of Colorado Anschutz
    affiliation-url: https://oneilsh.github.io/
    email: shawn@tislab.org
    orcid: 0000-0001-6220-7080

# reference-location: margin


csl: ../assets/csl/apa-7e.csl

---

# A Research Story {#sec-story}

**Chapter Leads**: Will Beasley, Jerrod Anzalone

:::{.callout-note}
This chapter is being written.
We hope to complete this chapter during May 2023.
:::

Now that we have introduced N3C and described its motivation and importance, we'll walk through the life cycle of an example project from onboarding to publishing.
This path typically takes at least 6 months and 6 collaborators.
It isn't easy to do yourself, but fortunately N3C has attracted a large and diverse set of researchers.
Coupled with a large and diverse set of robust patient records, completing a research project within a year is possible.

![Path of a typical N3C project.](images/story/fig-story-010-intro-to-story.png){#fig-story-010-intro-to-story fig-alt="Path of a typical N3C project"}

Suppose you are starting a project by yourself.
In that case, the N3C ecosystem of researchers and resources is at your fingertips.
You'll likely be able to recruit collaborators with complementary skills (in addition to N3C-wide resources such as [instructional material](support.md) and [office hours](support.md#sec-support-office)).
If you would like to join an existing project,
there are [domain teams](onboarding.md#sec-onboarding-dt) and ongoing projects that likely will fit your interests and benefit from your abilities.
@fig-story-010-intro-to-story provides a high-level overview of the path of a typical N3C project from clinical question to research product.

Electronic Health Record (EHR) research has become an increasingly important tool to evaluate real-world evidence (RWE) to understand insights into treatment effectiveness,
the impact of healthcare interventions, and our understanding of rare diseases.
EHRs provide access to large, diverse patient populations and longitudinal data that allows observations of health changes over time or in cross-section.
The strength of the EHR is that it reflects real-world care and is often a better representation of clinical care than the controlled settings of a traditional clinical trial.
However, with this comes challenges of interpreting differences in care delivery, data standards, and merging expertise from clinical subject matter experts, clinical informaticists, biostatisticians and epidemiologists, medical terminologists, and other experts as healthcare data is linked with other health assets to move toward a more comprehensive representation of a patient's lived experience relative their health outcomes.

:::{.callout-note icon=false}

## Voice of Narrator

Our story begins in your own piece of heaven: your office.
As a researcher of scurvy, you have wondered, "do patients receiving the newest medications have more favorable COVID-19 outcomes than patients receiving the previous generation?"
Given that scurvy is a rare disease with no opportunities for industry funding, you decide to use observational data from the EHR.
You expect a modest improvement based on the medications' relationships with other diseases.
But many patients are required to detect a modest effect size, and your local institution has a small population.
Given the disease's low prevalence, no single US-based institution likely has a sufficient sample size to answer your research question.

Yesterday you attended a local N3C presentation and became interested because it likely has enough qualifying scurvy patients to detect even small signals.
Your mind wanders, and you begin to daydream of additional hypotheses.
*Does the relationship attenuate as you move inland?*
You realize that a massive national dataset can not only better address your existing question, but it could also allow you to ask newer and more nuanced questions.
*Is the relationship more pronounced in other racial/ethnic groups?*
Your thoughts race into the night, a never-ending stream of possibilities.
:::

## Onboarding {#sec-story-onboarding}

As is typical for access to patient data outside your own institution, institutional participation in N3C requires legal agreements.
The initial time investment is higher for an N3C investigation compared to most, but project-specific work tends to go faster.
System access generally requires your institution to sign a Data Use Agreement with N3C,
and even with strong institutional support this can takes several months in legal and administrative channels.^[On the other hand,
hundreds of institutions have already done so;
check the list at <https://covid.cd2h.org/duas>.
This process is described in @sec-onboarding-enclave-access.]

Yet after clearing that first (tall) hurdle for your site, data access for each specific project takes only a week or two to be processed by the N3C Data Access Committee.
That's a remarkably short time considering the scale of available data.
It's likely quicker than initiating a project based on a single EHR from your site, and much quicker than accessing EHRs from 70+ sites individually.

:::{.callout-note icon=false}

## Voice of Narrator

The next afternoon you are chatting with your institution's navigator.^[
This "navigator" role may be called something differently at your institution;
the roles are defined below in @sec-story-team.  If your institution doesn't support this position, we suggest starting with the [N3C Office Hours](support.md#sec-support-office) or other avenues of [support](support.md).]
She organized the local N3C presentation and invited any interested attendees to contact her.
:::

::: {.callout-tip appearance="simple" icon=true}
Hover over a footnote to see the popup, without jumping to the bottom of the page.
:::

* **Navigator**:
  I'm glad you think the N3C might help your research.
  As I wrote in this morning's email, the agreement between the university and the NIH was established last year, so don't worry about that.^[Read about the institutional-level DUA in @sec-onboarding.]
  There are two remaining steps.
  First, complete your personal paperwork.^[See @sec-onboarding.]
  Second, submit a DUR tailored to your hypotheses.^[Project-level paperwork is discussed in @sec-onboarding.]

* **Investigator**:
  Remind me.  What is a [DUR](access.md#sec-access-dur)?

* **N**:
  A *D*ata *U*se *R*equest describes your upcoming project.
  Once an NIH committee approves your proposal, your project's code and data are protected in an associated workspace allotted on the NIH cloud.^[The NIH "Enclave" is detailed in @sec-tools.]
  Everyone on your project shares this dedicated workspace.
  Once you've submitted it, your collaborators can request to join your workspace by signing a copy of your DUR in the Enclave as well.^[DURs are the topic of @sec-access.]

* **I**:
  Umm, I think I got it.

* **N**:
  It will make sense once you get it into it.
  Skim the example DUR proposals I'm sending now.
  Then start filling out this online form.
  Get as far as you can, and then I'll help with the rest.
  If there's something I don't know, I'll ask a friend.
  The DUR application process will take about an hour.
  Then the proposal will likely be approved within a week or two.
  In the meantime, we can talk about potential collaborators.

* **I**:
  Is there anything else I need to know?

* **N**:
  The only other consideration at this point is whether your want your study to use
  Level 2 or Level 3 data.
  [Level 2](access.md#sec-access-request-l2) data is fully de-identified,
  meaning all the dates are shifted within &plusmn;180 days.
  Also, all location identifiers are obfuscated to prevent reidentification,
  so you won't have access to 5-digit ZIP Codes or other granular location measures.
  If you need either of those, you have to submit [Level 3](access.md#sec-access-request-l3) data,
  which is a limited data set containing these data elements.
  Some institutions requires an IRB protocol to submit a Level 3 DUR, so keep that in mind.
  Our institutional IRB has provided a letter covering most Level 3 DURs in N3C, so I can provide that to you.

* **I**:
  Ok, that's very helpful.
  I may need real dates as I anticipate differences in treatment deliveries based on real-world availability.
  Am I stuck with Level 2 data if I start there?

* **N**:
  No.
  If needed, you can request a workspace to be updated from Level 2 to Level 3 and receive IRB approval.

* **I**:
  That's great.
  I think we'll start with Level 2 and go from there.
  I'll work on the research protocol.

After some thought, the investigator develops a research protocol and
submits a DUR, shown in @fig-story-020-dur.

![Submitted Data Use Request.](images/story/fig-story-020-dur.png){#fig-story-020-dur fig-alt="Submitted Data Use Request"}

## Team building & collaborating {#sec-story-team}

:::{.callout-note icon=false}

## Voice of Narrator

The next step is to build a team to leverage retrospective medical records.
Like most contemporary research teams, heterogenous skills are important.
You follow some advice and assemble the following team.
:::

1. a **navigator** who has learned the administrative and IRB requirements and can facilitate the investigation,
1. a **subject matter expert** (SME) who has clinical experience with the disease of interest and can inform decisions with EHR variables,
1. a **statistician or data scientist** who understands the limitations of observational collection and can model retrospective data,
1. a **logic liaison or informaticist** who understands the challenges of EHRs and can extract and transform information (also known as a data engineer),
1. a **data liaison** who has expertise in medical terminology to help develop concept sets or identify previously validated concept sets, and
1. a **principal investigator** who knows the literature and can testable hypotheses and write the manuscript.

@fig-story-030-team-formation depicts these roles.  Depending on the investigation and the personnel, sometimes one person can serve multiple roles.

![Typical N3C Team Composition.](images/story/fig-story-030-team-formation.png){#fig-story-030-team-formation fig-alt="Typical N3C Team Composition"}

N3C teams have some differences from conventional research teams at single sites.
Some trends we have noticed are:

1. Most N3C teams have researchers from multiple institutions.
  In the experience of the authors and editors, this encourages more diverse opinions and more willingness to express constructive criticism.
  Researchers from a single institution/lab are sometimes more reluctant to generate contrary views.

1. The role of the navigator is often the most important member of a successful team.
  Your local investigations are likely guided by someone with years of experience with institutional safeguards and the personnel who can help when something stalls.
  N3C is bigger and younger than your site's EHR research team, so an N3C project will benefit when guided by a bright, patient, and persistent navigator.

If your team needs someone, consider asking a relevant [domain team](onboarding.md#sec-onboarding-dt) for help identifying and approaching potential collaborators.
Note that community-wide data and logic liaisons are available for consultation during regular office hours.

## Research Team's First Meeting

:::{.callout-note icon=false}

## Voice of Narrator

The team is assembled after a few weeks.
The first discussion is usually a variation of the following exchange, with the goal to move toward completion of a research protocol.
:::

* **Investigator**:
  Welcome everyone.
  We'd like to know if Drug A or Drug B is associated with better outcomes.
* **Statistician**:
  No problem.
  I can longitudinally model the type and amount of each medication received by each patient, relative to their intake date.
* **Logic Liaison**:
  Hmmm.
  I'm happy to produce a dataset with the `dose` and `frequency` columns, but you may not find it useful.^[
  <!-- Read about the OMOP Standard Tables in @sec-understanding,
  specifically the medications are in the [`drug_exposure`](https://ohdsi.github.io/CommonDataModel/cdm60.html#DRUG_EXPOSURE) table. -->
  OMOP tables are designed to represent data from many sources,
  but typically they need to be transformed before they are analyzed with conventional statistical software.
  ]
  Those two columns are sparsely populated and they look inconsistent across sites.^[Conformance is a topic in @sec-cycle.]
* **I**:
  Bummer.
  Then what's realistic or feasible?
* **Subject Matter Expert**:
  Maybe this simplifies the picture...
  In my clinical experience, a patient rarely switches between Drugs A & B.
  Based on the initial presentation, their provider will pick A *or* B, and complete the regimen unless there's an adverse event.
* **St**:
  In that case, should my initial model have three levels for treatment: A, B, and A+B?
* **I**:
  Probably.
  In the N3C database, can someone tell me how many patients get both during the same visit?
* **LL**:
  I'm already logged into the Enclave^[See @sec-access for accessing the N3C Enclave.].
  Give me 2 minutes to add this drug to our templated fact tables^[
  See @sec-understanding-sets-library-published
  and @sec-support-liaisons-logic
  ] which show same day events and also summarize events at the patient level.^[Read about SQL, Python, and R transforms in Code Workbooks in @sec-tools.]
* **I**:
  Oh my goodness, is that your cat?
  What a cutie!^[There is a brief discussion of SME's cat.]
* **LL** *after a few minutes*:
  Ok, I got it.  [Unmutes himself.]
  Ok, I got it.
  40% of patients are Drug A only, 52% are Drug B only, while 8% have at least one administration of both Drug A & B in the same visit.
* **SME**:
  Weird.
  8% is a lot more than I expected.
  I was thinking around 1%.
* **LL**:
  Hmm, let me check.
  Give me another minute.^[There is a brief discussion of S's daughter strutting in the background wearing a cowboy hat and waiving a fairy wand.]
* **LL** *after a few minutes*:
  I see what you mean.
  It looks like the bulk of the combo patients were admitted in the spring of 2020.
  After Jan 2021, only 3% of patients have both Drug A & B.
* **St**:
  I was already planning to model the phase of the pandemic.
  I'll test if there's a significant interaction between time and treatment.
* **I**:
  I like that as a starting point.
  Regarding the question about dose and frequency...
  For now let's assume the providers were following the current dosing guidelines.
  Therefore the `dose` and `frequency` variables can be dropped from the analyses.
* **St**:
  Phew.
  I didn't want to admit this.
  But I skimmed the dosing guidelines you emailed yesterday.
  It looked complicated.
  I wasn't sure if I could appropriately incorporate those variables in the model.
* **I**:
  Well, that's everything I wanted to cover today.
  See you in two weeks.
  Wait.
  I can't believe I forgot.
  Sorry -our Navigator is sick this week and I'm almost worthless in her absence.
  Is everyone still on the call?  For our secondary hypothesis, we want everything to connect  to a patient's diagnoses.  ...before, during, and after their covid hospitalization.
* **LL**:
  Bad news.
  This is kinda like the `dose` and `frequency` situation a few minutes ago.
  The structure of the [OMOP diagnosis table](https://ohdsi.github.io/CommonDataModel/cdm60.html#CONDITION_OCCURRENCE)
  theoretically can connect a patient's diagnoses across different locations.
  But the quality of the historical records really depends on the site.
  Some places like Rhode Island leverage their state's HIE^[An [HIE](https://www.healthit.gov/topic/health-it-and-health-information-exchange-basics/health-information-exchange)
  is a health information exchange.] to populate their N3C dataset.
  However other places are not as well connected.
  If a patient doesn't have diagnosis records, it's tough to determine if they are healthy,
  or if their primary care provider uses a siloed EHR.^[The benefits and caveats of real-world data are a theme throughout the book,
  particularly in the best practices discussed in @sec-practices.]
* **I**:
  Ugh.
  Good point.
* **LL**:
  But I've got good news.
  All the N3C contributors comprehensively capture all conditions diagnosed *during* the visit.
  Furthermore the diagnosis codes are standardized really well across sites.
  That's because most providers enter ICD codes into the EHR,
  which eventually can be cleanly mapped to OMOP's standard concepts.^[Authoring and using concept sets are described in @sec-understanding.
  Mapping an ICD to SNOMED diagnosis code is an example of mapping a "non-standard" to a "standard" concept, discussed in @sec-understanding.]
* **I**:
  Well, that's fine for this paper.
  Maybe our next manuscript will follow up with N3C's death records.^[Mortality records are discussed in @sec-understanding-pprl-mortality.]
* **SME**:
  Sorry everybody, I have clinic this week, and they're calling me.
  I need to drop.^[Everyone says goodbye to the cat.]
* **St**:
  Can I go back and ask a question about medications?  I see that Drug A has 15 different brand names.
  I don't recognize half of them.
  How should I classify them?
* **LL**:
  It's actually worse than that.
  Sorry I'm a downer today.
  Can you see my screen?  Drug A has 15 brand names and 200 different...^[
  The conversation get really technical.  More technical than the editors want for this chapter.
  ]
  <!--
  RxNorm codes; each package is uniquely identified by the NIH's NLM.
  SME and I started on a concept set Thursday.
  We're operationalizing the drug classes by their [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/docs/appendix5.html) ingredient.
  There are five ingredients that are conceptualized as Drug A.
  A friend showed me how she used the OMOP tables in a different project.^[The [`concept_relationship`](https://ohdsi.github.io/CommonDataModel/cdm60.html#CONCEPT_RELATIONSHIP)
  table is discussed with the OMOP concept hierarchy in @sec-understanding.]
  I'll roll up the meds into the patient-level dataset.
  It will have one integer for the number of medication records tied to a Drug A ingredient and another integer for Drug B records. -->
  So long story short, you'll probably want to transform the two counts into two booleans.
* **St**:
  Ok.  Thanks for simplifying the dataset for me.

## Protocol, variables, & definitions

:::{.callout-note icon=false}

## Voice of Narrator

Developing a research protocol is both familiar and vague in the context of EHR studies,
even when researchers have several years of graduate-level courses and real-world experience.
Tradeoffs are inevitable when selecting variables,
and an investigator's first choice is not always available.

:::

An investigation can realistically use only a fraction of the terabytes of information in an EHR.
The research team must identify the relevant variables among the qualifying patients
to produce a coherent dataset tailored to their hypotheses.

While there are different approaches to developing a Research Protocol, the general steps involved include:

1. Define the research question:
  The first step is to clearly define the research question and the patient population of interest.
  This will guide the selection of relevant clinical concepts and data sources.

1. Determine the study design:
  The research team should choose an appropriate study design, such as a cohort study or case-control study,
  and determine the inclusion and exclusion criteria for the patient population.

1. Develop the analytic plan:
  The research team should prospectively specify the statistical methods to be used to analyze the data,
  including any adjustments for confounding variables and any sensitivity analyses.

1. Document the study protocol:
  The research team should document a detailed study protocol that includes all of the above information,
  as well as any other relevant information,
  such as the ethical and regulatory considerations, data privacy and security measures, and data sharing agreements.

The Enclave's Protocol Pad supports the development and documentation of detailed study protocols.^[
@sec-tools-apps-protocol describes the tool
and @sec-practices describes the best practices.
]

## OMOP Tools

:::{.callout-note icon=false}

## Voice of Narrator

After you have creating a research protocol,
you turn to OMOP and N3C tools to define the variables.

:::

The [Observational Health Data Sciences and Informatics (OHDSI)](https://www.ohdsi.org/)
Observational Health Data Sciences and Informatics (OHDSI) program maintains the Observational Medical Outcomes Partnership (OMOP) common data model (CDM).
OMOP was funded in 2008 by the US Food and Drug Administration, primarily for adverse drug events surveillance, but it has since expanded to become the de-facto global research CDM.
Detecting a small signal requires a large datasets --larger than any single health care database [@ohdsi_2019, Chapter 1].
Given its ubiquity and active research community, OMOP is well suited for N3C.
OMOP has extensive tooling to support researchers,
including two that directly support the curation of concept sets from the OHDSI program and one that is specific to N3C:

1. [Atlas](https://github.com/OHDSI/Atlas/wiki) provides a user-friendly interface for querying and analyzing data in the OMOP CDM.
  In the context of N3C, it supports browsing medical terminology and supports the development of concept sets.

1. [Athena](https://athena.ohdsi.org/) is a centralized repository of standardized clinical vocabularies.

1. The [N3C Concept Set Browser](@sec-tools) is an N3C specific tool that allows you to explore and modify existing concept sets as well as create new concept sets to fit your exact study needs.

Concept sets, described in detail in @sec-understanding and @sec-tools, are the basic building blocks of an analytic dataset.
The contain lists of medical codes, usually restricted to very specific definition or computable phenotype.
In N3C, they are used to identify cohorts or exposures to answer a research question.
They point to standardized vocabularies and clinically organized domains in the OMOP CDM (e.g., drug, condition, measurement).

In general, the overall process involved in developing concepts is as follows:

1. Define the research question: The first step is for the research team to clearly define the research question and population of interest, which will guide the selection of relevant clinical concepts.
1. Explore the data: Using Atlas or the N3C Concept Set Browser, the team member filling as the data liaison will explore the data available or existing concept sets to identify relevant clinical concepts.
1. Refine the concept set: The data liaison works with the SME to refine the concept set, which is usually an iterative process, to include clinically relevant and exclude clinically irrelevant concepts.
1. Validate the concept set: Once the concept set has been defined, the SME and logic liaison validate the concept set and publish it in the N3C Concept Set Browser, which allows for reuse across the N3C community.

:::{.callout-note icon=false}

## Voice of Narrator

After determining the need for a concept set defining anemia, which is a common symptom of scurvy, the subject matter expert and data liaison meet to refine the concept set.
:::

* **Data Liaison**:
  Good morning! I've started digging into existing concept sets for anemia and found one potential option.
* **Subject Matter Expert**:
  Good morning! That's great.
  Let's take a look at it.
* **DL** *pulls up concept set for anemia*:
  This is one that's out there.
  It uses the parent SNOMED CT Code [271737000](https://athena.ohdsi.org/search-terms/terms/439777).
* **SME**:
  Hmm...this isn't quite right.
  We need anemia caused by blood loss.
  A lot of these are unrelated.
* **DL**:
  Gotcha.
  Let's take a look at the hierarchy and see if we can refine it.
  We can look at the descendants and go from there.
* *Three hours later*
* **DL**:
  Ok, great.
  I think we have a working example.
  I'm going to extract all of these into a spreadsheet.
  Please go through this one more time and then I'll share with the group to review.

## Creating an analysis-ready dataset

:::{.callout-note icon=false}

## Voice of Narrator

Once the project team has outlined the study protocol, key definitions, and timing of study elements, the next phase is the curation of a dataset for analysis.
This is typically within the purview of the team informaticist or logic liaison.
Let's take a peak into the process...
:::

After clarifying all the data elements and study protocol, the next step is to curate an an analytic dataset.
Depending on the study design, this can be organized in multiple ways.
In general, analytic datasets are organized at either the person or encounter level.
This means that you'll have a single analytic dataset that contains one row with facts about either an individual patient or an individual encounter.
This topic is covered in greater detail in the [Tools](tools.md) and [Best Practices](practices.md) chapters.

Using the previously defined protocol, the informaticist will use the [concept set browser]
to identify or create concept sets of relevance to the study and begin to pull together the analytic dataset in a [code workbook](tools.md#sec-tools-apps-workbook)
or [code repository](tools.md#sec-tools-apps-repo) in the N3C Enclave.
This will be a time-intensive process that, once completed, will result in a dataset that is ready for analysis, which can be handed off to the team's statistician for analysis.
N3C Logic Liaison templates are available to help build these datasets more quickly using defined pipelines where the custom concept sets can quickly be added as inputs.
They also provide templates to assess the quality of the derived dataset which can provide insights into data density and completeness and help support decisions about dropping certain sites for the analysis (for example, if they appear to be systematically missing key variables).

<div style="overflow-x:auto;">

| Age | Sex | Race Ethnicity                         | Quarter of COVID dx  | Smoking Status                   | Scurvy pre-COVID | Med A | Med B | Diabetes pre-COVID | COPD pre-COVID | Liver Disease pre-COVID | Cancer pre-COVID | Renal Disease pre-COVID | COVID Hospitalization | ECMO IMV | Time to ECMO IMV | Death | Time to Death |
| --- | --- | :------------------------------------- | :------------------- | :------------------------------- | :--------------: | :---: | :---: | :----------------: | :------------: | :---------------------: | :--------------: | :---------------------: | :-------------------: | :------: | :--------------: | :---: | ------------: |
| 27  | M   | Non-Hispanic White                     | 2022<br>Q2           | Current or Former Smoker         | 0                | 0     | 0     | 0                  | 1              | 0                       | 0                | 0                       | 1                     | 0        | 28               | 0     | 28            |
| 75  | F   | Hispanic or Latinx                     | 2021<br>Q1           | No Documented History of Smoking | 0                | 0     | 0     | 0                  | 0              | 0                       | 1                | 0                       | 0                     | 0        | 28               | 0     | 28            |
| 54  | M   | Non-Hispanic Black or African American | 2020<br>Q4           | No Documented History of Smoking | 1                | 1     | 0     | 1                  | 0              | 0                       | 1                | 0                       | 1                     | 0        | 1                | 1     | 1             |
| 34  | F   | Non-Hispanic White                     | 2023<br>Q1           | Current or Former Smoker         | 1                | 0     | 1     | 1                  | 0              | 1                       | 0                | 0                       | 1                     | 1        | 3                | 1     | 5             |
| …   | …   | …                                      | …                    | …                                | …                | …     | …     | …                  | …              | …                       | …                | …                       | …                     | …        | …                | …     | …             |

: Scurvy Analytic Dataset {#tbl-story-analytic}
</div>

## Analyses

:::{.callout-note icon=false}

## Voice of Narrator

Once the analytic dataset is finalized, the handoff between the informaticist and statistician takes place.
This often requires a discussion or ongoing dialogue to understand the data structure and definitions.
:::

* **Navigator**:
  Welcome everyone.
  Today we'd like to review the analytic dataset and next steps in moving the analysis forward.
* **Informaticist**:
  Yep.
  I've made a new code workbook in your folder in the project workspace.
  Can you pull it up and we can take a look?
* **Statistician**:
  Sure.
  Did you send me the dataset? I don't remember seeing an email.
* **N**:
  Remember, everything has to be done within the secure N3C platform.
  So you won't be doing anything on your local machine.
  It all has to be done within the platform.
  Do you know how to get to the project workspace?
* **S**:
  ...remind me.
* *A few minutes later after a refresher.*
* **S**:
  Ok, great.
  I think I get it.
  So it's not that different from using R in RStudio as long as I follow the documentation you sent me.
  I think I can figure that out.
  What happens when I want to share results with the rest of the team? Can I send them out?
* **N**:
  You can add them to a report and share them within the N3C Enclave to those who have access to our project workspace.
  If you want to share results outside the platform, you can request any summary results, model output, or plots using the download review process.
  N3C leadership reviews any results before they can be extracted from the Enclave to ensure compliance with the N3C privacy and security expectations.
* **S**:
  Gotcha.
  I'll reach out if I have any questions once I get to that point in the process.
  Thanks!

From here, the statistician can work directly in N3C using R or Python for data analysis.
After some work figuring out the platform, the statistician has some simple summary statistics to add to a report.
Within a code workbook, they develop the following code and output to add to a report.

```r
descriptive_statistics <- function(analytic_dataset) {
  library(gtsummary)
  library(dplyr)

  patient_characteristics <-
    analytic_dataset %>%
    dplyr::select(
      Scurvy_Indicator_Before_COVID,
      Age,
      Race_Ethnicity,
      Medication_A,
      Medication_B,
    ) %>%
    gtsummary::tbl_summary(
      by = Scurvy_Indicator_Before_COVID
    )

  table1 <- patient_characteristics <- as_tibble(table1, col_labels = FALSE)

  return(table1)
}
```

Which produces the following @tbl-story-demographics.

| Characteristic                             | No History&nbsp;of&nbsp;Scurvy | History&nbsp;of&nbsp;Scurvy |
| :----------------------------------------- | ------------------: | ------------------: |
| Patient Count                              | 19,871              | 2,199               |
| Age, Median<br>(IQR)                       | 50<br>(25,&nbsp;75) | 51<br>(27,&nbsp;75) |
| Race/Ethnicity                             | NA                  | NA                  |
| Non-Hispanic<br>White                      | 7,834<br>(39%)      | 883<br>(40%)        |
| Non-Hispanic<br>Black or African American  | 3,970<br>(20%)      | 431<br>(20%)        |
| Hispanic or Latinx                         | 3,986<br>(20%)      | 430<br>(20%)        |
| Missing/Other                              | 4,081<br>(21%)      | 455<br>(21%)        |
| Medication A                               | 3,017<br>(15%)      | 318<br>(14%)        |
| Medication B                               | 1,661<br>(8%)       | 173<br>(8%)         |

: Characteristics of Patients with and without Scurvy {#tbl-story-demographics}

<!--,<br>January 2020 - December 2022-->

After repeating this for the remaining analyses for the project, the statistician creates a report and requests it be reviewed by the [N3C Download Review Committee](publishing.md)

* **Statistician**:
  Good afternoon! I just received notification from N3C that my download review request was approved.
  What happens now?
* **Navigator**:
  That's great! Now that it's been approved, you can go into the Download Review Dashboard and there's an area where you can safely download the results.
  The review comes with a [DRR ID](publishing.md#sec-publishing-tech-process-download), which is required to download the associated results.
* **S**:
  Ok.
  And then I can send it out to the rest of the team?
* **N**:
  Yep! Once it's been reviewed, you can share it with the rest of the team outside of the Enclave.
* **S**:
  Great.
  Thank you! I'll set up a time to review the results with the team next week.

## Draft paper, pub committee

:::{.callout-note icon=false}

## Voice of Narrator

Nearing the trail head...
:::

* **Investigator**:
  Thanks everyone for making this meeting.
  I hope you've had a chance to review the results that were circulated last week.
* **Subject Matter Expert**:
  They looked great.
  Very unexpected, but intriguing results.
  I was surprised that outcomes were so much better in those exposed Medication B than Medication A.
* *Team reviews the results in detail.
  Manuscript write-up divided amongst the study team.*
* **I**:
  Ok, so we should all know what the next steps are in terms of the write-up.
  Are there any other requirements from N3C before we can submit the paper to our target journal?
* **Navigator**:
  Good question.
  The manuscript draft has to be reviewed by the N3C Publication Committee.
  They meet weekly and will review the drat to make sure it's compliant with N3C policies and adheres to the original research question proposed by us.
* **I**:
  Ok, that makes sense.
  How long does it usually take?
* **N**:
  In my experience, it's a pretty quick turnaround.
  Usually 1-2 weeks unless there are serious issues with the draft.
  They are primarily concerned about compliance with N3C policies, such as not having small cell counts and having gone through the download review process.
  Since we did this, it should be a quick review.
* **I**:
  Awesome.
  I hope you'll be able to help us when we get to the step.
  Thank you!
* **N**:
  Of course.
  Let's plan on meeting after the draft is closer to being finished.
* **I**:
  Sounds great.
  See you all in two weeks!

At this point, the team divides up the remaining work and gets to writing.
After completing a draft that's almost ready to be submitted for publication, they submit their draft to the [N3C Publication Committee](publishing.md).
After a week, they hear back from the N3C Publication Committee.

### Sample Email from N3C Publication Committee
>
> Title: Approved to submit MSID:383.23 | Investigator | The Impact of Drug A and Drug B on Patient with Scurvy Post-Acute COVID-19
>
> Dear Investigator,
>
> The publication committee has reviewed and conditionally approved your manuscript for submission.
> The following must be addressed:
> Please add "on behalf of the N3C consortium" to the end of the author list with an asterisk that says consortial contributors are in the process of being documented.
>
> Sincerely, The N3C Publication Committee

::: {.callout-note appearance="simple"}

## Additional Chapter Details

This chapter was first published May 2023.
If you have suggested modifications or additions, please see [How to Contribute](../index.qmd#sec-welcome-contribute) on the book's initial page.
:::
