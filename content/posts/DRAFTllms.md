---
title: "What's the <catch> with ChatGPT?"
date: 2025-01-21
draft: true
toc: true
categories: ['python','machine learning','nlp','semantic similarity','sentiment','trends']
---

# Validation of NLP tools and comparison to LLMs

##### Validation of NLP tools and comparison to LLMs

## Introduction

’
“word”

Many Natural Language Processing (**NLP**) tools are perhaps becoming obsolete with the emergence of complex Large Language Models (**LLMs**), most notably ChatGPT.

LLMs have been around for a while but gained attention around 2020 when GPT3 was released by OpenAI[^openai].
LLMs are designed to understand human language and are trained on large amounts of text: books, code, social media, clinical documentation, transcripts, and more.
These models learn the patterns in language in order to "communicate".
When asked a question, the model observes the tokens (words) you used and based on its knowledge, it’ll generate a response by predicting/arranging tokens in such a way that resembles a conversation.

LLMs don’t actually think or understand these patterns. For example, back in 2020 if you’d ask an LLM for a list of published papers, the model would generate “fake” references based on recognising how citations are typically structured and authors in that research area - rather than providing real, verified sources.

**Side note**: readers can explore ChatGPT and ask some questions if they haven’t already: [https://chatgpt.com/](https://chatgpt.com/).

Jabberwocky is an NLP toolkit designed to handle unstructured text, with features to implement those nonsensical ontologies[^jabberwocky].
I have been developing [Jabberwocky]({{< ref "jabberwocky" >}} "jabberwocky blog") since 2019 and over time has expanded with more capabilities. 

The primary NLP annotation function is Catch that uses a [`PhraseMatcher()`](https://spacy.io/api/phrasematcher "link to spacy python library") to annotate a corpus with words - or phrases - of interest.
See the [GitHub](https://github.com/sap218/jabberwocky) for more information on functionality.

**Annotation**
: to add meaningful information to text data. In the context of this article, to indicate whether a specific word is present in a sentence.

Jabberwocky was developed because manually annotating a corpus is an exhaustive task, especially data large in size, and often researchers can miss important information, for example, they may not consider particular synonyms, accidentally skip over lines, or don’t consider the context.

This article aims to compare manual annotation, Jabberwocky’s Catch, and various LLMs to show differences in how manual, computational tools, and an LLM’s ability to annotate text.

**Side note**: although ChatGPT is mentioned in the name, I won’t be using that specific model and instead use models from Google, Meta, and Mistral.
Additionally, I aimed to time each method but the LLMs are being accessed via API requests, after the first 30 requests there are delays and so I decided to average them across models and raise here that they cannot be fairly compared.

##### Experiments in comparison to a Manual task

+ Experiment 1: to annotate text (binary, 1/0) if a word (+synonym) is present.
+ Experiment 2: after following the same steps as experiment 1, for those annotated (1) a sentiment score is to be derived.
+ Experiment 3: similar to experiment 1 to annotate text, however this task is to compare a precise objective vs. a broader aim.

***

## Methods

Using [Kaggle](https://www.kaggle.com/ "link to kaggle") to access an open source data set, I downloaded a [dataset](https://www.kaggle.com/datasets/alexandrakim2201/spotify-dataset?resource=download "link to dataset") on Spotify user reviews.

This dataset has **51,473** rows, however considering time to manually annotate, I used pandas `sample()` to filter for a **random 100** posts:

```
df.sample(n=100, random_state=123)
```

### Experiment 1 - binary

As mentioned, experiment 1 a binary task to annotate text 1 or 0 if a word is present, also considering synonyms.
After a very - quick - initial review, I chose the following words of interest: advertisement, audio, download, and update.
I then considered synonyms, plus a quick Google search.

I timed the manual annotation exercise and noted a 1 for each post if the word (and/or synonym) was present.
After the manual annotation, some additional synonyms were highlighted:
+ **Advertisement**: ad, advert
+ **Audio**: bluetooth\*, quality, sound
+ **Download**: redownload\*
+ **Update**: change\*, fix\*, upgrade\*\*, version

\*curated from data; \*\*google.

### Experiment 2 - sentiment

Experiment 2 follows similarly to experiment 1, text is checked for a word (and/or synonyms) then a sentiment score is derived for those annotated.
In this task, I used “**music**” as the topic of interest and the following synonyms were included: song, listen\*, and track.
The main objective in this task is looking at how each method derives a sentiment score: a human’s opinion against LLM interpretation.
\*curated from data.

Sentiment ranges from -1 (negative) to 0 (neutral) to 1 (positive). Humans can have difficulty scoring sentiment and can be subjective to what is neutral and so with manual annotation I annotated only “p” or “n”. 
With the computational scores, I can convert them into “p” and “n” via thresholds:

```
if Score > 0.05 = p (positive)
elif Score < -0.05 = n (negative)
else = neutral
```

Jabberwocky doesn’t have sentiment analysis included yet and so in this experiment after Catch does the annotation, each annotated post will go through [VADER](https://github.com/cjhutto/vaderSentiment "link to vader") sentiment analysis.
It is my goal in the future to implement sentiment analysis into Jabberwocky as a function.

### Experiment 3 - broader

In a final experiment, although similar to experiment 1 in terms of annotating text for terms and synonyms, the focus will shift in this experiment to comparing search strategies: each method will conduct two inner tests relating to **paying for the App**. 

The first is a precise approach to annotate posts relating to App payments, for example Catch is to annotate using only “pay” while LLMs will annotate posts related to paying for the App.
The second test is broader: Catch will annotate using various terms alongside “pay” and the LLMs will annotate if the post is related to paying for the App with additional terms.

This experiment covers three methods: manual annotation to highlight posts related to paying for the App; Catch will show the power of additional terms/synonyms for annotation tasks; and LLMs will show the flexibility and differences in approaches for models.

Additional terms/synonyms: buy, cents\*, expensive, features, free, invaluable\*, money, paid, payment, premium, price, subscribe\*.

*curated from data.

### Jabberwocky

Jabberwocky’s Catch script includes text cleaning, lemmatisation (putting words in base form), and removes stop words (e.g. we, my, had, isn’t).
The code snippet below shows this:

```
[in] Hello world! This is an example of text cleaning with lemmatisation and stop word removal!
[out] hello world example text clean lemmatisation stop word removal
```

As you can see, tokens are put in lowercase and special characters (!) are cut.
Words like “this, is, an, of, with, and” are stop words and so have been removed.
The word “cleaning” has been put into base form as “clean” (lemmatisation).

### LLMs

Using [GroqCloud API](https://console.groq.com/docs/quickstart "link to groq cloud") I chose 3 [models](https://console.groq.com/docs/models "link to groq models") - see Table N below.
The column, “Referred as” is how these models will be mentioned throughout this article.

| Model | Developer | Referred as |
|-------|-----------|-------------|
| [`gemma2-9b-it`](https://huggingface.co/google/gemma-2-9b-it) | Google | Gemma |
| [`llama-3.1-8b-instant`](https://github.com/meta-llama/llama-models/blob/main/models/llama3_1/MODEL_CARD.md) | Meta | Llama |
| [`mixtral-8x7b-32768`](https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1) | Mistral | Mixtral |

Table N: The models used in this experiment.

### Statistics

In this final section, I have introduced the various statistical tests I conduct throughout the experiments.

Experiment 1:
+ **Accuracy**: how often the method predicted the manual 1s and 0s. For example, 0.97 means the method correctly identified 97 out of every 100 cases.
+ Cohen's **Kappa**: measures how well the method agrees with the manual annotation, highlighting performance if meaningful or randomness. For example, a score of 0.8 means a strong agreement. An **agreement** score was also derived via a [threshold](https://pmc.ncbi.nlm.nih.gov/articles/PMC3900052/table/t3-biochem-med-22-3-276-4/ "link to kappa threshold"). 
+ Matthews **Correlation** Coefficient: measure of the method's performance considering all correct and incorrect predictions. For example, 0.86 indicates the method is performing well and a strong positive correlation. It is useful with uneven distributions of 1s and 0s. 
+ **Precision**: how accurate the predicted 1s are. For example, 0.77 means 77% of the time the method correctly predicted 1.
+ **Recall** (also called sensitivity): measures how good the method is at identifying actual 1s and not missing any. For example, 1 (or 100%) means the method correctly predicted all the "1" cases.
+ **F1-score**: the balance between precision and recall. For example, 0.87 means the method strikes a pretty good balance between catching all 1s (recall) AND ensuring 1s are accurate (precision). Useful with uneven distributions of 1s and 0s.

Experiment 2:
+ Converting scores into ints, I curated: Accuracy, Kappa, and Correlation.
+ For the continuous scores, I conducted a **T-statistic**: the difference between two methods via the averages, considering variability. A larger T-statistic (from 0) suggests a greater difference.

Experiment 3:
+ **McNemar**: measures the size of change of two related techniques, e.g. precise vs. broad. A higher McNemar value represents the number of discordant pairs (changes between conditions).
+ **Friedman**: check for significant differences in related groups, e.g. differences in all broad methods. Larger values indicate a greater difference between groups (one method may perform noticeably better/worse than others).

Most importantly, **P-values** were calculated.
A P-value represents the randomness of the statistical test.
A small P-value indicates significance, meaning the test is unlikely to be random.
P-value size is often discussed/disputed as to define what is significant, often we see p<0.05 is the limit for significance.

***

## Results

### Experiment 1

#### Timings

#### Counts

#### Advertisement

#### Audio

#### Download

#### Update

### Experiment 2

#### Timings

#### Counts

#### Sentiment

### Experiment 3

#### Timings

#### Counts

#### Precise vs. Broad

#### Method vs. Method

***

## Discussion

These experiments - although small - have shown how straightforward it can be to conduct annotation tasks.
The move to computational methods means computers are doing a heavier bulk of the work, in such a shorter time, but we shouldn’t ignore the importance of statistical tests for validation, specifically against some manual annotation to highlight how reliable and accurate methods are.

I manually annotated a series of reviews for an App and then used NLP tools and LLMs to do the same task.
Although manually annotating text is often considered the “gold standard”, it can be quite a time-consuming, draining task and users may make mistakes - as I did - despite the small sample size. 

The first limitation of this study is that my opinions can be subjective.
Moreover, Catch annotated the exact thing I asked for, this introduces bias: I developed Catch and I know its capabilities despite wanting to see how it compared to the novel LLMs.
Regardless, we saw that LLMs sometimes considered context/related words for annotation - does this mean I missed vital information, despite the LLM ignoring the direct request?
Can we reliably use LLMs if they do more than what was asked?

For each experiment, there was a topic of interest: a word and corresponding synonyms.
I chose these synonyms, I did a quick Google search, and more were curated from the text after my annotations.
Are the synonyms correct? Could I be missing more? Are there any hidden synonyms the LLMs used?

Without synonyms, Catch has a poor performance, concluding that Synonyms are invaluable for these sorts of NLP tasks.
This is why synonym extraction tasks are useful (see Jabberwocky’s [Bite](https://github.com/sap218/jabberwocky) function).
For Catch to be even more useful, one would probably need to include common misspellings or abbreviations.
Catch included functions for text cleaning in order to annotate, a user can modify this to suit their objective.

In contrast, LLMs take text directly - without any cleaning or formatting - as the models are trained on unstructured text.
However, as mentioned, the models often “ignored” the request and annotated posts if similar words are included: sometimes incorrect, sometimes correct.
Furthermore, LLMs tokenise words for processing and so this task of exact word matching can lead to inconsistencies.

To continue with the LLM request issue: these LLMs may be trying to “over complicate” the request and look for a “deeper” meaning: these models are overfitting!
These additional annotations from the models means they are involving semantics, and although could be correct, is going against the request.
It is important to note that some models, specifically Mixtral, are designed for more complex tasks and perhaps a little “overkill” for these “simple” experiments, or perhaps need more optimisation - which may also explain why Mixtral’s sentiment analysis had a stronger agreement with the manual.

Highlighting again about manually annotating being a time-consuming task, Catch took mere seconds to annotate whilst the LLMs - although still half the time compared to manual - took around 3 minutes for each word (+synonyms).
I cannot fairly compare these results due to the API request limits.
In future we can consider using the [TensorFlow](https://www.tensorflow.org/) toolkit to run the LLMs locally via GPU which would drastically speed these annotation tasks.
Some other things to consider is the model choice - I chose these based on what was available from GroqCloud and choose from different developers.
In reality with a subscription, I can access more advanced models and the API requests will be faster.

Catch and Gemma consistently had better agreement with the manual annotation, even highlighting some posts that the manual, I, missed. 
Catch and Gemma also had strong agreements amongst each other. Despite these agreements, Gemma typically searched more broadly.
Synonym choice, again, is important: although more were available for “update” resulting in better performance for Llama, it seemed that Catch and Gemma picked up more posts than necessary. 
However in experiment 3’s broader search, all methods had improved results with more synonyms.

Before finishing with some notes on LLMs, to briefly discuss the sentiment analysis, it seemed that each method moderately agreed with the manual annotation and scored in their own way.
Although I made a mistake in one, I would say a user’s opinion is more reliable than a computer’s.

And finally, LLMs require a strong prompt.
You might have noticed that in the requests, I specifically had to note: `Your response should only have the necessary data of a...` this is because LLMs would respond with an introductory response, e.g. `Here’s the result based on whether <word> is mentioned in the sentence...`.
Moreover, for the sentiment analysis, I found the LLM would provide a score unless I specifically included the following statement: `do not bother with the sentence if a word of interest is not present`.
This was one of the drawbacks of LLMs: having to wrangle with the prompt.

### Conclusion

Overall, with manual annotation we can review posts ourselves: we can investigate on a more granular level and consider context (sarcasm), synonyms, and misspellings or abbreviations.
However, humans can make mistakes, and mistakes can become more frequent with more data.
Furthermore, with more data means more time and effort and so annotating becomes an exhaustive task and mistakes can become more frequent.

NLP tools on the other hand are much faster and can handle larger volumes of data more efficiently.
Yet may not consider the wider context.
To tap into the full potential of these tools, one needs to have prerequisite knowledge of synonyms, common misspelling, or abbreviations.
Moreover, the effectiveness of these tools may depend on parameter fine-tuning.
For example, one needs knowledge in text cleaning and other unstructured text formatting methods to know if the text should be cleaned more harshly or if lemmatisation is appropriate.

LLMs have thought beyond the request prompts: doing more than what was required by considering context and semantics in their responses.
With sufficient computational resources they can be extremely useful.
But one should consider the complexity of the task before using LLMs.
And finally, LLMs themselves admit they can make mistakes: these models’ patterns could be built on unreliable sources.

Validation is invaluable though, so going forward, manual work is essential to ensure the work is accurate and reliable.

## References

[^openai]: Brown TB, Mann B, Ryder N, Subbiah M, Kaplan J, Dhariwal P, et al. Language Models are Few-Shot Learners. arXiv. 2020. Available: https://splab.sdu.edu.cn/GPT3.pdf
[^jabberwocky]: Pendleton S, Gkoutos G. [Jabberwocky](https://joss.theoj.org/papers/10.21105/joss.02168 "jabberwocky manuscript"): an ontology-aware toolkit for manipulating text. Journal of Open Source Software. 2020;5: 2168. doi:10.21105/joss.02168
