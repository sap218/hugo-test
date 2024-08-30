---
title: "Patient Voice"
date: 2023-01-01
toc: true
categories: ['ontology','nlp','tf-idf','project','patient voice','phd','semantic similarity','sentiment']
---

# Investigations into the patient voice: a multi-perspective analysis of inflammation

This work is my PhD[^thesis], completed in 2023.

## Background

The patient is the expert of their medical journey and their experiences go largely unheard in clinical practice.
Understanding the patient is important as bridging gaps in the medical domain enhances clinical knowledge: benefiting patient care in addition to improving quality of life. 

My PhD presented challenges and solutions exploring quality of life pertaining to two inflammatory diseases, Uveitis and Inflammatory Bowel Disease (IBD), which are often undifferentiated.
My work explored these inflammatory conditions and the patient's voice through various methods, including sentiment analysis, semantic characterisations, and clustering.

Most notably, resources derived from this work is available, open-source, for secondary research use.

## Methods

With guidance from domain experts and a foundation derived from clinical consensus documents, I created the Ocular Immune-Mediated Inflammatory Diseases Ontology ([OcIMIDo]({{< ref "ocimido" >}} "ocular ontology project")).
OcIMIDo was enhanced with patient-preferred terms, curated from online forum conversations, using a semi-automated statistical approach - with application of sentiment analysis.

Semantic similarity was explored using a pre-existing embedding model derived from clinical letters to retrain with patient-generated forum conversations ([PatientINF]({{< ref "patientinf-coid" >}})).
Systematic comparison were conducted to compare the clinician and patient voice.

In a final experimental chapter, blood markers of IBD participants were clustered and mapped to questionnaire data relating to quality of life.

## Impact

OcIMIDo is the first of its kind in ophthalmology[^ocimido] and patient-preferred terms prove the patient voice provides meaningful research efforts.
Sentiment analysis highlighted insight into the role a forum plays for patients and carers.

Semantic similarity highlighted potential novel disease associations and the patient lexicon for terms relating to inflammation[^coid].
Experiments revealed frequent misspellings from clinicians; use of abbreviations from patients; and patient priorities.

Clusters unveiled insight into the presence of inflammatory stress and the relationship with happiness.

In summary, this work benefits the clinical domain.
We better understand the patient: the terms they are using, synonyms, and relation to biological markers.
Understanding the patient can improve the clinical-patient relationship, including communication standards and medical journey.
In future, this work can highlight extra investigations during the diagnosis process, treatment plans, and shortening intensive time hauls in clinical practice.

---

## PhD Chapter Summaries

Inflammation is the body's first response to threat, generally present in many cases, and has a complex relationship with a wide range of diseases.

### Chapter 1
Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions and in many cases life threatening.
Uveitis itself is one of the top causes of blindness and often undifferentiated: no identifiable cause.

Having good vision is important to our everyday lives and these ocular IMIDs cause problems, such as pain or blurriness.
These symptoms or complications can affect our Quality of Life (QoL).
Not only is there an unmet need for capturing the patient voice and their perspective of ocular IMIDs, but these clinical terms also needed to be standardised.

The patient voice provides insight into their medical journey: ranging from clinical tests, symptoms, side-effects, to treatments.
We can understand the patient better when we understand the terms they use and their emotional wellbeing. 

Sentiment analysis is essentially opinion mining - we can look at the emotions of particular medical therapies to better design treatment plans.
Sentiment analysis uses clinical terms to mine valuable results, however the task benefits with synonyms: additionally, patients may have their own vocabulary.

A resource of patient-preferred synonyms is online patient forum conversations; however these are inaccessible due to being unstructured.
Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text yet currently there are structural and terminology gaps.

**Ontology**
: a domain of knowledge condensed into a machine-readable format. For example: domain = anatomy, concepts in the ontology includes: hand, arm, and relationship can be hand "part of" arm.

This chapter built an ontology for ocular IMIDs to standardise the clinical vocabulary and structure, based on clinical experts and consensus documents.
To apply this ontology to forum conversations, it needed to be expanded with corresponding patient-preferred synonyms.

To capture these patient synonyms, a statistical technique for important terms was applied to the forum to curate, annotate, and then enhance the ontology.
This formally encodes and integrates patient-preferred terms to their formalised and standardised clinical terms within an ontology.
These terms and synonyms improved text mining and so a more fruitful sentiment analysis.

Capturing patient-preferred terms aids in understanding the patient voice: we can understand them better through vocabulary and sentiment.
A deeper knowledge of these and QoL can potentially lead to improved condition management and positive QoL interventions: bridging gaps in the clinical and patient domain.

### Chapter 2

This chapter continued to investigate the differences between the terms clinicians and patients use.
The clinical experts and I noticed a large number of *surprising* terms that the patient used.
In my research and literature review, previous work has found that patients mention things amongst themselves that they would not to clinicians or terms that the clinician is unfamiliar with.

To better understand the patient and clinician, semantic similarity is explored to map terms.
Semantic similarity can be encapsulated via vectorisation.

**Semantic similarity**
: measure of relatedness between two concepts. For example: bone fracture and broken bone are the same.

**Vectorisation**
: numerically representing text in an embedding model. For example: hello and hi may be numerically close.

However, there is an absence of embedding models available which captures patient-generated texts hindering secondary research use.
Some clinically relevant models are available and valuable for the clinical domain but not fully exploited and systematically compared to patient text.

Both clinical and patient text cover a wide range of medical-related concepts and relatedness, such as chronic severe inflammatory conditions to less intense acute incidents.
Three objectives can build upon a solution: 1) using a preexisting model derived from clinical text (it is difficult to access clinical records).
2) Train a model solely consisting patient-generated text. 3) Retraining the existing clinical model with the patient text.

These three will let us see semantics in 1) the clinician, 2) the patient, and 3) both semantically.
My investigations included a combination of manual evaluation, clustering, and semantic analysis.

### Chapter 3

Inflammatory Bowel Disease (IBD) is characterised as a chronic, non-infectious, autoimmune, digestive, inflammatory disease.
Patients who have IBD learn to live with their disease, specifically to control their inflammation.
There are numerous methods to manage their condition - including medical treatments, maintaining a strict diet, or stop smoking.
IBD can severely affect QoL and so takes a toll on the emotional wellbeing of the patient.

For these patients, their biomarkers may be stable due to the regulation of their disease.
For those who do not-yet have a diagnosis or having an episode, their intestinal inflammation may be active and so causing many symptoms.
To diagnose, there are rigorous investigations, however, very invasive and can take years.

One solution for better diagnostic methods is looking into blood tests, since they are preferred by the patient and less invasive.
For IBD, there is a need for identifying novel blood biomarkers as many GPs only refer patients for further tests if there is an elevated C-reactive protein (CRP) or issues in a stool sample (uncomfortable for the patient). 
Although studies have investigated biomarkers for IBD, or patient questionnaires, there lacks a bridge between the two, and so I use this chapter to dive into the biology realm to look at blood biomarkers and the relationship with a patient's emotional wellbeing.

The data I have access to has an enrolment date questionnaire for patients, blood measurements, and hospital records.
These hospital records have dates that can stratify patients into groups: diagnosed, and those who were not-yet diagnosed at enrolment.

My methods in this chapter explored the world of Machine learning (ML) I applied numerous clustering techniques to seek out patterns in the data.
I concluded the ML by conducting statistical analysis to observe cluster/group differences in relation to possible novel blood/QoL biomarkers: the overlaps.

**Machine learning**
: finding complex patterns in data potentially to predict an outcome.

The goal was being able to characterise and extract valuable information from clustering.
To see how blood markers and adjacent QoL markers interact but also direct improvements in the diagnosis time and diagnosis tests.

### Interesting results

+ Thesis has proven how invaluable the patient voice is.
+ Patient terms are used frequently and need to be considered in research, especially abbreviations or common misspellings.
+ Sentiment can show the role online forums play in a patient's emotional wellbeing and develop personalised therapy plans.
+ Semantics presented terms patients were using, revealing their priorities.
+ Furthermore, these terms were - in the opinion of the clinical experts - not medically relevant revealing important differences across domains.
+ Blood biomarkers had a relationship with QoL markers.
+ In those who had an abnormally high white blood cell count & CRP and unhappier, were diagnosed within 2 years on average.
+ Although we know second-hand smoking can increase your risk of IBD (Crohn's), results highlighted a relationship that maternal smoking (during pregnancy) had an impact.
+ These findings can indicate emotional changes and should be pursued.
+ Finally, my work allowed for scientific resources for secondary research use: the development of two ontologies expanded with patient-preferred terms, and a vectorisation embedding model with clinician and patient-generated texts.

A patient's experience with their chronic, inflammatory disease is complex.
This work has shown that the patient's voice, being qualitative or quantitative, in ontologies; or combined with novel biomarkers, can be investigated for improved patient outcomes and quality of life.

**The patient is the expert of their experience and their voice is indispensable to science.**

## References

[^thesis]: Pendleton, Samantha C. [Investigations into the patient voice: a multi-perspective analysis of inflammation](https://etheses.bham.ac.uk/id/eprint/13244/ "thesis"). Thesis. University of Birmingham, 2023.
[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
[^coid]: Pendleton, Samantha C., et al. "Combined Ontology for Inflammatory Diseases [COID](https://doi.org/10.5281/zenodo.5524650 "paper for inflammation project")." Zenodo (2021).
