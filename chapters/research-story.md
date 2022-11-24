---
# reference-location: margin

abstract: 40,000-foot view of a research project, from onboarding to publishing

author:
  - name: William H Beasley
    affiliation: University of Oklahoma Health Sciences Center
    affiliation-url: https://ouhsc.edu/bbmc/
    email: wibeasley@hotmail.com
    orcid: 0000-0002-5613-5006
    attributes:
      corresponding: true

  - name: Alfred H Anzalone
    affiliation: University of Nebraska Medical Center
    affiliation-url: https://gpctr.unmc.edu/cores/biostatistics-epidemiology-research-design/
    email: alfred.anzalone@unmc.edu
    orcid: 0000-0002-3212-7845
---

# A Research Story {#sec-story}

**Additional Contributors**: Sharon Patrick, Shawn O'Neil<a href="https://orcid.org/0000-0001-6220-7080"><img alt="ORCID logo" src="https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png" width="16" height="16"/></a>

Now that we have introduced N3C and described its motivation and importance, we'll walk through the lifecycle of an example project from onboarding to publishing.  This path typically takes at least 6 months and 6 collaborators.  It is difficult to do by yourself, but fortunately the N3C has attracted a large and diverse set of researchers.  Coupled with a large and diverse set of patients, it is possible to complete a research project within a year.

If you are starting a project by yourself, you'll likely be able to recruit collaborators with a complementary set of skills (in addition to the resources such as [instructional material]() and [office hours](https://covid.cd2h.org/support)).  If you would like to join an existing project, there are [domain teams](https://covid.cd2h.org/domain-teams) and ongoing projects that likely will fit your interests and benefit from your abilities.

:::{.callout-note icon=false}
## Voice of Morgan Freeman

Our story begins in your office.  Your own piece of heaven.  As a researcher of scurvy, you have wondered, "do patients receiving the newest medications have more favorable covid outcomes than patients receiving the previous generation?".  Based on the meds' relationships with other diseases, you expect there is a modest improvement.  But in order to detect a modest effect size, many patients are required, and your local institution's EMR doesn't have enough meeting the inclusion criteria.  In fact, no single institution's EMR has enough.

Yesterday you attended a local N3C presentation and became interested because it likely has enough qualifying scurvy patients to detect even small signals.  Your mind wanders as you get a little greedy; additional hypotheses enter your daydream.  *Does the relationship attenuate as you move inland?*  You realize that a massive national dataset can not only better address your existing question, it could also allow you to ask newer and more nuanced questions.  *Is the relationship more pronounced in other racial/ethnic groups?*  The stream persists throughout the night.
:::

{Should we use 2nd person or 3rd person?}

Onboarding {#sec-story-onboarding}
----------------------------------------------

The startup costs are more expensive for an N3C investigation compared to most, but the incremental costs are cheaper.  Even with strong institutional support, the university's agreement with the NIH takes several months in legal and administrative channels.  Yet after clearing that first (tall) hurdle for your site, each specific project takes only a week or two to be processed by the N3C staff.  That's a remarkably short time considering the scale of available data.  It's likely quicker than initiating a project based on a single EMR from your site --much quicker than EMRs from 70+ sites.

:::{.callout-note icon=false}
## Voice of someone like Bill Kurtis, but without the connotation of murder

The next afternoon you are chatting with your institution's Navigator.^[This role may be called something differently at your Institution; the roles are defined below in @sec-story-team.]  She organized the local N3C presentation and invited any interested attendees to contact her.
:::

::: {.callout-tip appearance="simple" icon=true}
Hover over a footnote to see the popup, without jumping to the bottom of the page.
:::

* **Navigator**: I'm glad you think the N3C might help your research.  As I wrote in this morning's email, the agreement between the university and the NIH was established last year, so don't worry about that.^[Read about the institutional-level DUA in @sec-onboarding.]  There are two remaining steps.  First, complete your personal paperwork.^[See @sec-onboarding.]  Second, submit a DUR tailored to your hypotheses.^[Project-level paperwork are discussed in @sec-onboarding.]

* **Investigator**: Remind me what a DUR is?

* **N**: A *d*ata *u*se *r*equest describes your upcoming project.  Once a committee approves your proposal, your project's code and data are protected in this workspace allotted on the NIH cloud.^[The NIH "Enclave" is detailed in @sec-data-analysis.]  Everyone on your project uses this dedicated workspace too.  But they don't have to submit additional DURs --your grant them permission to join yours.^[DURs are the topic of @sec-data-analysis.]

* **I**: Umm, I think I got it.

* **N**: It will make sense once you get it into it.  Skim the example DUR proposals I'm sending now.  Then start filling out this online form.  Get as far as you can, and then I'll help with the rest.  If there's something I don't know, I'll ask a friend.  The DUR application process will take about an hour.  Then the proposal will likely be approved within a week or two.  In the meantime, we can talk about potential collaborators.


Team building & collaborating {#sec-story-team}
----------------------------------------------

The next step is to build a team to leverage retrospective medical records.  Like most contemporary research teams, heterogenous skills are important.  Ideally a team has at least:

1. a **navigator** who has learned the administrative and IRB requirements and is able to facilitate the investigation,
1. a **data engineer** who understands the challenges of EMRs and is able to extract and transform information,
1. a **statistician** who understands the limitations of observational collection and is able to model retrospective data,
1. a **subject matter expert** (SME) who has clinical experience with the disease of interest and is able to inform decisions with EMR variables, and
1. a **principal investigator** who knows the literature and is able form testable hypotheses and write the manuscript.

N3C teams have some differences from conventional research teams at single sites.  Some trends we have noticed are:

1. Most N3C teams have researchers from at least three institutions.  In the experience of the authors and editors, this encourages more diverse opinions and more willingness to express constructive criticism.  Researchers from a single institution/lab are sometimes are more reluctant to generate contrary views.

1. The role of navigator is even more important.  Your local EMR investigations are likely guided by someone with years of experience with the institutional safeguards and the personnel who can help when something stalls.  N3C is bigger and younger than your site's EMR research team, so an N3C project will benefit when guided by a bright, patient, and persistent navigator.

If your team needs someone, consider asking a relevant [domain team](https://covid.cd2h.org/domain-teams) for helping identifying and approaching a potential collaborator.


:::{.callout-note icon=false}
## Voice of Jamie Foxx

Recruiting your crew...
:::

Research Team's First Meeting
----------------------------------------------


:::{.callout-note icon=false}
## Voice of ...

Three weeks later...

Once the team is assembled, the first discussion is usually a variation of this exchange:
:::

* **Investigator**: Welcome everyone.  We'd like to know if Drug A or Drug B is associated with better outcomes.
* **Statistician**: No problem.  I can longitudinally model the type and amount of each medication received by each patient, relative to their intake date.
* **Data Engineer**: Hmmm.  I'm happy to produce a dataset with the `dose` and `frequency` columns^[Read about the OMOP Standard Tables in @sec-data-understanding, specifically the medications are in the [`drug_exposure`](https://ohdsi.github.io/CommonDataModel/cdm60.html#DRUG_EXPOSURE) table.], but you may not find it useful.  Those two columns are sparsely populated and they look inconsistent across sites.^[Conformance is a topic in @sec-lifecycle.]
* **I**: Bummer.  Then what's realistic or feasible?
* **Subject Matter Expert**: Maybe this simplifies the picture...  In my clinical experience, a patient rarely switches between Drugs A & B.  Based on the initial presentation, their provider will pick A *or* B, and complete the regimen unless there's an adverse event.
* **S**: In that case, should my initial model have three levels for treatment: A, B, and A+B?
* **I**: Probably.  In the N3C database, can someone tell me how many patients get both during the same visit?
* **DE**: I'm already logged into the Enclave^[See @sec-data-access for accessing the N3C Enclave.].  Give me 2 minutes to whip up something in SQL.^[Read about SQL, Python, and R transforms in Code Workbooks in @sec-data-analysis.]
* **I**: Oh my goodness, is that your cat?  What a cutie! ^[There is a brief discussion of SME's cat.]
* **DE** *after a few minutes*: Ok, I got it.  [Unmutes himself.]  Ok, I got it.  40% of patients are Drug A only, 52% are Drug B only, while 8% have at least one administration of both Drug A & B in the same visit.
* **SME**: Weird. 8% is a lot more than I expected.  I was thinking around 1%.
* **DE**: Hmm, let me check.  Give me another minute.^[There is a brief discussion of S's daughter strutting in the background wearing a cowboy hat and waiving a fairy wand.]
* **DE** *after a few minutes*: I see what you mean.  It looks like the bulk of the combo patients were admitted in the spring of 2020. After Jan 2021, only 3% of patients have both Drug A & B.
* **S**: I was already planning to model the phase of the pandemic.  I'll test if there's a significant interaction between time and treatment.
* **I**: I like that as a starting point.  Regarding the question about dose and frequency...
  For now let's assume the providers were following the current dosing guidelines.  Therefore the `dose` and `frequency` variables can be dropped from the analyses.
* **S**: Phew.  I didn't want to admit this.  But I skimmed the dosing guidelines you emailed yesterday.  It looked complicated.  I wasn't sure if I could appropriately incorporate those variables in the model.
* **I**: Well, that's everything I wanted to cover today.  See you in two weeks.  Wait.  I can't believe I forgot.  Sorry -our Navigator is sick this week and I'm almost worthless in her absence.  Is everyone still on the call?  For our secondary hypothesis, we want everything to connect  to a patient's diagnoses.  ...before, during, and after their covid hospitalization.
* **DE**: Bad news.  This is kinda like the `dose` and `frequency` situation a few minutes ago. The structure of the [OMOP diagnosis table](https://ohdsi.github.io/CommonDataModel/cdm60.html#CONDITION_OCCURRENCE) theoretically can connect a patient's diagnoses across different locations.  But the quality of the historical records really depends on the site.  Some places like Delaware leverage their state's HIE^[An [HIE](https://www.healthit.gov/topic/health-it-and-health-information-exchange-basics/health-information-exchange) is a health information exchange.] to populate their N3C dataset.  However other places are not as well connected.  If a patient doesn't have diagnosis records, it's tough to determine if they are healthy, or if their primary care provider uses a siloed EMR.^[The benefits and caveats of real-world data are a theme throughout the book, particularly in the best practices discussed in @sec-practices.]
* **I**: Ugh.  Good point.
* **DE**: But I've got good news.  All the N3C contributors comprehensively capture all conditions diagnosed *during* the visit.  Furthermore the diagnosis codes are standardized really well across sites.  That's because all the providers enter ICD codes into the EMR, which eventually can be cleanly mapped to OMOP's standard concepts.^[Authoring and using concept sets are described in @sec-data-analysis.  Mapping an ICD to SNOMED diagnosis code is an example of mapping a "non-standard" to a "standard" concept, discussed in @sec-data-understanding.]
* **I**: Well, that's fine for this paper.  Maybe our next manuscript will follow up with N3C's death records.^[TODO: is the book planning to have a section on the CMS & death records?]
* **SME**: Sorry everybody, I have clinic this week, and they're calling me.  I need to drop.^[Everyone says goodbye to the cat.]
* **S**: Can I go back and ask a question about medications?  I see that Drug A has 15 different brand names.  I don't recognize half of them.  How should I classify them?
* **DE**: It's actually worse than that.  Sorry I'm a downer today.  Can you see my screen?  Drug A has 15 brand names and 200 different RxNorm codes; each package is uniquely identified by the NIH's NLM.  SME and I started on a concept set Thursday.  We're operationalizing the drug classes by their [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/docs/appendix5.html) ingredient.  There are five ingredients that are conceptualized as Drug A.  A friend showed me how she used the OMOP tables in a different project.^[The [`concept_relationship`](https://ohdsi.github.io/CommonDataModel/cdm60.html#CONCEPT_RELATIONSHIP) table is discussed with the OMOP concept hierarchy in @sec-data-understanding.]  I'll roll up the meds into the patient-level dataset.  It will have one integer for the number of medication records tied to a Drug A ingredient and another integer for Drug B records.  You'll probably want to transform the two counts into two booleans.
* **S**: And if I change my mind and decide to use the counts, then at least I'll know.
* **Shoreleave**: and knowing is half the battle.

Protocol, variables, & definitions
----------------------------------------------

This aspect of the scientific process is probably both the most familiar and most vague.  Most researchers have several years of graduate-level courses and real-world experience.

1. Tradeoffs are inevitable when selecting variables.  Rarely will an investigator's first choice be available.

2. Retrospective medical records are extracted from a larger dataset.  An investigation can use only a fraction of the terabytes in an EMR.  Many decisions are involve to include only the relevant variables among the qualifying patients.


{Mention CD2H's [Informatics Playbook](https://playbook.cd2h.org/en/latest/index.html)}

[@cd2h1, Chapter 1]

Creating an analysis-ready dataset
----------------------------------------------

{Conventional data engineer role.  Dataset is created with input from the analyst.}

Learning and using OMOP (e.g. concept sets)
----------------------------------------------

OMOP originated in 2014 to facilitate the detection of small but significant side effects from new pharmaceuticals.  Detecting a small signal requires a large datasets --larger than any single health care database [@ohdsi2019, Chapter 1].  Since then, the foundation has supported many other research goals.  It is well-suited for N3C because:

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

:::{.callout-note icon=false}
## Voice of Sam Elliot

Nearing the trail head...
:::
