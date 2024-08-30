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

## Year 1 (Oct 2018-)

> You don't have as much experience as I would have thought…

This was one of the first things said to me. By a postdoc. 
**Imposter syndrome** was planted and settling in for the long haul.

For the first month there was no desk available so I sat alone in the quiet room.
I felt isolated yet understood that this was just an unfortunate start to the PhD.
But I *tried* to push forward: I read papers, followed tutorials ([infamous Pizza for ontologies](https://protegewiki.stanford.edu/wiki/Protege4Pizzas10Minutes "Protege tutorial for ontologies")), and toyed with a dataset.

I wanted to prove that person wrong. I knew that statement was true on some level, I don't think we should say that to new students.

I spent the first 9 months trying my best to impress but it always felt like nothing I did was enough.
I would read about a particular method as they instructed, but then they'd say I'm wasting too much time reading and should focus on being able to run it.
Yet, when I tried presenting results, I would be questioned about every little detail (which I would've known from the reading). 
If I didn't know the smallest detail I would be berated and told I didn't know enough.

Now reflecting from experience, I would like to say that the above should not have happened.
I can understand wanting the best for a student, but I don't think shouting at them or giving contradicting instructions is fair.
This caused me to avoid the office.
I don't want to share this negativity to push people away from a PhD, but I appreciate using my platform to reflect on this.


My first-year progress review was approaching, so I met with my supervisor about the work I've been doing for the past year, and this is when things started to change...

> I'm very impressed!

And there it was - I was a little teary.
Validation that I was making progress and that I wasn't doing a bad job...in fact I was doing OK.
There were days I still felt like a burden, but I was feeling better after *finally* some positive feedback.
I would continue to second guess myself throughout the PhD but majority in good research practice.

## Year 2 (Oct 2019-)

The second year definitely followed the "second year blues" and I was a little lost in finding the story of my PhD.
Although I had multiple projects in the works, I didn't know the trajectory and how these projects connected.
But I continued on...

I was working on a cardiovascular clinical trial data to look at the effect of beta-blockers, developing an ontology for uveitis, diving into text analysis and more.
I was finally using `Python dictionaries` and discovering the world of dimensionality reduction techniques.

{{< figure src="/academia/first-seminar.jpg" width="500" alt="presenting at my first seminar on my birthday" >}}

On my birthday I [presented at my first seminar](https://twitter.com/sap218/status/1225068022483836929 "first seminar") (see photo above).
And then **COVID**.

At the beginning of March, as reports of COVID was present in the UK and rumours of university staff infected, I decided to work from home.
Not long after, the UK went into lockdown. 
My new office was a corner in my bedroom.
I become quite the "agoraphobe" and struggled to leave the house (eventually persuaded to [visit the beautiful National Botanical Garden of Wales](https://twitter.com/sap218/status/1305896697705508871)).
But a **fun fact**: as a new hobby I dived deep into creative things, such as [art]({{< ref "digitalart" >}}) and pottery. 

Although the second year started with the blues, during the Summer I found a spark in my work and headed into a direction: **Patient Voice and Inflammation**.

I discovered the story I wanted to tell and the research I wanted to explore.
This passion was to investigate the patients and their persepctives: the data they generate (e.g. forums or questionnaires), the terms they are using, their priorities, quality of life - all within the clinical domain.

I originally hoped to look at patients with all types of inflammation, but this would cover too large a topic.
So, I narrowed down to chronic, autoimmune, inflammatory disorders with an association.

## Year 3 (Oct 2020-)

We had our heading!

The course of this PhD was set. The data was curated from various sources. And so the research was ready to follow through.
This final year was stressful - I felt a lot of pressure to produce "outstanding" results, to ensure it was novel, and to start writing up.

I also enjoyed it: I really found my passion for research.
Lots of online meetings - with lots of slideshows - each week were updates of my progress and new results.
Tense conversations were had, but all to a good purpose: I was becoming a better communicator of science and I am grateful for my supervisor in trusting me with this.

### Writing-up / Year 4 (Oct 2021-May 2022)

| First day | Entering my final year |
| -------- | ------- |
| {{< figure src="/academia/first-day.jpg" width=181 alt="on my first day" >}} | {{< figure src="/academia/final-year.jpg" width=190 alt="entering my final year" >}} |

Writing-up the PhD was quite the experience.
I had heard stories from others and I previously watched my [partner complete their PhD]({{< ref "outsider-perspective-of-phd" >}} "outside perspective of PhD") and somewhat knew what was coming.

I think I'm lucky that I enjoy writing so this experience was fun for me.
I collected all my research together: methods, results, and read so much literature - all to merge as one large document.
It was like a trip down memory lane.
Toward the end, for the final discussion chapter, I started to grow tired and got a bit of writer block - the final hurdle.

The review process was tricky. Rereading the thesis **multiple** times to spell/grammer-check, etc. was exhausting.
This part was especially difficult as I didn't have much time left - I was being told my grammar wasn't the best and so panicked with the thought of needing to rewrite the whole thing.
I was a little frustrated as I had hoped to have that sort of feedback much earlier.

So with the help from my partner, we spent a lot of evenings proof-reading the thesis. Which I am forever grateful for as I know it was a huge task and burden.

**Important**: the next section is a summary of the thesis, a full version is available to [read here]({{< ref "patientvoice" >}}).
If you wish to skip, you can [click here to continue onto the Viva]({{< relref "the-phd.md#viva-sep-2022" >}}).

***

## Thesis summary

Inflammation is the body's first response to threat, generally present in many cases, and has a complex relationship with a wide range of diseases.

### Chapter 1
Uveitis and other ocular immune-mediated inflammatory diseases (IMIDs) are chronic conditions and in many cases life threatening.
Having good vision is important to our everyday lives - affecting our Quality of Life (QoL) - and these ocular IMIDs cause problems, such as pain or blurriness.
Not only is there an unmet need for capturing the patient voice and their perspective of ocular IMIDs, but these clinical terms also needed to be standardised.

We can understand the patient better when knowing the terms they are using. 
A resource of patient-preferred synonyms is online patient forum conversations; however these are inaccessible due to being unstructured.
Ontologies have previously demonstrated great success in addressing the challenge presented by unstructured text, yet current biomedical ontologies for uveitis are limited.

**Ontology**
: a domain of knowledge condensed into a machine-readable format. For example: domain = anatomy, concepts in the ontology includes: hand, arm, and relationship can be hand "part of" arm.

This chapter built an ontology for ocular IMIDs to standardise the clinical vocabulary and structure and expanded with patient-preferred synonyms.
To capture these patient synonyms, a statistical technique was applied to a forum for curation and enhancement of the ontology.
The ontology was then used for opinion mining on particular medical therapies, types of uveitis, symptoms, etc.

### Chapter 2

This chapter continued to investigate the differences between the terms clinicians and patients use.
The clinical experts and I noticed a large number of *surprising* terms that the patient used.
To better understand both the patient and clinician, semantic similarity was explored, encapsulated via vectorisation.

**Semantic similarity**
: measure of relatedness between two concepts. For example: bone fracture and broken bone are the same.

**Vectorisation**
: numerically representing text in an embedding model. For example: hello and hi may be numerically close.

I used an embedding model derived from clinical letters and retrained with patient forum conversations.
Both clinicians and patients cover a wide range of medical-related concepts and relatedness, such as chronic severe inflammatory conditions to less intense acute incidents.
My investigations included a combination of manual evaluation, clustering, and semantic analysis.

### Chapter 3

Inflammatory Bowel Disease (IBD) is characterised as a chronic, non-infectious, autoimmune, digestive, inflammatory disease.
Patients who have IBD learn to live with their disease - specifically to control their inflammation - via medical therapies, strict diets, or stop smoking and so their biomarkers may be stable due to the regulation of their disease.
To diagnose, there are rigorous investigations, however, very invasive and can take years.

For IBD, there is a need for identifying novel blood biomarkers (preferred by the patient) as many GPs only refer patients for further tests if there is an elevated C-reactive protein (CRP) or issues in a stool sample (uncomfortable for the patient). 
Furthemore, studies lack in bridging biomarkers for IBD and the patient QoL.

The data I have access to consists of hospital records for stratifying patients into groups for those at study enrollment: diagnosed and not-yet diagnosed.
My methods explored the world of Machine learning (ML) with application of numerous clustering techniques to reveal patterns in biomarkers and mapping questionnaire data.
The goal was being able to characterise and extract valuable information from clustering in hope a pattern with QoL emerged.

**Machine learning**
: finding complex patterns in data potentially to predict an outcome.

### Interesting results

+ Patient terms are used frequently and need to be considered in research, specifically abbreviations or common misspellings.
+ Observed the role online forums play in a patient's emotional wellbeing.
+ Semantics presented terms patients were using in contrast to the clinician, revealing priorities.
+ Blood biomarkers had a relationship with QoL markers - indicating emotional changes in patients should be investigated.
+ Although we know second-hand smoking can increase your risk of IBD (Crohn's), results highlighted a relationship that maternal smoking (during pregnancy) had an impact.

A patient's experience with their chronic, inflammatory disease is complex yet they are the expert of their experience and their voice is indispensable to science.

***

## Viva (Sep 2022)

I was quite nervous leading up to the Viva; imposter syndrome was at peak.
I worried about blanking at questions, forgetting what I did, or not being able to complete corrections.
One day before the Viva I had a call from my supervisor...

> You're very enthusiastic about your work...try and enjoy it!

This is all I needed for that extra confidence boost.
I was happier knowing my supervisor saw the passion I had for my work and they had no negatives. 

In a small room, at the back of a caravan, on a farm, in the middle of Swansea, on a cold day, despite the heating on: **I could not stop shivering**.
The nerves, the excitement, the adrenaline.

The Viva started around 9am, I presented an overview of my thesis and then we dived straight into it.
At the beginning I thought the questions were intense but immediately calmed as I noticed we all enjoyed the conversations.
I had excellent discussions with both brilliant examiners, and I appreciate both their feedback and time.
The main issue discussed was that my literature review was a complete separate chapter and instead they wanted it integrated into the introduction with some additional methods.
They eventually winded down the conversations and told me to wait for a few minutes whilst they had a private chat.

I was recalled. Hearing that I passed made the biggest lump in my throat.
They congratulated me and we all ended the call. 12pm. 
**I burst into tears**.
I genuinely do believe that my life's work had triumphed. I made it. I was a Doctor in Philosophy.

I went to the caravan door, where my partner was waiting for me. I was still crying - a complete mess.
He thought it went bad with the amount of tears - all I could get out within each cry, "it...went...so...good".
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

+ In 2019 my New Year Resolution was to try a new thing every week and a lot of these included work/PhD ([Twitter/X thread](https://twitter.com/sap218/status/1082047398652850179 "twitter thread of all the things i did in 2019")).
+ During lockdown I got pretty good at burger flipping.
+ In November: 2021 I went to York; 2022 Bath spa; 2023 Leamington Spa for award-winning chicken wings.
+ Started my post-PhD job at the University of Oxford as a Data Wrangler/Data Scientist and moved to Oxford! (*blog comming soon*)

{{< figure src="/academia/graduation.jpg" width="300" alt="me with the fancy PhD cap and gown" >}}