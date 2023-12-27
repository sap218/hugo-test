---
title: "Fashun"
date: 2022-10-21
toc: true
categories: ['r','shiny','sentiment','trends']
---

# Fashun: an `R` Shiny app of fashion trends

[**>> Shiny Fashun app**](https://sap218.shinyapps.io/fashun_app/ "R Shiny fashion application")

## Introduction

I want to start by saying fashion is whatever you want it to be - whether that is wearing double demin, or two completely different patterns.

Setting the scene: I have just handed in my PhD thesis and found that there's extra free time in my evenings.
I thought, what skills can I learn in my spare time? 

I enjoy fashion. By "fashion" I mean any outfit as I find clothing an outlet to expressing oneself.
Using Google Trends, Twitter API, and `R` Shiny I created a project that looks at fashion trends, correlations, and sentiment analysis.

The Trends analysis includes correlations, seasonal trends, and possible upcoming trends.
Sentiment analysis of Twitter posts that included particular fashion terms describes and compares various fashion topic sentiments via boxplots and correlation heatmaps.

You can explore data via the interactive [`R` Shiny app I developed](https://sap218.shinyapps.io/fashun_app/ "R Shiny application of fashion trends").

{{< color-block style="info" >}}
Other than `R` for the Shiny app, I used `Python` to extract and wrangle the data.
{{< /color-block >}}


## Google Trends

I used Google's `pytrends` to collect the data using category 185 "Fashion & Style" from official category list. Date from the beginning of 2019 until July 2022.

```
from pytrends.request import TrendReq as UTrendReq 
pytrends.build_payload(values, cat=185, geo="GB-ENG", timeframe=f'2019-01-01 {date.today()}',)
```


### Trend occurances

{{< figure src="/fashun/trends/heatmap_full.png" caption="**Figure**: Correlation matrix of trend occurances between terms of interest. Green represents high correlation relationships, white neutral, and purple negative correlation. For example: earrings and necklace are highly correlation, both a fashion accessory." alt="trends correlation matrix" >}}

We can see some fashion correlations from the above matrx, such as: accessories (earrings and necklace) and seasonal (winter, coat, boots, scarf). Winter itself correlating negatively with Summer.
Correlation can infer semantics (coat and jacket) and indicate synonyms.
Some interesting correlations include a positive relationships between earrings and black; and a negative relationship between Summer and bracelet & earrings.

| High correlation  | Low correlation |
| ------------- | ------------- |
| earrings & scarf | earrings & summer |
| earrings & boots | summer & bracelet |
| earrings & black | shorts & scarf |
| bag & bracelet | sunglasses & scarf |
| winter & autumn | summer & scarf |
| summer & sunglasses | shorts & boots |
| coat & scarf | winter & summer |
| jacket & coat | summer & boots |
| winter & coat | coat & shorts |
| coat & boots | coat & sunglasses |
| winter & boots | summer & coat |
| beach & dress |  |
| jeans & trainers |  |

Below dives in deeper with two terms with correlated highly with others, summer and boots.
We can see that summer correlates positively with sunglasses, shorts, floral, dress, and beach (x > 0.5). However correlates negatively with winter, boots, coat, scarf, and interestingly earrings (x < -0.5).

On the other hand, boots correlates with scarf, coat, black, and more (x > 0.5).
Correlates low with terms that summer correlates high with.

| Summer | Boots |
| ------------- | ------------- |
| {{< figure src="/fashun/trends/heatmap_summer.png" width=200 alt="heatmap of summer correlations" >}} | {{< figure src="/fashun/trends/heatmap_boots.png" width=200 alt="heatmap of boots correlations" >}} |


### Time

{{< figure src="/fashun/trends/time_seasons.png" caption="**Figure**: Longitudinal line plot showing the trend of seasonal terms over the year." alt="seasonal terms longitudinal line plot" >}}

The above plot shows seasonal fashion over time: spring starts to trend in the new year, summer trends over longer intervals, and both autumn and winter start to trend in July (mid Summer). 

Below are specific terms and their trends both over the year (left) and a weekly average (right).
Scarf starts to trend in the autumn and peaks in December.
The foral (pattern) trends around the beginning of Summer and cardigan has no obvious trend with the exception of peaks in June/July.

| Seasonal | Weekly |
| ------------- | ------------- |
| {{< figure src="/fashun/trends/time_seasons_scarf_full.png" width=400 alt="yearly trend scarf" >}} | {{< figure src="/fashun/trends/time_seasons_scarf_weekly.png" width=400 alt="weekly trend scarf" >}} |
| {{< figure src="/fashun/trends/time_seasons_floral_full.png" width=400 alt="yearly trend floral" >}} | {{< figure src="/fashun/trends/time_seasons_floral_weekly.png" width=400 alt="weekly trend floral" >}} |
| {{< figure src="/fashun/trends/time_seasons_cardigan_full.png" width=400 alt="yearly trend cardigan" >}} | {{< figure src="/fashun/trends/time_seasons_cardigan_weekly.png" width=400 alt="weekly trend cardigan" >}} |

Below represents a visualisation of "upcoming" fashion, specifically within the Summer season, and shows trends from January 2022 to June 2022.
As expected Summer starts to become more popular as the year progresses toward Summer and a somewhat foundation to compare "Pink". 
Pink, which was fashionable in Summer 2022, steadily increased over time.

| Upcoming Summer | Upcoming Pink |
| ------------- | ------------- |
| {{< figure src="/fashun/trends/upcoming_summer.png" width=400 alt="progression trend of summer" >}} | {{< figure src="/fashun/trends/upcoming_pink.png" width=400 alt="progression trend of pink" >}} |



## Twitter API Sentiment

I used Twitter's API package `tweepy` only obtaining single tweets - excluding replies, retweets, and links. 
```
tweet_search = "lang:en -filter:links -filter:replies -filter:retweets"
```
I used `VADER` for sentiment analysis as it is a rule-based method pre-trained with tweets.

### Analysis

{{< figure src="/fashun/sentiment/boxplot_sentiment.png" caption="**Figure**: Boxplots of sentiment scores across all fashion topics." alt="sentiment scores boxplots" >}}

Looking into categories: in accessories earrings and ring have a lower average sentiment with ring being less than 0 (most neutral).
In make-up, mascara has the lowest average sentiment yet remains higher than 0.
In patterns: stripes has the lowest sentiment whereas gingham has the highest average sentiment.
Finally, in shoes we see that both heels and boots have a lower average sentiment as footwear - which we know can be uncomfortable.

| Accessories | Make-up |
| ------------- | ------------- |
| {{< figure src="/fashun/sentiment/boxplot_accessories.png" width=300 alt="..." >}} | {{< figure src="/fashun/sentiment/boxplot_makeup.png" width=300 alt="..." >}} |

| Patterns | Shoes |
| ------------- | ------------- |
| {{< figure src="/fashun/sentiment/boxplot_patterns.png" width=300 alt="..." >}} | {{< figure src="/fashun/sentiment/boxplot_shoes.png" width=300 alt="..." >}} |


## Wrapping-up

[**>> Shiny Fashun app**](https://sap218.shinyapps.io/fashun_app/ "R Shiny fashion application")

This project was fun! In future - with more time - I would need to investigate the outputs in more detail.
For example, with the Twitter API text output, I would need to properly investigate and conduct further NLP tasks on the text as some fashion terms may have pulled irrelevant information.
Although, future work on this can be difficult: as of 2023, Twitter is now X and so I don't believe I can replicate the sentiment analysis.

{{< color-block style="info" >}}
Please do have a little explore of the Fashun app and do some investigations.
{{< /color-block >}}