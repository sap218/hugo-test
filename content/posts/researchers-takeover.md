---
title: "ResearcHers Code takeover"
date: 2021-02-12
toc: true
categories: ['phd','trends']
---

{{< color-block style="info" >}}
I ran the ResearcHers Twitter account from the 8th until the 12th February 2021 - the below are Tweets I copied over and edited/shortened for the blog & update the reader.
{{< /color-block >}}

## Monday: history

Hello! I'm Samantha, and I'll be tweeting from this account for the week! I'm a 3rd year PhD student at the University of Birmingham in the UK. My field is Clinical Informatics and I am looking at inflammation! Today I’ll talk about my experience learning to code throughout education: when it started, how it progressed, and what I can do now!

I was lucky to attend a primary school with a computer suite. My first search engine was Ask Jeeves. I didn't understand what a search engine was at the time and seeing "Ask" meant I literally asked it full questions! These days Google already knows what I want to ask before I have finished typing.

The first time I encountered coding was when I was around 8 years old. A school visitor introduced us to "drag & drop" visual programming with a tool called Flowol (somewhat like Scratch). 
We started with a few exercises: shown how to drag and drop these shapes and that they make a sequence of commands.
I remember enjoying it so much that I rushed through to ensure I could try all the exercises.

We finished with a competition: we were grouped up and it was a race to solve the traffic light problem and having to consider the rules.
I remember my partner and I struggled but I didn't want to stop and so I kept working on. I remember my sequence of shapes became very complex at the end with arrows pointing everywhere, but it worked!

Our school also had a programmable floor robot. There was only one so we couldn't individually try but the teacher would show us how to run it. 
As much as I enjoyed these experiences I wouldn't cross paths with programming again until I was in college.

In college (aged 16) I decided to study IT as I enjoyed it and realised I was actually pretty good at it too.
I originally wanted to be a midwife and undertook child development and health and social care studies alongside IT. I wondered maybe there would be a way I could somehow combine healthcare and IT in my future. 

My IT course at college covered many areas, including: animation, business, and web development.
I still have the animation project available to watch - [Little Lonely Bird](https://www.youtube.com/watch?v=hrTA1cGky4o&ab_channel=SamPendleton) - the aim was the provoke emotion.

I really enjoyed the web modules. I remember our first task was to build a basic website with `HTML` and `CSS` with Adobe Dreamweaver. I still didn't have a computer at home, so I spent my evenings at school to make sure I wouldn't fall behind.
The web module is where I also met `Javascript` - although the course was not programming-focused, the teacher provided code snippets which I further explored.
When I got a laptop of my own, I tried to learn `Javascript` in my spare time. 

It was at this stage that I had to start thinking about my future: what were my career options? Did I actually want to be a midwife? Did I want to focus on IT? I found IT much easier and it was so fun. I asked my IT teacher for advice… My IT teacher strongly encouraged me to apply for computer science and to choose a university outside my hometown to gain independence and confidence.

I started my [undergraduate degree]({{< relref "undergraduate.md" >}}) at Aberystwyth University, UK, studying Computer Science in 2014. Some coding skills I learnt in my first year included: `Java`, `Arduino C`, and my old friend `Javascript`.
The CompSci department runs an activity weekend every year for all first years for various team building activities - without phone signal!

One of my first challenges as an undergrad was the introduction to Linux and the command line interface. It was nothing like I've ever done before. I stepped into this whole new computing world that included other operating systems! I had previously only ever interacted with a Windows OS.

I enjoyed - and struggled - with the `Arduino`. On the other hand, I failed `Java`: going from `Arduino C` to object-orientated `Java` was too confusing for me.
I found it hard to wrap my head around all these new concepts, I tried taking out a book or two from the library but I didn't understand it as much as I had hoped.

Due to these struggles and other great advice: it was recommended to swap over to Business IT for my second year onward, and I was happy with that decision. I found programming languages difficult yet enjoyed web building. But it was not the end of my coding experiences!

My second year modules included: web programming, system administration, and databases.
During web programming I learnt `PHP` and in databases I learnt `PostgreSQL`.
I also chose some modules outside the department as I wanted to widen my career choices.

My third year included a group project and my final dissertation. My final dissertation was creating a website for a small cake business with a database and a forum for users to talk recipes.
This is also the year I was introduced to Machine Learning. The machine learning module focused on using the Weka software.
At the end of my third year, I needed to start thinking about my next steps: I had applied for Data Science.

Over the Summer of 2017 - after undergraduate graduation - I got an student research position in [bioinformatics]({{< relref "bioinformatics-project.md" >}}) and started my `Python` journey.
With some help, I finally figured out programming - it all clicked. Despite my prevoius troubles, I finally felt like I understood a programming language with ease! 

Autumn 2017 was the start of my [Masters]({{< relref "masters-dissertation.md" >}}) in Data Science! I explored various topics: statistics; and reintroduced in machine learning and databases. I also learnt new skills: `R` and `MongoDB`.
One of my most memorable university modules was the introduction to `Python`. This was taught via lectures and practicals, both with live coding during the session and the lecturer would get us involved.
My Masters project used a varity of skills, especially `Python` looking at Acidobacteria and its DNA content - as part of this I made my first `Python` tool and released it on GitHub.

## Tuesday: PhD

One of the major topics I wanted to discuss is my PhD.

Firstly I'd like to discuss PhD applications! I've had a few questions from Masters students over the past year about PhD applications, including essays & interviews.
(Although I Tweeted some advice - in this blog it'd be best to link over to the [PhD applications]({{< relref "phd-applications.md#tips" >}}) post.)

My PhD is focused on inflammation!
I am looking into non-traditional biomarkers of inflammation through various methods & data sources: structured and unstructured.
Some non-traditional biomarkers includes blood assays or clinical letters.

My original PhD title was different: the plan was to use various Biobanks studies and link up missing gaps, however we soon learnt that the data wasn't available... 
The new aim is to work on patients in the UK Biobank, which is a long study aimed to investigate the contributions and development of a disease both genetically and environmentally.

"Creating an AI based data assistant to bridge genotype to metadata linking primary clinical data to biobank sample" - my original PhD title

To link back to yesterday and my coding experience - currently my main language is `Python`, sometimes I use `R` for statistics or plotting. At first, I struggled a lot with `Python` dictionaries but I've finally become friends with them.

## Wednesday: skills

My main interests are: machine learning, ontologies, and natural language processing!

Machine learning (ML) is "learning from data", it can be supervised prediction with labelled data or unsupervised clustering to highlight unseen relationships in data.

I'm most interested in clustering as I like to observe patterns in my data and enjoy exploring the clusters.
I've used `K-means`, `hierarchical`, `DBScan`, `spectral`, and more!
Because I work with such large datasets, I have used various dimensionality reduction methods: specifically `t-SNE` and `PCA`. An interesting tool I found is `PCAmixdata` (in `R`) essentially combining `PCA` (continuous) and `MCA` (categorical) - I would definitely recommend!

The main toolkit I use for my clustering is the `scikit-learn` module in `Python` - it also includes functionality for dimensionality reduction and methods for the optimal number of `K`.
I like to say that there's no "right way" to do machine learning - but parameter finetuning can improve results! Don't forget visualisation - it's important to see what the data looks like too.

Ontologies condense a domain of knowledge in formalised structure. The concepts of an ontology have metadata and relationships.
For example in human anatomy: hand "part of" arm [synonym = upper limb]. 

Ontologies allow us to do association text mining: we can extract important sentences from a document using terms and their corresponding synonyms. 
In relation to my PhD: I aim to look at clinical letters of patients with inflammation and look into word vectorisation: looking how terms are closely related to one-another.

If you want a way to visualise an ontology, I recommend the `WebVOWL` online tool - with interactive features!
If you are interested in NLP, I recommend `spaCy` as it has a brilliant tutorial/guide - I personally find this tool the best one for `PoS tagging` and such thus far.

My NLP work has proved difficult as many tools that exist for NLP tasks don't allow for easy ontology use and additional wrangling was needed... A first step to overcome this barrier: I developed [Jabberwocky]({{< relref "jabberwocky.md" >}})! An initial plan to plug-in an ontology for associated text mining.

Finally, I have also been dipping my toes into the genomics side of bioinformatics via genome-wide association studies (GWAS): looking into genetic variants of a group of people to observe if any variant is associated with a trait; e.g. diabetic patients could have the same variant which is associated with a particular trait of diabetes.
To be honest, this is not my strongest skill: I don't feel confident in the genetics area yet, but individuals in my lab co-created a script and shared with me!

## Thursday: struggles

One of my biggest struggles is trying to explain my methods or results to others - I'm still learning about terms that I should be using or still trying to communicate my results... An example of this is: using "feature" instead of "column" when describing data.

Writing - although I enjoy writing, my grammar is not the best...BUT it doesn't stop me from trying, and I appreciate others spending time helping me improve my work!
It started off quite difficult to accept feedback but it came from a place of embarrassment - I've learnt to value comments!

Relating to work itself, it's important for me to have some sort of IDE while programming. I like to easily run a script, tab functions, and observe my variables.
I need to "see" my output before I can continue, maybe it’s because I'm still not 100% confident in my programming skills.
I use `Spyder` for `Python` and `RStudio` for `R`.

Conferences: I'm quite nervous about conferences because I worry that I'll be aksed a question that I can't answer - but conferences are good for networking and career experiences.

Mental health! It's very important to take time for yourself and do things you enjoy!
I've had to take a day or few off in the past year because of the overwhelming stress… No matter if you're in academia or industry, you need to take care of yourself and it's important for businesses/companies to take care of their employees!
In 2018 [I wrote a blog post about witnessing my partner writing their PhD]({{< relref "outsider-perspective-of-phd.md" >}}) and I had to watch them sad, happy, angry….and now being in that position, I completely understand!

Trying to survive this pandemic has been difficult.
I'm lucky to not have my work affected as it's computational - but I still struggle.
My body aches as I don't get my daily walk into work & my back hurts from my cheap chair!
I'm too nervous to go outside because I see a lot of people not wearing masks and times are scary for me...

## Friday: funday

Hobbies! Since the pandemic I’ve started a bunch of hobbies: knitting, clay sculpting, and I also code for fun!
I have a [Colours]({{< relref "colours.md" >}}) project that's been in development for a new years: small, simple tools with the techniques I've learnt throughout the years! 

Music I listen to whilst working: I love soundtracks! Such as Tron Legacy & Interstellar... Hans Zimmer is my go-to!