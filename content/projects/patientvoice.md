---
title: "Patient Voice"
date: 2023-01-01
toc: true
categories: ['ontology','nlp','tf-idf','project','patient voice','phd','semantic similarity','sentiment']
---

# Investigations into the patient voice: a multi-perspective analysis of inflammation

This work is my PhD[^thesis], completed in 2023.

## Abstract

### Background

The patient is the expert of their medical journey and their experiences go largely unheard in clinical practice.
Understanding the patient is important as bridging gaps in the medical domain enhances clinical knowledge: benefiting patient care in addition to improving quality of life. 

My PhD presented challenges and solutions exploring quality of life pertaining to two inflammatory diseases, Uveitis and Inflammatory Bowel Disease (IBD), which are often undifferentiated.
My work explored these inflammatory conditions and the patient's voice through various methods, including sentiment analysis, semantic characterisations, and clustering.

Most notably, resources derived from this work is available, open-source, for secondary research use.

### Methods

With guidance from domain experts and a foundation derived from clinical consensus documents, I created the Ocular Immune-Mediated Inflammatory Diseases Ontology ([OcIMIDo]({{< ref "ocimido" >}} "ocular ontology project")).
OcIMIDo was enhanced with patient-preferred terms, curated from online forum conversations, using a semi-automated statistical approach - with application of sentiment analysis.

Semantic similarity was explored using a pre-existing embedding model derived from clinical letters to retrain with patient-generated forum conversations ([PatientINF]({{< ref "patientinf-coid" >}})).
Systematic comparison were conducted to compare the clinician and patient voice.

In a final experimental chapter, blood markers of IBD participants were clustered and mapped to questionnaire data relating to quality of life.

### Impact

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

## Thesis summary

Inflammation is the body's first response to threat, generally present in many cases, and has a complex relationship with a wide range of diseases.

### Chapter 1

Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions and in many cases life threatening.
Having good vision is important to our everyday lives - affecting our Quality of Life (QoL) - and these ocular IMIDs cause problems, such as pain or blurriness.
Not only is there an unmet need for capturing the patient voice and their perspective of ocular IMIDs, but these clinical terms also needed to be standardised.

We can understand the patient better when knowing the terms they are using. 
A resource of patient-preferred synonyms is online patient forum conversations; however these are inaccessible due to being unstructured.
Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text, yet current biomedical ontologies for uveitis are limited.

**Ontology**
: a domain of knowledge condensed into a machine-readable format. For example: domain = anatomy, concepts in the ontology includes: hand, arm, and relationship can be hand "part of" arm.

This chapter built an ontology for ocular IMIDs to standardise the clinical vocabulary and structure and expanded with patient-preferred synonyms.
To capture these patient synonyms, a statistical technique was applied to a forum for curation and enhancement of the ontology.
The ontology was then used for opinion mining on particular medical therapies, types of uveitis, symptoms, etc.

More information can be [read here]({{< ref "ocimido" >}} "ocular ontology project").

### Chapter 2

This chapter continued to investigate the differences between the terms clinicians and patients use.
The clinical experts and I noticed a large number of *surprising* terms that the patient used.
To better understand both the patient and clinician, semantic similarity was explored, encapsulated via vectorisation.

**Semantic similarity**
: measure of relatedness between two concepts. For example: bone fracture and broken bone are the same.

**Vectorisation**
: numerically representing text in an embedding model. For example: hello and hi may be numerically close.

I used an embedding model derived from clinical letters and retrained with patient forum conversations.
Both clinicians and patients cover a wide range of medical-related concepts and relatedness, such as chronic severe inflammatory conditions to less intense acute incidents.
My investigations included a combination of manual evaluation, clustering, and semantic analysis.

More information can be [read here]({{< ref "patientinf-coid" >}} "semantics project").

### Chapter 3

Inflammatory Bowel Disease (IBD) is characterised as a chronic, non-infectious, autoimmune, digestive, inflammatory disease.
Patients who have IBD learn to live with their disease - specifically to control their inflammation - via medical therapies, strict diets, or stop smoking and so their biomarkers may be stable due to the regulation of their disease.
To diagnose, there are rigorous investigations, however, very invasive and can take years.

For IBD, there is a need for identifying novel blood biomarkers (preferred by the patient) as many GPs only refer patients for further tests if there is an elevated C-reactive protein (CRP) or issues in a stool sample (uncomfortable for the patient). 
Furthemore, studies lack in bridging biomarkers for IBD and the patient QoL.

The data I have access to consists of hospital records for stratifying patients into groups for those at study enrollment: diagnosed and not-yet diagnosed.
My methods explored the world of Machine learning (ML) with application of numerous clustering techniques to reveal patterns in biomarkers and mapping questionnaire data.
The goal was being able to characterise and extract valuable information from clustering in hope a pattern with QoL emerged.

**Machine learning**
: finding complex patterns in data potentially to predict an outcome.

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
