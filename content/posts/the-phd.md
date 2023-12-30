---
title: "The PhD"
date: 2023-12-12
toc: true
categories: ['phd','my perspective','ontology','machine learning','patient voice','sentiment','semantic similarity']
---

# Becoming a Doctor in Clinical Informatics

{{< color-block style="info" >}}
The information in this post is my personal PhD journey. I aim to inform and share my PhD (experience and research) with you – the reader.
{{< /color-block >}}


## Year 1

> You don't have as much experience as I would have thought…

This was one of the first things said to me...during my first week.
Imposter syndrome was planted and settling in for the long haul.

For the first month there was no desk for me and so I sat alone in the quiet working room. 
I felt quite isolated - this was just an unfortunate start to the PhD.
But I *tried* to push forward: I read papers, followed tutorials ([infamous Pizza for ontologies](https://protegewiki.stanford.edu/wiki/Protege4Pizzas10Minutes "Protege tutorial for ontologies")), and playing around with a dataset.

I wanted to prove that person wrong. I spent the first 9 months trying my best to impress.
But it always felt like nothing I did was good enough.
I would read about a particular method as they instructed, but then they'd say I'm wasting too much time reading and should focus on being able to run it.
Yet, when I tried presenting results, I would be questioned about every little detail (which I would've known from further reading) and if I didn't know the smallest detail I would be berated and told I didn't know enough.

Now reflecting from experience, I would like to say that the above should not have happened.
I don't believe it is fair to act like that around a new student - I avoided working in the office because of this.
And I don't want to share negativity that will push people away from a PhD, but I appreciate that I can use my platform to reflect on my time over the years.

My first-year progress review was approaching, so I met with my supervisor about the work I've been doing for the past year, and one particular project changed things...

> I'm very impressed!

And there it was - I was a little teary. I finally felt like I knew what I was doing.
Validation that I was making progress and that I wasn't doing a bad job...in fact I was doing OK.
There were days I still felt like a burden, but I was feeling better after *finally* some positive feedback.
I continued to second guess myself throughout the PhD but majority in good research practice.

## Year 2

The second year definitely followed the "second year blues" and I was a little lost in finding the story of my PhD.
Although I had multiple projects in the works, I didn't know the trajectory and how these projects connected.
But I continued on...
On my birthday I [presented at my first seminar](https://twitter.com/sap218/status/1225068022483836929 "first seminar").

{{< figure src="/academia/first-seminar.jpg" width="600" alt="presenting at my first seminar on my birthday" >}}

And then **COVID**.

At the beginning of March, as reports of COVID was present in the UK and rumours of university staff infected, I decided to work from home.
Not long after, the UK went into lockdown. 
My new office was in my house and I become quite the "agoraphobe" and struggled to leave the house (eventually persuaded to [visit the beautiful National Botanical Garden of Wales](https://twitter.com/sap218/status/1305896697705508871)).
But a **fun fact**: as a new hobby I dived deep into creative things, such as [digital art](https://twitter.com/sap218/status/1309595880190861313) and [pottery](https://twitter.com/sap218/status/1349410440821014530). 

Although the second year started with the blues, during the Summer I found a spark in my work and headed into a direction: **Patient Voice and Inflammation**.

I discovered the story I wanted to tell and the research I wanted to dive into.
This passion was investigating patients: the data they generate (e.g. forums or questionnaires).
I wanted to research the patient perspective - the terms they used and their emotions - within the clinical domain.

I originally hoped to look at patients with all types of inflammation, but this would cover too large a topic.
So, I narrowed down to chronic, autoimmune, inflammatory disorders with a strong association.

## Year 3

We had our heading!

The plot to this PhD was set. The data was curated from various sources and so the research followed through.
This final year was stressful as I felt a lot of pressure to produce "outstanding" results, but also enjoyable as I really found my passion for research.

Lots of online meetings with lots of slideshows that each week were updated with new results.
Tense conversations were had but all to a good purpose: I was becoming a better communicator of science.

### Writing-up

Writing-up the PhD was quite the experience.
I had heard stories from others and I previously watched my [partner complete their PhD]({{< ref "/outsider-perspective-of-phd" >}} "outside perspective of PhD") and somewhat knew what was coming.
However I enjoy writing.

This experience was fun for me: I collected all my research, methods, results into one large document.
It was like a trip down memory lane - I saw my own work grew.
Toward the end, for the final discussion chapter, I started to grow tired. This was the few areas of the thesis I struggled with because it was the final hurdle.

I especially grew tired of the review process: I had to reread the thesis multiple times to spell-check, grammar-check, and more.
This part was especially difficult as I didn't have much time left and was told that my grammar wasn't the best.
I was both worried and frustrated as I had hoped to have that sort of feedback earlier.

So with the help from my partner, we spent a lot of evenings proof-reading the thesis. Which I am forever grateful for as I know it was a huge burden/task.

## Chapters summary

Inflammation is the body's first response to threat, generally present in many cases, and has a complex relationship with a wide range of diseases.

### Chapter 1
Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions and in many cases life threatening.
Uveitis itself is one of the top causes of blindness and often undifferentiated: no identifiable cause.

Having good vision is important to our everyday lives and these ocular IMIDs cause problems, such as pain or blurriness.
These symptoms or complications can affect our Quality of Life (QoL).
Not only is there an unmet need for capturing the patient voice and their perspective of ocular IMIDs, but these clinical terms also needed to be standardised.

The patient voice provides insight into their medical journey: ranging from clinical tests, symptoms, side-effects, to treatments.
We can understand the patient better when we understand the terms they use and their emotional wellbeing. 

Sentiment analysis is essentially opinion mining - we can look at the emotions of particular medical therapies to better design treatment plans.
Sentiment analysis uses clinical terms to mine valuable results, however the task benefits with synonyms: additionally, patients may have their own vocabulary.

A resource of patient-preferred synonyms is online patient forum conversations; however these are inaccessible due to being unstructured.
Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text yet currently there are structural and terminology gaps.

**Ontology**
: a domain of knowledge condensed into a machine-readable format. For example: domain = anatomy, concepts in the ontology includes: hand, arm, and relationship can be hand "part of" arm.

This chapter built an ontology for ocular IMIDs to standardise the clinical vocabulary and structure, based on clinical experts and consensus documents.
To apply this ontology to forum conversations, it needed to be expanded with corresponding patient-preferred synonyms.

To capture these patient synonyms, a statistical technique for important terms was applied to the forum to curate, annotate, and then enhance the ontology.
This formally encodes and integrates patient-preferred terms to their formalised and standardised clinical terms within an ontology.
These terms and synonyms improved text mining and so a more fruitful sentiment analysis.

Capturing patient-preferred terms aids in understanding the patient voice: we can understand them better through vocabulary and sentiment.
A deeper knowledge of these and QoL can potentially lead to improved condition management and positive QoL interventions: bridging gaps in the clinical and patient domain.

### Chapter 2

This chapter continued to investigate the differences between the terms clinicians and patients use.
The clinical experts and I noticed a large number of *surprising* terms that the patient used.
In my research and literature review, previous work has found that patients mention things amongst themselves that they would not to clinicians or terms that the clinician is unfamiliar with.

To better understand the patient and clinician, semantic similarity is explored to map terms.
Semantic similarity can be encapsulated via vectorisation.

**Semantic similarity**
: measure of relatedness between two concepts. For example: bone fracture and broken bone are the same.

**Vectorisation**
: numerically representing text in an embedding model. For example: hello and hi may be numerically close.

However, there is an absence of embedding models available which captures patient-generated texts hindering secondary research use.
Some clinically relevant models are available and valuable for the clinical domain but not fully exploited and systematically compared to patient text.

Both clinical and patient text cover a wide range of medical-related concepts and relatedness, such as chronic severe inflammatory conditions to less intense acute incidents.
Three objectives can build upon a solution: 1) using a preexisting model derived from clinical text (it is difficult to access clinical records).
2) Train a model solely consisting patient-generated text. 3) Retraining the existing clinical model with the patient text.

These three will let us see semantics in 1) the clinician, 2) the patient, and 3) both semantically.
My investigations included a combination of manual evaluation, clustering, and semantic analysis.

### Chapter 3

Inflammatory Bowel Disease (IBD) is characterised as a chronic, non-infectious, autoimmune, digestive, inflammatory disease.
Patients who have IBD learn to live with their disease, specifically to control their inflammation.
There are numerous methods to manage their condition - including medical treatments, maintaining a strict diet, or stop smoking.
IBD can severely affect QoL and so takes a toll on the emotional wellbeing of the patient.

For these patients, their biomarkers may be stable due to the regulation of their disease.
For those who do not-yet have a diagnosis or having an episode, their intestinal inflammation may be active and so causing many symptoms.
To diagnose, there are rigorous investigations, however, very invasive and can take years.

One solution for better diagnostic methods is looking into blood tests, since they are preferred by the patient and less invasive.
For IBD, there is a need for identifying novel blood biomarkers as many GPs only refer patients for further tests if there is an elevated C-reactive protein (CRP) or issues in a stool sample (uncomfortable for the patient). 
Although studies have investigated biomarkers for IBD, or patient questionnaires, there lacks a bridge between the two, and so I use this chapter to dive into the biology realm to look at blood biomarkers and the relationship with a patient's emotional wellbeing.

The data I have access to has an enrolment date questionnaire for patients, blood measurements, and hospital records.
These hospital records have dates that can stratify patients into groups: diagnosed, and those who were not-yet diagnosed at enrolment.

My methods in this chapter explored the world of Machine learning (ML) I applied numerous clustering techniques to seek out patterns in the data.
I concluded the ML by conducting statistical analysis to observe cluster/group differences in relation to possible novel blood/QoL biomarkers: the overlaps.

**Machine learning**
: finding complex patterns in data potentially to predict an outcome.

The goal was being able to characterise and extract valuable information from clustering.
To see how blood markers and adjacent QoL markers interact but also direct improvements in the diagnosis time and diagnosis tests.

## Interesting results

+ Thesis has proven how invaluable the patient voice is.
+ Patient terms are used frequently and need to be considered in research, especially abbreviations or common misspellings.
+ Sentiment can show the role online forums play in a patient's emotional wellbeing and develop personalised therapy plans.
+ Semantics presented terms patients were using, revealing their priorities.
+ Furthermore, these terms were - in the opinion of the clinical experts - not medically relevant revealing important differences across domains.
+ Blood biomarkers had a relationship with QoL markers.
+ In those who had an abnormally high white blood cell count & CRP and unhappier, were diagnosed within 2 years on average.
+ Although we know second-hand smoking can increase your risk of IBD (Crohn's), results highlighted a relationship that maternal smoking (during pregnancy) had an impact.
+ These findings can indicate emotional changes and should be pursued.
+ Finally, my work allowed for scientific resources for secondary research use: the development of two ontologies expanded with patient-preferred terms, and a vectorisation embedding model with clinician and patient-generated texts.

A patient's experience with their chronic, inflammatory disease is complex.
This work has shown that the patient's voice, being qualitative or quantitative, in ontologies; or combined with novel biomarkers, can be investigated for improved patient outcomes and quality of life.

**The patient is the expert of their experience and their voice is indispensable to science.**

## Viva

I was very nervous leading up to the Viva; imposter syndrome was at peak.
I started to worry that I would blank at questions or forgot all my skills and couldn't complete the corrections.
One day before the Viva and I had a call from my supervisor...

> You're very enthusiastic about your work...try and enjoy it!

This is all I needed to go into the Viva with some confidence.
I felt happier knowing my supervisor saw the passion I had for my work - it gave me that extra boost. 

In a small room, in a caravan on a farm, in the middle of Swansea, on a cold day, despite heating on; I couldn't stop shivering.
The nerves, the excitement, and adrenaline.

The Viva started around 9am, I presented an overview of my thesis and then we dived into it.
At the beginning I thought the questions were intense but immediately calmed as I noticed we all enjoyed the conversations.
I had excellent discussions with both brilliant examiners, and I appreciate both their feedback and time.
The main issue discussed was that my literature review was a complete separate chapter and instead they wanted it integrated into the introduction with some additional methods.
They eventually winded down the conversations and told me to wait for a few minutes whilst they had a private chat.

I was recalled. Hearing that I passed made the biggest lump in my throat.
They congratulated me and we all ended the call. 12pm. 
I burst into tears.
I genuinely do believe that my life's work had triumphed. I made it. I was a Dr in Philosophy.

I went to the caravan door, where my partner was waiting for me. I was still crying - a complete mess.
He thought it went bad as he saw the tears and all I could get out, "it...went...so...good".
And then for the first time in my life, I ate some meat and cheeses to celebrate.
I had 3 months of minor corrections, and they were completed/approved before the 2022 Winter holidays.
The photograph below (left) is immediately post-Viva with the celebration cake my partner decorated.

| Post-Viva celebration | PhD award |
| -------- | ------- |
| {{< figure src="/academia/post-viva-cake.jpg" width=400 alt="me immediately post viva with my celebration cake" >}} | {{< figure src="/academia/phd-award.jpg" width=400 alt="me immediately post viva with my celebration cake" >}} |

**INVESTIGATIONS INTO THE PATIENT VOICE: A MULTI-PERSPECTIVE ANALYSIS OF INFLAMMATION**

My [PhD thesis](https://etheses.bham.ac.uk//id/eprint/13244/ "PhD thesis") was made available online and it's available in the University of Birmingham's library.
With the official written feedback from the examiners and vote from my supervisor, I won "Outstanding PhD Thesis of the Year 2022" (above, right).

My graduation was in July 2023 and although it rained, it was an amazing day spent with my favourite people.

## Wrapping-up

What else have I been up to?

+ In 2019 my New Year Resolution was to try a new thing every week and a lot of these included work/PhD ([twitter thread](https://twitter.com/sap218/status/1082047398652850179 "twitter thread of all the things i did in 2019"))
+ During COVID and lockdown I got pretty good at burger flipping and dived into creative crafts
+ Post-COVID, in November: 2021 I went to York; 2022 Bath spa; 2023 Leamington Spa for famous chicken wings
+ Started my post-PhD job at the University of Oxford as a Data Wrangler/Data Scientist and moved to Oxford!
