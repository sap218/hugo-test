---
title: "Jabberwocky"
date: 2021-05-11
categories: ['python','ontology','nlp','tf-idf','project']
---

# Jabberwocky: a `Python` toolkit for NLP tasks and manipulation of those nonsensical Ontologies

Unstructured text is a valuable resource for research, yet text mining is a complicated task.
Text mining with key terms can be limited and potentially enhanced with the knowledge of synonyms.
Especially synonyms in that domain.

Ontologies are useful as they condense a domain of knowledge in a structured manner.
Concepts in an ontology have a label and possibly synonyms, yet in cases there lacks this vital information.
Ontologies have proven useful in text mining tasks, yet there lie gaps in the NLP community for the easy manipulation of ontologies.

**Jabberwocky** allows a user to extract synonyms from an ontology giving keywords [concepts] of interest. 
Jabberwocky uses [spaCy](https://spacy.io/ "spacy website") `PhraseMatcher` to curate text from a corpus using these keywords and corresponding synonyms.

Using the methods from Pendleton et al. (2021)[^ocimido], Jabberwocky offers TF-IDF (statistical method) for users to view terms of importance - which could prove useful for the ontology and future text mining.
Finally, Jabberwocky allows a user to update their ontology via adding new synonyms (possibly extracted from the TF-IDF).
With these new synonyms, you can re-run Jabberwocky to curate more from the corpus.

| GitHub | Manuscript | Guide | Packaged |
| -------- | ------- | ------- | ------- |
| [{{< figure src="/links/github.png" width=25 alt="github" >}}](https://github.com/sap218/jabberwocky "github") | [{{< figure src="/links/paper.png" width=30 alt="manuscript" >}}](https://joss.theoj.org/papers/10.21105/joss.02168 "manuscript") | [{{< figure src="/links/guide.png" width=25 alt="guide" >}}](https://sap218.github.io/jabberwocky/ "guide") | [{{< figure src="/links/link.png" width=30 alt="zenodo" >}}](https://zenodo.org/records/4747764 "zenodo") |

## References

[^ocimido]: Pendleton, S. C., Slater, L. T., Karwath, A., Gilbert, R. M., Davis, N., Pesudovs, K., ... & Braithwaite, T. (2021). Development and application of the ocular immune-mediated inflammatory diseases ontology enhanced with synonyms from online patient support forum conversation. Computers in biology and medicine, 135, 104542.
