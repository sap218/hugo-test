---
title: "Jabberwocky"
date: 2021-05-11
categories: ['python','ontology','nlp','tf-idf','project']
---

# Jabberwocky: a `Python` toolkit for NLP tasks and manipulation of those nonsensical Ontologies

Unstructured text is a valuable resource for research, yet text mining is a complicated task.
Text mining with key terms can be limited and potentially enhanced with the knowledge of synonyms.
Especially synonyms in that domain.

Ontologies are useful - they condense a domain of knowledge in a structured manner and classes may have synonyms.
Ontologies have proven useful in text mining tasks, yet there lie gaps in the NLP community for the easy manipulation of ontologies.

**Jabberwocky**
allows a user to extract synonyms (and other metadata) from an ontology giving key terms [classes] of interest.
With these key terms, and corresponding synonyms, users can annotate a corpus for which posts/sentences the term occurs.
An **important feature** as of 2021 is the use of annotation with a Phrase Matcher[^spacy], which users can now use phrases.

**Other features**:
with the methods from Pendleton et al. (2021)[^ocimido] users can run a TF-IDF[^tfidf] (statistical method) to view terms of importance.
An **important feature** as of 2024 is to ability to apply this method via n-grams so rankings are not limited to uni-grams but also bi-grams, tri-grams, and more.
The TF-IDF output can prove useful for updating the ontology and future text mining tasks.
Finally, as of 2024 users can plot an ontology in web or tree format.

| GitHub | Manuscript | Guide | Packaged |
| -------- | ------- | ------- | ------- |
| [{{< figure src="/links/github.png" width=25 alt="github" >}}](https://github.com/sap218/jabberwocky "github") | [{{< figure src="/links/paper.png" width=30 alt="manuscript" >}}](https://joss.theoj.org/papers/10.21105/joss.02168 "manuscript") | [{{< figure src="/links/guide.png" width=25 alt="guide" >}}](https://sap218.github.io/jabberwocky/ "guide") | [{{< figure src="/links/link.png" width=30 alt="zenodo" >}}](https://zenodo.org/records/4747764 "zenodo") |

## References

[^spacy]: [spaCy](https://spacy.io/ "spacy website") `PhraseMatcher()`.
[^ocimido]: Pendleton, S. C., Slater, L. T., Karwath, A., Gilbert, R. M., Davis, N., Pesudovs, K., ... & Braithwaite, T. (2021). Development and application of the ocular immune-mediated inflammatory diseases ontology enhanced with synonyms from online patient support forum conversation. Computers in biology and medicine, 135, 104542.
[^tfidf]: Term frequency inverse document frequency.
