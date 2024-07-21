---
title: "Masters Dissertation"
date: 2018-10-02
toc: true
categories: ['masters','python','bioinformatics']
---

# Metagenomics of Acid Soil: a study of Nanopore long-reads and Acidobacteria

**tl;dr**: developed a `Python` package to classify unclassified Acidobacteria, [`acidoseq`](https://github.com/sap218/acidoseq "acidoseq git repository") - check out a [summarised version](https://github.com/sap218/misc/blob/master/acidoseq.pdf "acidoseq preprint") of the dissertation.

Since I enjoyed my [Summer Bioinformatics research position]({{< ref "bioinformatics-project" >}} "bioinformatics blog") (2017), for my Masters dissertation I hoped to work with [Amanda Clare](https://www.aber.ac.uk/en/cs/staff-profiles/listing/profile/afc/ "Amanda Clare staff profile") again.

Amanda spoke to the same research group, who had new sequences for me to look at.
These reads were derived using Nanopore sequencing from Aberystwyth soil.
The output includes ~2 million sequences: made of `ACGT` basepairs.

## Week 1
**Acidobacteria** is a phylum of bacteria belonging in the bacteria kingdom. It was only recognised in 2012 despite the most abundant and diverse on Earth soils.
It has been observed in mines, soils, and metal-contaminated soils; coincidently there are metal mines near Aberystwyth that have contaminated the Rheidol streams possibly resulting in metal contaminated soils.

## Week 2
Amanda and I discussed looking into a variety of tools for demographics of the data: read count, quality, and time-yield plots.
We also discussed using [`BLAST`](https://pubmed.ncbi.nlm.nih.gov/2231712/ "BLAST") to look at any present species.

I used [`Kaiju`](https://www.nature.com/articles/ncomms11257 "Kaiju") and found that Acidobacteria was present with a major subset classified as "unclassified" (not yet placed in a class group/subdivision).
Furthermore, the `GC` content of the genomes are consistent within their subdivisions.
For example: in subdivision 3 the `GC` content for those species will have the same `GC` coverage.
Subdivisions are also dependent on pH, e.g. a pH of 4 means subdivision 1, 2, 3, and 13 will be more likely to appear.

## Week 3
Amanda and I discussed finding a way to extract the Acidobacteria sequences which `Kaiju` classified. 
Despite `Kaiju` providing an output with annotated sequence IDs, we can't determine which are Acidobacteria due to absence of taxonIDs.

This is where the idea of **`acidoseq`** emerged: using a `Kaiju` output file with a list of Acidobacteria taxonomy IDs and merge.

## Week 4
As mentioned, literature highlighted that `GC` content in some subdivisions were consistent.
I downloaded the full and partial genomes of Acidobacteria and found that the `GC` content were somewhat consistent in all subdivisions.

To expand on `acidoseq` it was discussed to include a way `GC` content in Acidobacteria sequences could be investigated for patterns and plotting subdivisions.

## Week 5
We found that the `BLAST` job of the 2 million reads took a month to process only 400,000. Amanda recommended [`Blast2Go`](https://academic.oup.com/bioinformatics/article/21/18/3674/202517 "Blast2Go") that runs locally and looks at the genes in further detail.

## Week 6
Using `Blast2Go` meant we were able to create a database of Acidobacteria genomes and run a local `BLAST` to find the sequences which identified as Acidobacteria.
In `acidoseq`, I included the ability to look at `AT` comparing `GC` content (high `AT` suggests unstable DNA).

## Week 7
I added a feature to `acidoseq` that outputs subdivisions of sequences which have that particular `GC` content.

## Week 8
Amanda and I discussed assembly: building up the sequences into larger ones. Amanda suggested the tool, [`Miniasm`](https://academic.oup.com/bioinformatics/article/32/14/2103/1742895 "Miniasm").

## Week 9
The assembly job with `Miniasm` was unsuccessful: due to soil being diverse, the output didn't build up larger sequences. The largest being only 16,000 base-pairs long.

## Week 10
I started to expand `acidoseq` into a usable tool for the scientific community and looked into command line options with `Click` and how I would package with `PIP`.

## Week 11
I filtered the data to have at least a quality score of 12 and read-length of 2500: 89 reads.
We decided to use `Blast2Go` to do a final run and look into the genes.
The output for Acidobacteria was annotated with the [Gene Ontology](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-9-S5-S2 "Gene Ontology"), however, due to lack of time I didn't have time to explore the results.
For the final two weeks the time was mostly focused on writing up my dissertation.

## Week 12
During my final meeting, Amanda and I discussed corrections, and she provided great feedback. Three days later, I submitted!

## Wrapping-up

The tool I developed, **`acidoseq`**, was packaged up and made available on [GitHub](https://github.com/sap218/acidoseq "acidoseq git repository"). 

My Masters is complete and it feels great! The [dissertation](https://github.com/sap218/misc/blob/master/postgraduate_dissertation.pdf "masters dissertation") is available to read and includes more information!
A [summarised version](https://github.com/sap218/misc/blob/master/acidoseq.pdf "acidoseq preprint") is also availale (the aim was to publish, which unfortunately we didn't find the time to complete).

I had such fun with this project that I made a Twitter bot, [`acidobot`](https://twitter.com/acido_bot "discontinued acidobot twitter bot"), that dispenses facts about Acidobacteria once a day! ***discontinued***

**I would like to thank** my supervisor [Amanda](https://twitter.com/afcaber "Amanda's Twitter") for providing such a fun research experience and [Arwyn Edwards](https://twitter.com/arwynedwards "Arwyn's Twitter") and team for the intellectual engagement and access to data.

After submission, I only had 4 days until the start of my PhD. Almost a year after submitting my Masters dissertation...I had my Masters graduation!

{{< figure src="/aberystwyth/msc_graduation.jpg" width=400 alt="me at my masters graduation" >}}