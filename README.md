# MapUTR experiemntal design

To test a variant of interest, both the reference and the alternative allele were designed into
200nt oligos synthesized by Twist Biosciences. Each oligo contains a 164nt flanking sequence
centered around the variant and adaptor sequences for cloning. The oligos were then cloned
into the 3’ UTR region of the eGFP gene, whose expression is driven by the CAG promoter, in
the plasmid reporters. We introduced 3ug plasmid libraries into 15M HEK293/HeLa cells via cell
electroporation for each biological replicate, with a total number of three replicates. Total
mRNA was isolated from the cells 24h after electroporation, reverse-transcribed into cDNA, and
made into sequencing libraries through a stepwise PCR. Specifically, a unique molecular
identifier (UMI) was added to each cDNA transcript in the first round of PCR. The PCR products
were further amplified to add Illumina sequencing adaptors in the second round of PCR. A
similar stepwise PCR protocol was also applied to the plasmid DNA to generate DNA sequencing
libraries. Both DNA and RNA sequencing libraries were pooled together to be sequenced on Illumina
HiSeq 3000 PE150 or NovaSeq 6000 PE150 with 15% PhiX spike-in. For data analysis, we extracted
UMIs from each read to remove PCR duplicates. The remaining reads were aligned to the
designed reference sequences and UMIs were counted using UMItools<sup>1</sup>. UMI counts were normalized before calling functional variants using
MPRAnalyze<sup>2</sup>.


Reference

1. Smith, T., Heger, A. &amp; Sudbery, I. UMI-tools: Modeling sequencing errors in Unique
Molecular Identifiers to improve quantification accuracy. Genome Res. 27, 491–499
(2017).

2. Ashuach, T. et al. MPRAnalyze: Statistical framework for massively parallel reporter
assays. Genome Biol. 20, 1–17 (2019).


[![DOI](https://zenodo.org/badge/639880970.svg)](https://zenodo.org/doi/10.5281/zenodo.10601708)
