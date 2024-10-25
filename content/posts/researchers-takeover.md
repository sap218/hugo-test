---
title: "ResearcHers Code takeover"
date: 2021-02-12
toc: true
categories: ['phd','my perspective']
---

{{< color-block style="info" >}}
I ran the ResearcHers Twitter account from the 8th until the 12th February 2021 - below are Tweets I copied over and edited/shortened for the blog/reader.
{{< /color-block >}}

## Monday: history

I'm a 3rd year PhD student (2021) at the University of Birmingham, UK. My field is Clinical Informatics, and I am looking at inflammation!
Today I'll talk about my experience learning to code throughout education: when it started, how it progressed, and what I can do now!

I was lucky to attend a primary school with a computer suite. My first search engine was **Ask Jeeves**.
I didn't understand what a search engine was at the time, seeing "Ask" meant I would literally ask it full questions! 
These days Google already knows what I want to ask before I have finished typing.

I was around 8 years old when I first encountered coding.
A school visitor introduced us to "drag & drop" visual programming with a tool called **Flowol** (like Scratch). 
We started with a few exercises: arranging shapes to make a sequence of commands.
I remember enjoying it so much that I rushed through to ensure I could attempt all the exercises.

We finished with a competition: groups would race to solve the **traffic light problem** and students had to consider the rules.
My partner and I struggled but I persisted. I remember my sequence of shapes became very complex at the end with arrows pointing everywhere, but it worked!

Our school also had a **programmable floor robot**. There was only one for the school so we couldn't individually try. The teacher would show us how to run it. 
As much as I enjoyed these experiences, I wouldn't cross paths with programming again until I was in college.

In college (aged 16) I decided to study IT as realised I was actually pretty good at it (plus I enjoyed it too).
This course covered many areas of computing, including: animation, game design, business, and web development.
I still have the animation project available to anyone to watch - [Little Lonely Bird](https://www.youtube.com/watch?v=hrTA1cGky4o&ab_channel=SamPendleton "my college animation video") - the aim was the provoke emotion.

I really dived in with web lessons. We had to build a basic website with `HTML` and `CSS` with **Adobe Dreamweaver**.
I didn't have a computer at home, so I spent my evenings at school to ensure I wouldn't fall behind.
There was another web course which included some `Javascript` - the teacher provided some code snippets, which I further explored in my own time.
I vageuly recall adding a **clock** to my site.
When I got a laptop of my own, I tried to learn `Javascript` in my spare time. 

It was at this stage that I had to start thinking about my future: what were my career options?
I found IT "easy" and fun. I asked my IT teacher for advice, who strongly encouraged me to do **Computer Science** and told me to choose a university outside my hometown to gain confidence.

I started my [undergraduate degree]({{< ref "undergraduate" >}} "undergraduate blog") at Aberystwyth University, UK in 2014.
Some coding skills I learnt in my first year: `Arduino C` and `Java`.
I struggled with `Java` as going from `Arduino C` to an object-orientated language was too confusing.
But with every module, I took a book from the library to try and understand more.
One of my first challenges as an undergrad was the introduction to `Linux` and the command line interface: this was stepping into a whole new computing world.
It was nothing like I had ever done before.

My second year modules included: **web programming**, **system administration**, and **databases**.
New skills gained included: `PHP` and `PostgreSQL`.

My third year included a group project and my [dissertation](https://github.com/sap218/misc/blob/master/undergraduate_dissertation.pdf "undergraduate dissertation"). 
The disseration was a major **web project**: I developed a site for a small cake business with a database.
This is also the year I was introduced to **Machine learning** which we used the `Weka` software.
At the end of my third year, I started to think about my next steps: I decided to apply for a Masters in for Data Science.

During the Summer of 2017 - after undergraduate graduation and before my Masters - I started a research position in [bioinformatics]({{< relref "bioinformatics-project.md" >}} "bioinformatics blog").
This is also the Summer I really started to dive in `Python` - with help of course!
This is where I finally *figured out* programming: at all clicked.

Autumn 2017 was the start of my Masters in Data Science! 
I explored various topics and dived deeper into **Machine learning**, **databases**, and newly **statistics**.
This expanded my skill set with: `R` and `MongoDB`.

One of my most memorable and favourite university modules was the `Python` module.
This was taught through "live" coding sessions, which the lecturer would get us involved.

My [Masters disseratation project]({{< ref "masters-dissertation" >}} "masters blog") used a variety of skills, 
The [dissertation](https://github.com/sap218/misc/blob/master/postgraduate_dissertation.pdf "masters dissertation") involved looking at **Acidobacteria** and its DNA content.
Here I really explored my `Python` skill and developed my first `Python` tool and released it on [GitHub](https://github.com/sap218/acidoseq "link to my first python tool").

## Tuesday: PhD

**PhD applications**: over the years, I've had questions from students about PhD applications, including essays & interviews.
**Note to reader**: although I Tweeted advice, to avoid duplication you read the information in my [PhD applications]({{< ref "phd-applications.md#tips" >}} "PhD applications blog specifically tips") blog.

My **original PhD title was different**: the plan was to use various Biobanks and link metadata gaps, however, we soon learnt that the data wasn't available... 

> Creating an AI based data assistant to bridge genotype to metadata linking primary clinical data to biobank sample

The new aim is to investigate **inflammation** using the **UK Biobank**.
I am looking into non-traditional biomarkers of inflammation through various methods & data sources: structured and unstructured.
Some non-traditional biomarkers include **blood assays** and **clinical letters**.

**Note to reader**: this takeover was in 2021 (3rd year) and I have since completed my PhD! Readers can read about it [here]({{< ref "the-phd.md" >}} "the PhD blog").

To link back to yesterday about coding experience, currently my main language is `Python` but I also use `R` for statistics or making **nice plots**.

## Wednesday: skills

My main interests are: **Machine learning**, **ontologies**, and **natural language processing**!

Machine learning (ML) is "learning from data", it can be supervised prediction with labelled data or **unsupervised clustering** to reveal patterns in data.
I'm most interested in **clustering** and have experience using `K-means`, `hierarchical`, `DBScan`, `spectral`, and more!

Don't forget **visualisation** - it's important to see what the data looks like.
To visualise data with a high number of dimensions, I explored various **dimensionality reduction** methods: specifically `t-SNE` and `PCA`. An interesting tool I found is `PCAmixdata` (in `R`) essentially combining `PCA` (continuous) and `MCA` (categorical).

For all things Machine learning, I use the `scikit-learn` module in `Python` which also does statistics, dimensionality reduction, and methods for the optimal number of `K`.
I like to say that there's no "right way" to do Machine learning - but **parameter finetuning can improve results**! 

**Ontologies** condense a domain of knowledge in formalised structure. The concepts of an ontology have metadata and relationships.
For example, in human anatomy: hand "part of" arm [synonym = upper limb]. 

Ontologies help with **semantic similarity**: allowing us to do association text mining: extracting important information from a document using terms and corresponding synonyms. 
In relation to my PhD: I aim to look at **word vectorisation** of clinical letters: looking how inflammatory terms are closely related to one-another.

My work in **natural language processing** (NLP) has proved difficult as many tools don't allow for easy ontology use and so additional wrangling is needed... 
A first step to overcome this barrier: I developed [Jabberwocky]({{< ref "jabberwocky.md" >}} "jabberwocky project"), an NLP toolkit for the easy manipulation of ontologies.

If you are interested in **NLP**, I recommend `spaCy` as it has a brilliant [tutorial/guide](https://spacy.io/ "link to spacy").
Moreover, if you are interested in visualising an ontology, I recommend the `WebVOWL` [online tool](https://service.tib.eu/webvowl/ "link to webvowl, an online ontology plotting tool").

**Note to reader**: I've found `WebVOWL` to not be 100% reliable. I have since developed `Jabberwocky eyes()` [function](https://github.com/sap218/jabberwocky "link to Jabberwocky repository") for plotting ontologies.

Finally, I have also been dipping my toes into the genomics side of bioinformatics via genome-wide association studies (**GWAS**): looking into genetic variants of a group of people to observe common traits.
To be honest, this is not my strongest skill: I am not confident in genetics, but others in my lab created a script and shared with me to help!

## Thursday: struggles

One of my biggest struggles is trying to communicate my work - I'm still learning about the correct terms I should be using and how to present my results...
An example of this is: using "feature" instead of "column" when describing data.

Futhermore, I'm quite nervous about conferences because I worry that I'll be asked questions that I can't answer (relating to my struggle in communicating).
In all though, conferences are good for networking and career experiences.

Continuing with the struggle in communicating my work...Although I enjoy writing, my grammar is not the best - BUT it doesn't stop me from trying.
It started off quite difficult to accept feedback as it came from a place of embarrassment. 
Now I value comments and I appreciate others spending time reviewing my work!

Relating to work itself, it's important for me to have some sort of `IDE` while programming.
I "need to see" my variables to continue, perhaps this comes from a place of doubt as I'm still not 100% confident in my programming skills.
I use `Spyder` for `Python` and `RStudio` for `R`.

One major struggle is not specifically related to the PhD, but rather trying to survive this pandemic.
I'm lucky to not have my work affected as it's computational - but I still find it difficult.
I'm too nervous to go outside because I see a lot of people not wearing masks and times are scary for me...
My body aches as I don't get my daily walk & my back hurts from my cheap chair!

It's very important to take time for yourself and do things you enjoy!
I've had to take a day or few off in the past year because of the overwhelming stress...
No matter in academia or industry, you need to take care of yourself and businesses/companies need to take care of their employees!

The PhD is an emotional rollercoaster, in 2018 I wrote up about [witnessing my partner writing their PhD]({{< relref "outsider-perspective-of-phd.md" >}} "perspective of PhD blog") and now being in that position, I completely understand!

## Friday: funday

Hobbies! Since the pandemic I've started a bunch of hobbies: knitting, clay sculpting, and I also coding more for fun!
I have a [Colours]({{< relref "colours.md" >}} "colours project") project that's been in development for a few years: small tools developed with the techniques I've gained throughout my years in education!

Music I listen to whilst working: I love soundtracks! Such as Tron Legacy & Interstellar... Hans Zimmer is my go-to!

{{< color-block style="success" >}}
I do apologise for the wall of text! If you stuck around - thank you!
{{< /color-block >}}