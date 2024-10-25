---
title: "Hello World"
date: 2023-12-11
categories: ['command line','web development']
---

# Version 3 has been released

I started this website journey around 2015 for university assignments: writing blogs for modules.
I decided to create my own `CSS` and `index` page to better structure my work.
In 2021, midway through my PhD, I progressed onto GitHub pages with `Bootstrap` and a terrible repo structure.
Now in 2023, I’ve decided to try [**`Hugo`**](https://gohugo.io/ "Hugo website"). 

A few months ago, with COVID, I decided to revamp the site and intended to go with the markdown-file route.
Whilst ill with the decision to improve the blog, I had some time off work, so my 5-day isolation weekend turned *somewhat* productive.

With the exception of some commands, `Hugo` uses markdowns allowing for many automated features.
My goal was this to be **simple**. I didn't want to wrangle with `HTML` or design.
To start, I spent hours looking at the [theme list](https://themes.gohugo.io/ "full list of Hugo themes") - choosing tags/categories that were most important to me.

The design was a toughie. Many themes I explored were great, others relied on dependencies, and in the end, I was looking for something quite minimalistic.
I finalised on [**`Monochrome`**](https://github.com/kaiiiz/hugo-theme-monochrome.git "monochrome git repository") as I liked the minimalistic design and responsiveness.
Though a top contender was [`PaperMod`](https://github.com/adityatelange/hugo-PaperMod "papermod git repository"). 

After some playing around with the `Hugo` features - thinking perhaps this was overly complicated for my purpose - I've come to appreciate the autonomy and usability.
For example, I won't need to create any search features as it's automatic.

Below are the only commands I needed to set up this page:
```
hugo new site [NAME]
cd [NAME]
git init
git submodule add https://github.com/kaiiiz/hugo-theme-monochrome.git themes/mono
echo "theme = 'mono'" >> hugo.toml
hugo new content posts/hello-world.md
```
Then run with **`Hugo server`** - adding parameter `-D` to see my drafts.

## Where have I been? {#where}
My last blog post was in 2022 and before that 2021. I have a *not-so-great* habit of starting a project, become invested, and then when I aim to write-up: I lose the energy.
I'd like to find more time to post about projects, work, or more.

So where was I this past year? 
I completed my PhD! Now officially a **Doctor in Clinical Informatics**. I aim to write-up the PhD: experience, Viva, and corrections. 
My graduation was in July, my family visited Birmingham for the first time and although it rained, it was an amazing day spent with my favourite people.

{{< figure src="/other/where-am-i.jpg" width="450" alt="me sitting on an elephant bench in royal Leamington Spa" >}}

Even bigger news is that I've officially moved to Oxford! 
Throughout 2023 I have been living in a caravan on a Farm in Swansea, saving, to make the big leap and move closer to work.
I’ve been at my current job since 2022, Data wrangler/scientist at the Big Data Institute, the University of Oxford.
**Stay tuned for *hopefully* more content!**