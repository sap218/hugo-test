---
title: "Ocular Immune-Mediated Inflammatory Diseases ontology (OcIMIDo)"
date: 2021-06-18
toc: true
categories: ['ontology','nlp','tf-idf','sentiment','patient voice','inflammation','tool']
---

# Development and application of the Ocular Immune-Mediated Inflammatory Diseases ontology (OcIMIDo) enhanced with synonyms from online patient support forum conversation

**OcIMIDo** is the first ontology of its kind in opthamology[^ocimido].
Available open-source on [GitHub](https://github.com/sap218/ocimido "github") and other biomedical ontology platforms, including [Bioportal](https://bioportal.bioontology.org/ontologies/OCIMIDO "bioportal").

## Background

Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions (usually life-long) and in many cases, life threatening.
Uveitis itself is one of the top causes of blindness and often undifferentiated: no identifiable cause.

Having good vision is important and although these ocular IMIDs can cause problems (pain, blurriness, etc.) our quality of life (QoL) is affected differently.
Not only is there an unmet need for capturing the patient experience with ocular IMIDs, but the terminology of ocular IMIDs also need to be standardised.

The patient perspective provides insight: ranging from type of disorder, symptoms, side-effects, and treatments.
A resource of the patient perspective is the format of online forum conversations.
However, these are inaccessible due to being unstructured and patients may have their own vocabulary.

Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text.
There are structural and terminology gaps in concepts relating to ocular IMIDs respresented in current biomedical ontologies.

## Methodology

I developed an ontology for ocular IMIDs - OcIMIDo - to standardise the clinical vocabulary and structure, based on consensus documents and the guidance of clinical domain experts.
To apply this ontology to forum data, it needed to be expanded with corresponding patient-preferred synonyms.
And so to capture these patient synonyms, a novel method was applied to the forum, using a statistical technique.

We extracted the patient-generated forum conversations from the UK-based [Olivia's Vision](https://www.oliviasvision.org/ "olivias vision") charity (with permission).
The data was split into training/testing subsets. With the training, we used the statistical technique that ranks every term in order of importance.
The domain expert manually reviewed and matched any patient-generated terms to their corresponding clinical term.

With the curated/matched patient-generated synonyms and clinical terms, OcIMIDo was enhanced/expanded.
This formally encodes and integrates patient-preferred terms to their formalised and standardised clinical terms within an ontology.

For validation, we applied the same technique in the test set to ensure we didn't "miss" anything of importance.
Additionally two other domain experts manually annotated the forum data - timing their efforts.
Futhermore, with another forum, USA-based [Uveitis Foundation](https://uveitis.org/ "uveitis foundation") OcIMIDo term frequency was observed, revealing location-specific differences, e.g. US-based medications.

For appliction, sentiment (opinion mining) analysis was conducted on the forum data.

## Impact

Capturing patient-preferred terms aids in understanding the patient voice.
The computational statistical techique for synonym curation, was much more time-efficient, despite some manual review.

Using both clinical & patient-preferred terms in analysis, text mining efforts were increased, leading to a more fruitful sentiment analysis.
Sentiment analysis revealed that first posts were significantly more negative than replies, providing insight into the supportive role that online fora play for patients and their carers.

This research can lead to improved patient condition management and positive QoL interventions: bridging gaps in the clinical and patient domain.

{{< figure src="/ocimido/OCIMIDO_Graphical-Abstract_colour_2021.png" width=600 caption="**Figure**: Graphical abstract of the the project highlighting the (1) background, (2) methods, and (3) outcome. See the [MIRO](https://sap218.github.io/ocimido/MIRO 'miro') guidelines for reporting an ontology." alt="graphical abstract of the the project" >}}

## References

[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
