A Research Story {#story}
=========================

> 50,000-foot view of a research project, from onboarding to publishing

Now that we have introduced N3C and described its motivation and importance, we'll walk through the lifecycle of an example project from onboarding to publishing.  This path typically takes at least 6 months and 6 collaborators.  It is difficult to do by yourself, but fortunately the N3C has attracted a large and diverse set of researchers.  Coupled with a large and diverse set of patients, it is possible to complete a research project within a year.

If you are starting a project by yourself, you'll likely be able to recruit collaborators with a complementary set of skills (in addition to the resources such as [instructional material]() and [office hours](https://covid.cd2h.org/support)).  If you would like to join an existing project, there are [domain teams](https://covid.cd2h.org/domain-teams) and ongoing projects that likely will fit your interests and benefit from your abilities.

Onboarding {#story-person}
----------------------------------------------

Before the first data point is viewed, three things should be established by you and your institution:

* {A person's paperwork.  Include ORCiD}
* {DUA coverage & An institution's paperwork.}
* {DUR & a project's paperwork.}

The startup costs are more expensive for an N3C investigation compared to most, but the incremental costs are cheaper.  Even with strong institutional support, the DUA will take several months in legal and administrative channels.  Yet after clearing that first (tall) hurdle for your site, each specific project takes only a few days to be processed by the N3C staff.  That's a remarkably short time for scale of available data.  It's likely quicker than initiating a project based on a single EMR from your site --much less EMRs from 70+ sites.

Team building & collaborating
----------------------------------------------

The next step is to build a team to leverage retrospective medical records.  Like most contemporary research teams, heterogenous skills are important.  Ideally a team has at least:

1. a navigator who has learned the administrative and IRB requirements and is able to facilitate the investigation,
1. a data engineer who understands the challenges of EMRs and is able to extract and transform information,
1. a statistician who understands the limitations of observational collection and is able to model retrospective data,
1. a subject matter expert who has clinical experience with the disease of interest and is able to inform decisions with EMR variables, and
1. a principal investigator who knows the literature and is able form testable hypotheses and write the manuscript.

N3C teams have some differences from conventional research teams at single sites.  Some trends we have noticed are:

* Most N3C teams have researchers from at least three institutions.  In the experience of the authors and editors, this encourages more diverse opinions and more willingness to express constructive criticism.  Researchers from a single institution/lab are sometimes are more reluctant to generate contrary views.

* The role of navigator is even more important.  Your local EMR investigations are likely guided by someone with years of experience with the institutional safeguards and the personnel who can help when something stalls.  N3C is bigger and younger than your site's EMR research team, so an N3C project will benefit when guided by a bright, patient, and persistent navigator.

If your team needs someone, consider asking a relevant [domain team](https://covid.cd2h.org/domain-teams) for helping identifying and approaching a potential collaborator.

Common Discussion at the Team's First Meeting
----------------------------------------------

Once the team is assembled, the first discussion is usually a variation of this exchange:

* *Investigator*: Overall, we'd like to know if Drug A or Drug B is associated with better outcomes.
* *Statistician*: No problem.  I can longitudinally model the type and amount of each medication received by each patient, relative to their intake.
* *Data Engineer*: Hmmm.  I'm happy to produce a dataset with the `dose` and `frequency` column, but you won't like it.  Those two columns are sparsely populated and they look inconsistent across sites.
* *I*: Bummer.  Then what's realistic or feasible?
* *Subject Matter Expert*: Maybe this will help simplify the picture...  In my clinical experience, patients rarely switch between Drugs A & B.  Based on the initial presentation, the providers will pick A *or* B, and not switch unless something rare and unexpected happens.
* *S*: In that case, my initial models will have three levels for treatment: A, B, and A+B.
* *I*: Among N3C patients, how frequently is someone given both during the same visit?
* *DE after a few minutes*: 40% of patients are Drug A only, 52% are Drug B only, and 8% have at least one administration of both Drug A & B in the same visit.
* *SME*: Weird. 8% is more than I expected.
* *DE after a few minutes*: I see what you mean.  It looks like the bulk of the combo patients were admitted in the spring of 2020. After Jan 2021, only 2% of patients have both Drug A & B.
* *S*: I was already planning to model the time period --maybe an interaction with treatment will be significant.
* *I*: I like that as a starting point.  Circling back to the question about dose and frequency...
* *SME*: I suggest we start simply?  Let's assume the providers were following the current dosing guidelines.  Therefore the `dose` and `frequency` variables can be dropped from the analyses.
* *S*: Phew.  I didn't want to admit it before but I read the dosing guidelines the SME emailed yesterday.  I wasn't sure if I could model it adequately.
* *I*: Ok, that's everything I wanted to cover today. See you in two weeks.  Wait.  I can't believe I forgot to mention this.  I want to see what other drugs the patients were taking before and after their initial hospitalization for covid.
* *DE*: Similar to before, I can include those rows in the dataset, but the inconsistent population may introduce more problems.  If their primary care uses a different EMR than the hospital, we won't know what's prescribed.
* *S*: Oh, I see that Drug A has 15 different brand names.  I don't recognize half of them.  How do I classify them
* *DE*: It's worse than that.  Drug A has 15 brand names, but 200 different RxNorm codes; each package is uniquely identified.  SME and I were working on a [concept set]() Thursday.  We were going to operationalize the drug classes by the [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/docs/appendix5.html) ingredient.  Their are five ingredients that are conceptualized as Drug A and three ingredients conceptualized as Drug B.  A friend showed me how she derived this with the OMOP [`concept_relationship`](https://ohdsi.github.io/CommonDataModel/cdm60.html#CONCEPT_RELATIONSHIP) table for a different project.  I'll have that simplified in the patient-level dataset I give you.  It will have a integer for the number of times they were given a medication with a Drug A ingredient and another integer for Drug B ingredients.
* *All together*: and knowing is half the battle.

Protocol, variables, & definitions
----------------------------------------------

This aspect of the scientific process is probably both the most familiar and most vague.  Most researchers have several years of graduate-level courses and real-world experience.

1. Tradeoffs are inevitable when selecting variables.  Rarely will an investigator's first choice be available.


1. Retrospective medical records are extracted from a larger dataset.  An investigation can use only a fraction of the terabytes in an EMR.  Many decisions are involve to include only the relevant variables among the qualifying patients.


{Mention CD2H's [Informatics Playbook](https://playbook.cd2h.org/en/latest/index.html)}

Creating an analysis-ready dataset
----------------------------------------------

{Conventional data engineer role.  Dataset is created with input from the analyst.}

Learning and using OMOP (e.g. concept sets)
----------------------------------------------

OMOP originated around 20qq to facilitate the detection of small but significant side effects from new pharmaceuticals.  Detecting a small signal requires a large datasets --larger than any single health care database [@ohdsi2019].  Since then, the foundation has supported many other research goals.  It is well-suited for N3C because:

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
