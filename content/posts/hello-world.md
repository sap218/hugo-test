---
title: "Hello World"
date: 2023-08-29T14:45:03+01:00
draft: false
toc: false
---

# Version 3 has been released

I started this website journey around 2015 for university assignments: writing blogs for modules.
I decided to create my own `CSS` and `index` page to better structure my work.
In 2021, midway through my PhD, I progressed onto GitHub pages with `Bootstrap` and a terrible repo structure.
Now in 2023, I’ve decided to try [**`Hugo`**](https://gohugo.io/ "Hugo website"). 

COVID was the deciding factor. A few weeks ago, I decided to revamp the site and intended to choose plain markdown files.
At the same time as being ill, I also had a Bank Holiday weekend followed by some Annual Leave, so my 5-day isolation weekend turned *somewhat* productive.

With the exception of some commands, `Hugo` uses markdowns allowing for many automated features.
My goal was this to be **simple**. I didn't want to wrangle with `HTML` or design.
To start, I spent hours looking at the [theme list](https://themes.gohugo.io/ "full list of hugo themes") - choosing tags/categories that were most important to me.

The choice was a toughie. Some themes I explored were great, others relied on dependencies, and in the end, I was looking for something quite minimalistic.
A top contender was [`PaperMod`](https://github.com/adityatelange/hugo-PaperMod "papermod git repository"). 

I finalised on [**`Monochrome`**](https://github.com/kaiiiz/hugo-theme-monochrome.git "monochrome git repository") as I liked the design and responsiveness.
Although I used the 'Minimal' tag, and although I believe `Monochrome` is a minimal design, it's not under that category.

After some playing around with the `Hugo` features, thinking perhaps this was overly complicated for my purpose, I've come to appreciate the autonomy and usability.
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
Then run with **`Hugo server`** - adding parameter `-D` when this post was a draft.

## Where have I been?
My last blog was in 2022 and before that 2021 - I'd like to find more time to post about projects or work. So where was I this past year? 
I completed my PhD! Now officially a **Doctor in Clinical Informatics**. I aim to write-up the PhD: the Viva and corrections. 
My graduation was in July, my family visited Birmingham for the first time and although it rained, it was an amazing day spent with my favourite people.

{{< figure src="/academia/graduation.jpg" width="200" alt="me with the fancy PhD cap and gown" >}}

Even bigger news is that I’m moving to Oxford *very* soon! I've been living in a caravan for the past year, saving, to make a big leap and move closer to work.
I’ve been at my current job since 2022, Data wrangler/scientist at the Big Data Institute, the University of Oxford.
**Stay tuned!**