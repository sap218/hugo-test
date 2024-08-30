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

## References

[^thesis]: Pendleton, Samantha C. [Investigations into the patient voice: a multi-perspective analysis of inflammation](https://etheses.bham.ac.uk/id/eprint/13244/ "thesis"). Thesis. University of Birmingham, 2023.
[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
[^coid]: Pendleton, Samantha C., et al. "Combined Ontology for Inflammatory Diseases [COID](https://doi.org/10.5281/zenodo.5524650 "paper for inflammation project")." Zenodo (2021).
