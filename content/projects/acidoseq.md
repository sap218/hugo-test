---
title: "Acidoseq"
date: 2018-11-24
categories: ['command line','masters','python','bioinformatics','tool','trends']
---

# Acidoseq

**Acidoseq** is tool for studying unclassified Acidobacteria reads from Nanopore metagenomic data.
It is a `Python` package available open-source on [GitHub](https://github.com/sap218/acidoseq "github") with a [condensed paper](https://github.com/sap218/misc/blob/master/acidoseq.pdf "condensed acidoseq paper").

This work was a part of my [Masters degree]({{< ref "masters-dissertation" >}} "masters blog") (2018), which the [dissertation](https://github.com/sap218/misc/blob/master/postgraduate_dissertation.pdf "msc dissertation") is available to read.

**The motivation** behind development of this package was due to many of Acidobacteria's recovered sequences were labelled as "unclassified".

The `GC` content of the Acidobacteria genomes are consistent with their placements.
For example, those in the subdivisions V have a `GC` content of above 60% and those in subdivisions III is roughly 10% lower.
This highlights both the diversity and patterns within the phylum[^1].

Moreover, the abundance of the subdivisions correlate with the pH.
For example subdivisions 4, 6, 7, 10, 11, 16, 17, 18, 22, and 25 are sparse in low pH and more dense as pH increases[^2].
Whereas this is the opposite for subdivisions 1, 2, 3, 12, and 13.

In order to "predict" these unclassified reads into a subdivision, **acidoseq** uses both `GC` content and soil pH levels.

**Acidoseq features** includes a plot to represent subdivisions, the `GC` content for DNA stability tests, and a map of soil pH levels in the UK.
Users need to use [`Kaiju`](https://bioinformatics-centre.github.io/kaiju/ "link to kaiju tool")[^3] which classifies metagenomes with taxon IDs: thus labelling those classified or not.

Futhermore, users need to know the pH of the soil, if unknown, there is a map plotting function which users simply input a town/city and then manually derive the pH. 
**Note**: due to the spherical Earth and maps being 2-dimensional, there is some minor distortion when plotting locations.

**Testing** included data extracted from soil in Aberystwyth. 

```
$ acidoseq --taxdumptype U --kaijufile result_seqid_taxon.csv --fastapath all.fa --style seaborn --plottype span --ph 6.25
```

Using the mapping function, I inferred soil pH levels at `6.25` (see the Figure below).

{{< figure src="/aberystwyth/acidomap.PNG" width=350 caption="**Figure**: Feature of Acidoseq to plot the UK soil pH levels." alt="map of soil pH levels in the UK" >}}

Then after running **acidoseq** on the unclassified reads, we see that many reads are divided into subdivisions 4, 6, and 22 as one would expect with this pH (see the Figure below).

{{< figure src="/aberystwyth/acidoseq.PNG" width=350 caption="**Figure**: The `GC` content and subdivison visualiation of the reads." alt="plot of GC content and subdivisions" >}}

We then ran the unclassified reads though `BLAST`[^4] to see annotations/alignments.
From the `BLAST` output, we see reads aigned to subdivisions 6 and 4: there was presence of Luteitalea pratensis (90.91%) which resides in subdivision 6 and Pyrinomonas methylaliphatogenes strain K22 which resides in subdivision 4.

## References

[^1]: Quaiser, Achim, et al. "Acidobacteria form a coherent but highly diverse group within the bacterial domain: evidence from environmental genomics." Molecular microbiology 50.2 (2003): 563-575.
[^2]: Eichorst, Stephanie A., et al. "Isolation and characterization of soil bacteria that define Terriglobus gen. nov., in the phylum Acidobacteria." Applied and environmental microbiology 73.8 (2007): 2708-2717.
[^3]: Menzel, P., Ng, K. L., & Krogh, A. (2016). Fast and sensitive taxonomic classification for metagenomics with Kaiju. Nature communications, 7(1), 11257.
[^4]: Altschul, Stephen F., et al. "Basic local alignment search tool." Journal of molecular biology 215.3 (1990): 403-410.
