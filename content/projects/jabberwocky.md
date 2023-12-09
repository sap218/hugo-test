---
title: "Jabberwocky"
date: 2021-05-11T14:45:03+01:00
draft: true
toc: false
---

# Jabberwocky: a toolkit for those nonsensical Ontologies

Jabberwocky is a Python toolkit designed for ontology manipulation and natural language processing (NLP) [1]. Unstructured text is a valuable resource for research and extracting important sentences is a complicated task - we can extract valuable information using terms, however we can potentially extract more with synonyms, especially synonyms common in that domain of knowledge.
Ontologies are a useful as they condense a domain of knowledge in a structured manner - for example when looking at an ontology for anatomy, we can see that: hand is part of arm. The information surrrounding "arm" can include a description in addition to synonyms, e.g. "upper limb".
Current existing tools, such as spaCy or NLTK, are brilliant in the domain for NLP, however don't include an ontology plug-in aspect.

Jabberwocky allows a user to extract synonyms from an ontology giving words of interest, e.g. "arm", "foot", and "head". Jabberwocky uses spaCy PhraseMatcher to curate sentences from a text document using these words and synonyms of interest. Using the methods from Braithwaite et al. (2020), Jabberwocky offers a tf-idf statistical analysis for users to view terms of importance [2]. Viewing these high scoring important terms, you may notice synoynms which weren't previously in the ontology or which you didn't consider, you can update the ontology by adding new synonyms.
With these new synonyms, you can re-run Jabberwocky to curate more sentences using these words and updated synonyms of interest.

Jabberwocky v1.0 was released June 2020, however v2.0 was released May 2021. Version 2 update includes spaCy PhraseMatcher for sentence extraction and the ability to plot the tf-idf top-30 terms.