---
title: "OcIMIDo"
date: 2021-06-18
toc: true
categories: ['ontology','nlp','tf-idf','sentiment','patient voice','project']
---

# Development and application of the Ocular Immune-Mediated Inflammatory Diseases ontology (OcIMIDo) enhanced with synonyms from online patient support forum conversation

| GitHub | Manuscript | Bioportal | MIRO guidelines |
| -------- | ------- | ------- | ------- |
| [{{< figure src="/links/github.png" width=25 alt="github" >}}](https://github.com/sap218/ocimido "github") | [{{< figure src="/links/paper.png" width=30 alt="manuscript" >}}](https://www.sciencedirect.com/science/article/pii/S001048252100336X?via%3Dihub "manuscript") | [{{< figure src="/links/link.png" width=30 alt="bioportal" >}}](https://bioportal.bioontology.org/ontologies/OCIMIDO "bioportal") | [{{< figure src="/links/guide.png" width=25 alt="miro" >}}](https://sap218.github.io/ocimido/MIRO "miro") |

Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions and in many cases life threatening.
Uveitis itself is one of the top causes of blindness and often undifferentiated: no identifiable cause.

Having good vision is important to our everyday lives and these ocular IMIDs cause problems, such as pain or blurriness.
These symptoms or complications can affect our Quality of Life (QoL).
Not only is there an unmet need for capturing the patient voice and their perspective of ocular IMIDs, but these clinical terms also needed to be standardised.

The patient voice provides insight into their medical journey: ranging from clinical tests, symptoms, side-effects, to treatments.
We can understand the patient better when we understand the terms they use and their emotional wellbeing. 

A resource of patient-generated data is online patient forum conversations; however, these are inaccessible due to being unstructured.
Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text yet currently there are structural and terminology gaps: patient-preferred terms.

## Methodology

I developed an ontology for ocular IMIDs to standardise the clinical vocabulary and structure, based on consensus documents and the guidance of clinical experts.
To apply this ontology to forum conversations, it needed to be expanded with corresponding patient-preferred synonyms.

To capture these patient synonyms, a novel method was applied to the forum, using a statistical technique.
We extracted forum conversation from UK-based [Olivia's Vision](https://www.oliviasvision.org/ "olivias vision") and split the data into training/testing, with the training we used the statistical TF-IDF, which ranks every term in order of importance.
The domain expert manually matched them to OcIMIDo terms.
This statistical method, TF-IDF, allowed for multiple cycles to curate as many important terms.

For validation of the TF-IDF, we annotated term frequency in the forum test set to ensure we didn't miss any synonyms - also observing frequency of terms in both training and test sets.
Additionally had two other domain experts manually annotate the forum conversation for comparison, showing the TF-IDF curation was much more time-efficient.

These curated, patient-generated systems were then mapped to their clinical term to enhance the ontology.
This formally encodes and integrates patient-preferred terms to their formalised and standardised clinical terms within an ontology.

## Impact

Capturing patient-preferred terms aids in understanding the patient voice: we can understand them better through vocabulary and sentiment.
Using both clinical & patient-preferred terms, our text mining efforts were increased.
Futhermore, we extracted another forum, USA-based [Uveitis Foundation](https://uveitis.org/ "uveitis foundation") and observed terms in this forum were location-specific, e.g. US-based medications.
Text mining and sentiment analysis revealed that first posts were significantly more negative than replies, providing insight into the supportive role that online fora play for patients and their carers.
A deeper knowledge of these and QoL can potentially lead to improved condition management and positive QoL interventions: bridging gaps in the clinical and patient domain.

**This is the first ontology of its kind in opthamology.**

{{< figure src="/ontologies/OCIMIDO_Graphical-Abstract_colour_2021.png" caption="**Figure**: Graphical abstract of the the project highlighting the (1) background, (2) methods, and (3) outcome." alt="graphical abstract of the the project" >}}

## Citing

```
@article{PENDLETON2021104542,
title = {Development and application of the ocular immune-mediated inflammatory diseases ontology enhanced with synonyms from online patient support forum conversation},
journal = {Computers in Biology and Medicine},
volume = {135},
pages = {104542},
year = {2021},
issn = {0010-4825},
doi = {https://doi.org/10.1016/j.compbiomed.2021.104542},
url = {https://www.sciencedirect.com/science/article/pii/S001048252100336X},
author = {Samantha C. Pendleton and Luke T. Slater and Andreas Karwath and Rose M. Gilbert and Nicola Davis and Konrad Pesudovs and Xiaoxuan Liu and Alastair K. Denniston and Georgios V. Gkoutos and Tasanee Braithwaite},
}
```
