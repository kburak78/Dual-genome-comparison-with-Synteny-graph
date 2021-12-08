# Dual-genome-comparison-with-Synteny-graph

Steps referenced from the Tutorial on [https://cran.r-project.org/web/packages/RIdeogram/vignettes/RIdeogram.html](https://cran.r-project.org/web/packages/RIdeogram/vignettes/RIdeogram.html).
Synteny graph from H1 and H0 of Ppr.

## Plotting in R

Finished karyotype file: ../synteny/hap1/karyotype_h1_h0_Cat 

Finished synteny file: ../synteny/hap1/synteny_h1_h0.color

In R:

    human_karyotype <- read.table("karyotype.txt", sep = "\t", header = T, stringsAsFactors = F)

    gene_density <- read.table("data_1.txt", sep = "\t", header = T, stringsAsFactors = F)

    ideogram(karyotype = karyotype_dual_comparison, synteny = synteny_dual_comparison)
    convertSVG("chromosome.svg", device = "png")
