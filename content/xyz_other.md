---
title: "Features"
date: 2023-08-29
draft: true

toc: true
collapsible_toc: true

zooming_js: true
math: true
code_copy: true

#type: 'balloon'
#balloon_resources: "/about"
#balloon_img_src: '/thanks.jpg'
#balloon_circle: true

keywords:
- one
- two

categories: ['other']
---

***

# Draft blog for features

this is everything 

{{< recent-posts sortby="publishDate" limit=0 >}}

***

### Third header {#customid}

term
: definition

***

#### Icons

{{< icon vendor="feather" name="globe" link="https://sap218.uk" >}}
{{< icon vendor="feather" name="moon" >}}
{{< icon vendor="feather" name="sun" >}}
{{< icon vendor="feather" name="github" >}}
{{< icon vendor="feather" name="mail" >}}

***

#### Breadcrumbs
{{< breadcrumbs >}}

***

#### Term Cloud
{{< terms-cloud terms="categories" >}}

***

#### Figure

<!-- ![alty text](/dir/fig.jpg) -->

{{< figure src="/academia/post-viva.jpg" width="100" title="title" caption="caption" alt="if img not displayed show text" >}}

***

#### Links

[link to how to format figures](https://gohugo.io/content-management/shortcodes/#figure "alt title")

header "##" {#customid}
[link to header]({{< relref "xyz_other.md#customid" >}})

***

#### Word blocks

{{< color-block style="success" >}}
SUCCESS
{{< /color-block >}}

{{< color-block style="info" >}}
INFO
{{< /color-block >}}

{{< color-block style="warning" >}}
WARNING
{{< /color-block >}}

{{< color-block style="error" >}}
ERROR
{{< /color-block >}}

***

#### Code
Inline `code` or blocks:

```
code
```

***