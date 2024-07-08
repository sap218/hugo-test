---
title: "Jabberwocky"
date: 2021-05-11
categories: ['python','ontology','nlp','tf-idf','project']
---

# Jabberwocky

**Jabberwocky** is a Natural Language Processing (NLP) toolkit for those nonsensical ontologies[^jabberwocky].
Available open-source on [GitHub](https://github.com/sap218/jabberwocky "github").

Unstructured text is a valuable resource for research, yet text mining is a complicated task.
Text mining with key terms can be limited and potentially enhanced with the knowledge of synonyms.
Especially synonyms in that domain.

Ontologies are useful - they condense a domain of knowledge in a structured manner and classes may have synonyms.
Ontologies have proven useful in text mining tasks, yet there lie gaps in the NLP community for the easy manipulation of ontologies.

**Jabberwocky features** includes the extraction of synonyms (and other metadata) from an ontology giving key terms [classes] of interest.
With these key terms, and corresponding synonyms, users can annotate a corpus for which posts/sentences the term occurs.
An **updated feature** as of 2021 is the use of annotation with a Phrase Matcher[^spacy], which users can now use phrases.

**Other features**:
with the methods from Pendleton et al. (2021)[^ocimido] users can run a TF-IDF[^tfidf] (statistical method) to rank all corpus terms via importance.
An **updated feature** as of 2024 is to ability to apply this method via n-grams so rankings expand to uni-grams, bi-grams, tri-grams, and more.
The TF-IDF output can prove useful for updating the ontology and future text mining tasks. Users can also update the ontology with other metadata.
Finally, as of 2024 users can plot an ontology in web or tree format.

{{< figure src="/jabberwocky/workflow.png" width=800 caption="**Figure**: Workflow of Jabberwocky features. Read the [documentation](https://sap218.github.io/jabberwocky/ 'jabberwocky documentation') for more information and a scenario." alt="jabberwocky features visualised" >}}

## References

[^jabberwocky]: Pendleton, Samantha C., and Georgios V. Gkoutos. "[Jabberwocky](https://joss.theoj.org/papers/10.21105/joss.02168 "jabberwocky manuscript"): an ontology-aware toolkit for manipulating text." Journal of Open Source Software 5.51 (2020): 2168.
[^spacy]: Honnibal, Matthew, et al. "[spaCy](https://spacy.io/api/phrasematcher "spacy phrase matcher function"): Industrial-strength natural language processing in python." (2020).
[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
[^tfidf]: [Term frequency inverse document frequency](https://en.wikipedia.org/wiki/Tf%E2%80%93idf "Wikipedia link to TF-IDF").
