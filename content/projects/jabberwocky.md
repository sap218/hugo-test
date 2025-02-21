---
title: "Jabberwocky: an NLP toolkit for those nonsensical ontologies"
date: 2021-05-11
categories: ['python','ontology','nlp','tf-idf','tool']
---

# Jabberwocky

{{< color-block style="success" >}}
Most recent version: 3.1.1 (20-02-2025)
{{< /color-block >}}

**Jabberwocky** is a Natural Language Processing (NLP) toolkit for those nonsensical ontologies[^jabberwocky].
Available open-source on [GitHub](https://github.com/sap218/jabberwocky "github").

Unstructured text is a valuable resource for research, yet text mining is a complicated task.
Text mining with key terms can be limited and potentially enhanced with the knowledge of synonyms.
Especially synonyms in that domain.

Ontologies are useful - they condense a domain of knowledge in a structured manner and classes may have synonyms.
Ontologies have proven useful in text mining tasks, yet there lie gaps in the NLP community for the easy manipulation of ontologies.

Please see the [documentation](https://sap218.github.io/jabberwocky/ "documentation") for more information on features.
Below is a summary:

+ **`bandersnatch`**: extract metadata from ontology classes.
+ **`catch`**: annotate corpus with key terms and generate visualisations.
+ **`bite`**: rank terms in order of importance from a corpus.
+ **`arise`**: update ontology with new metadata.
+ **`eyes`**: ontology plotting function.

{{< figure src="/jabberwocky/workflow.png" width=800 caption="**Figure**: Workflow of Jabberwocky features. Read the [documentation](https://sap218.github.io/jabberwocky/ 'jabberwocky documentation') for more information and a scenario." alt="jabberwocky features visualised" >}}

[**Changelog**](https://github.com/sap218/jabberwocky/blob/master/Changelog.md "change log")

I started development in 2019 and Jabberwocky **v1.0** was published in 2020[^jabberwocky].
Jabberwocky both influenced and was influenced by the OcIMIDo project[^ocimido].

Version **2.0** (2021) improved the annotation script with a Phrase Matcher[^spacy] so both key terms and phrases work.

After a few years of a PhD and starting a job, in 2024 I came back to Jabberwocky and Version **3.0** was a complete revamp of the repository.
High-level functions for stop word removal & text cleaning and a new plotting feature was introduced: a pretty word cloud!
Furthmore, shortly after version **3.1** was released! This included a new plotting feature, `eyes`, to plot an ontology.
And the TF-IDF[^tfidf] (statistical method) was improved with the to ability to use n-grams so rankings can expand to uni-grams, bi-grams, tri-grams, and more.

In 2025, **v3.1.1** updates were inspired by an old project - [cyannotator](https://github.com/sap218/cyannotator "cyannotator") - users can now request an `HTML` output of the corpus with key terms highlighted.

## References

[^jabberwocky]: Pendleton, Samantha C., and Georgios V. Gkoutos. "[Jabberwocky](https://joss.theoj.org/papers/10.21105/joss.02168 "jabberwocky manuscript"): an ontology-aware toolkit for manipulating text." Journal of Open Source Software 5.51 (2020): 2168.
[^spacy]: Honnibal, Matthew, et al. "[spaCy](https://spacy.io/api/phrasematcher "spacy phrase matcher function"): Industrial-strength natural language processing in python." (2020).
[^ocimido]: Pendleton, Samantha C., et al. "Development and application of the [ocular immune-mediated inflammatory diseases ontology](https://www.sciencedirect.com/science/article/pii/S001048252100336X "paper for ontology project") enhanced with synonyms from online patient support forum conversation." Computers in biology and medicine 135 (2021): 104542.
[^tfidf]: [Term frequency inverse document frequency](https://en.wikipedia.org/wiki/Tf%E2%80%93idf "Wikipedia link to TF-IDF").
