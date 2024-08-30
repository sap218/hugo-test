---
title: "PatientINF & COID"
date: 2022-04-20
toc: true
categories: ['ontology','nlp','tf-idf','patient voice','machine learning','semantic similarity','project']
---

# PatientINF & COID

Resources in this project are both are available open-source for secondary research use:

+ [PatientINF](https://github.com/sap218/PatientINF "patientinf github") is an embedding model.
+ [COID](https://github.com/sap218/coid/ "coid github") is the Combined Ontology for Inflammatory Diseases.

## Background

Semantic similarity builds upon the patient voice in understanding synonyms and the sort of terms patients are using.
Not only can semantics help to better undertand the patient, but also the clinician.
Patients may not use clinical terms (jargon) often and domain experts may be unfamiliar with patient-preferred terms.

This work was influenced by the [OcIMIDo]({{< ref "ocimido" >}} "ocular ontology project") project[^ocimido] in that some patient-preferred terms were to the surprise of the domain expert.

## Methodology

**PatientINF** is a novel `Word2Vec` embedding model, developed like so:

1. Using [ClinicalBERT](https://github.com/kexinhuang12345/clinicalBERT "clinicalbert github")[^clinicalbert] - a model derived from the the clinician's voice via clinical letters.
2. Retrained using data extracted from [Patient.info](https://patient.info/ "patient dot info website") online forum, specifically topics on inflammatory diseases.

Multiple tests were conducted to observe the impact of a clinician-generated and patient-generated "combined" model.
Tests included Wilcoxon (the change of vector space) and a Pearson correlation coefficient to test the embedding model similarities compared to a physician annotations.

**COID** was developed due to the need of an ontology aimed solely on inflammatory diseases. COID also covers anatomy, symptoms, and more.
COID also used similar statistical methods for synonym curation from Pendleton et al. (2021).
Futhermore, synonyms were also curated from PatientINF embedding model: looking at semantic similarity of terms of interest.

{{< figure src="/ontologies/COID-snip.PNG" width=400 caption="**Figure**: Graphical representation of COID. Each node is a class and each edge is a relationship." alt="coid visualised" >}}

## Impact

Semantic characterisations of the models revealed clinicians consisted of more frequent misspellings, whereas patients used more abbreviations.
Patient priorities were highlighted: showing how clinicians and patient similarites differ.
For example, diarrhea and stomach cramp for patients are more similar yet not so much in the clinical domain.

{{< figure src="/ontologies/cbpi_coid.png" width=500 caption="**Figure**: t-SNE of the released embedding model highlighing terms in COID. Each dot is a term and colours represent the category within COID." alt="embedding model visualised" >}}

## References

[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
[^clinicalbert]: Huang K, Altosaar J, Ranganath R. [Clinicalbert](https://arxiv.org/abs/1904.05342 "clinical bert manuscript"): Modeling clinical notes and predicting hospital readmission. arXiv preprint arXiv:1904.05342. 2019.
