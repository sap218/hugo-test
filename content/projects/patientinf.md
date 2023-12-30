---
title: "PatientINF"
date: 2022-04-20
categories: ['ontology','nlp','tf-idf','patient voice','machine learning','semantic similarity','project']
---

# PatientINF project: PatientFORUM embedding model & Combined Ontology for Inflammatory Diseases (COID)

Semantic similarity builds upon the patient voice in understanding the sort of terms patients are using.
Not only can semantics help us better undertand the patient, but also the clinician.

Patients may struggle with clinical terms (jargon) but domain experts may also be unfamiliar with the terms patients are using.
Highlighting gaps in communication and understanding.

## Resources for secondary research use
This projet presents two resources of novel data for seconday research use.

### PatientFORUM embedding model
I presented a novel `Word2Vec` embedding model, **PatientFORUM**, dervived from two specific generated text data:

1. the clinician's voice via [ClinicalBERT](https://github.com/kexinhuang12345/clinicalBERT "clinicalbert github")[^clinicalbert].
2. retrained the model using data extracted from [Patient.info](https://patient.info/ "patient dot info website") online forum, specifically topics on inflammatotry diseases.

#### Analysis
With ClinicalBERT training parameters, I also create a stand-alone patient voice model alongside the PatientFORUM model (+ClinicalBERT).
These three models were compared together to show that the combined PatientFORUM model captures valuable information.

1. Firstly an observation is conducted into the models: visualisation via t-distributed stochastic neighbor embedding (t-SNE) to represent the complex relationship between terms.
2. Secondly a Wilcoxon signed-rank test is conducted to observe the semantic similarity scores of terms on the multi-domain model against the single-domain models.
3. Third, a Pearson correlation coefficient in which I look at how each embedding model similarities compare to physician annotations.
4. Finally, as a form of validation I ran the analysis on multiple seeds in expectation of similar results.

### Combined Ontology for Inflammatory Diseases (COID)
The second resource is [COID](https://github.com/sap218/coid/ "coid github")[^coid], an ontology developed for inflammatory diseases, anatomy, symptoms, and more.
Using the methods from Pendleton et al. (2021)[^ocimido], I ran TF-IDF to enhance the ontology with synyoms. 
Futhermore, synonyms were also curated from PatientFORUM embedding model looking at semantic similarity. 

## Outcome
Semantic characterisations of the models revealed clinician-generated models consisted of more frequent misspellings from clinicians and more use of abbreviations from the patient.
Patient priorities were highlighted: showing clinicians have a different understanding of some patient semantics.
Finally, the PatientFORUM embedding model performed better: the clinical domain extended with equivalent-sized, patient-generated data. 

| PatientINF | HuggingFace | COID | Zenodo |
| -------- | ------- | ------- | ------- |
| [{{< figure src="/links/github.png" width=25 alt="patientinf github" >}}](https://github.com/sap218/PatientINF "patientinf github") | [{{< figure src="/links/link.png" width=30 alt="hugging face" >}}](https://huggingface.co/sap218/PatientINF "hugging face") | [{{< figure src="/links/github.png" width=30 alt="coid github" >}}](https://github.com/sap218/coid/ "coid github") | [{{< figure src="/links/link.png" width=25 alt="zenodo" >}}](https://zenodo.org/records/5524650 "zenodo") |

## References

[^clinicalbert]: Huang K, Altosaar J, Ranganath R. Clinicalbert: Modeling clinical notes and predicting hospital readmission. arXiv preprint arXiv:1904.05342. 2019.
[^coid]: Pendleton SC. Combined Ontology for Inflammatory Diseases COID. Zenodo. 2021. https://doi.org/10.5281/zenodo.5524650.
[^ocimido]: Pendleton, S. C., Slater, L. T., Karwath, A., Gilbert, R. M., Davis, N., Pesudovs, K., ... & Braithwaite, T. (2021). Development and application of the ocular immune-mediated inflammatory diseases ontology enhanced with synonyms from online patient support forum conversation. Computers in biology and medicine, 135, 104542.
