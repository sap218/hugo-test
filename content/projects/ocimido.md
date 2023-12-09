---
title: "OcIMIDo"
date: 2021-06-18T14:45:03+01:00
draft: true
toc: false
---

# Ocular Immune Mediated Inflammatory Disease Ontology (OcIMIDo)

The patient voice is a valuable resource for advancing patient care, however text mining efforts for patient unstructured text is difficult as they contain patient-preferred terms, rather than formal clinical terms. To overcome these text mining efforts, we proposed development of an ontology to address the challenge presented by unstructured text data.

We started by looking at uveitis, inflammatory eye disorder of the uvea, and noticed current biomedical ontologies are not fully representing our domain of interest. We initially designed an ontology for uveitis and then expanded for the other inflammatory eye disorders and included associated diseases, complications, and medical therapies.

OcIMIDo is the first ontology of its kind in ophthalmology, developed via domain expertise and clinical guidelines.

We extracted forum conversation from UK-based Olivia’s Vision and split the data into training/testing, with the training we used a novel synonym extraction method (tf-idf), which ranks every term in order of importance. Our domain expert manually matched them to OcIMIDo terms - after the first round of tf-idf, we removed OcIMIDo terms from the forum, and re-ran. We did this until no more synonyms could be added to OcIMIDo.
For validation, we annotated term frequency in the forum test set to ensure we didn’t miss any synonyms - also observing frequency of terms in both training and test sets. Additionally had two other domain experts manually annotate the forum conversation for comparison, showing the tf-idf curation was much more time-efficient.

Using both clinical & patient-preferred terms, our text mining efforts were increased: e.g. using “methotrexate” with patient-preferred terms: “mtx”, “mxt” (a common misspelling based on ranking), and “amethopterin” increased the post count by 80%, from 185 to 333. Futhermore, we extracted another forum, USA-based Uveitis Foundation and observed terms in this forum were location-specific, e.g. US-based medications.
The increase in text mining efforts facilitates sentiment analysis for capturing the patient’s voice, we used pretrained models TextBlob and VADER. Sentiment analysis revealed that first posts were significantly more negative than replies, providing insight into the supportive role that online fora play for patients and their carers.