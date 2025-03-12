In this project, we sequenced zebrafish, Danio rerio genome with a number of technologies. We used both TU and AB strains of zebrafish, Danio rerio. The genomic DNA was extracted from the fibroblast and from the tissues. The data includes 25X PacBi HiFi and 300x coverage of Oxford Nanopore (ONT). The Raw DNA data from PacBio HiFi and ONT has been deposited on [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra) with the BioProject ID: PRJNA1159317.

### Gene annotation
### Methylation pattern analysis
### Repeat annotation
### Variant calling and analysis
### Centromere analysis and annotation(s)
## Zebrafish pangenome
The strategy we termed the “3 generations” approach. One fish from each of the 4 most commonly used zebrafish laboratory strains: TU, AB, WIK, and TL were used as the 4 “grandparents” and were short read sequenced to document all unique, identifying structural nucleotide variants [SNV] for each parent. One fish from each of the 2 grandparent pairings was used to generate pools of the 3rd generation offspring. The pooled genomic DNA from these offspring was used for both PacBio HiFi and ONT sequence. The SNV data from the grandparents is then used to separate all the reads into haplotype bins and all 4 haplotypes are resolved simultaneously using the Verkko assembler.
