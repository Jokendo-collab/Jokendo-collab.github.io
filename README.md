In this project, we sequenced zebrafish, Danio rerio genome usong both PacBio and Oxford Nanopore  (ONT) sequencing technologies. We used both Tubingen (TU) and AB strains of zebrafish. The genomic DNA was extracted from the fibroblast and from the tissues. The data includes 25X PacBi HiFi and 300x coverage of ONT. The Raw DNA data from PacBio HiFi and ONT has been deposited on [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra) with the BioProject ID: PRJNA1159317.

### Gene annotation
Did the lift off from the GRCz11 and the annotation file can be downloaded from here:
### Methylation pattern analysis
### Repeat annotation
### Variant calling and analysis
### Centromere analysis and annotation(s)
## Zebrafish pangenome
The strategy we termed the “3 generations” approach. One fish from each of the 4 most commonly used zebrafish laboratory strains: TU, AB, WIK, and TL were used as the 4 “grandparents” and were short read sequenced to document all unique, identifying structural nucleotide variants [SNV] for each parent. One fish from each of the 2 grandparent pairings was used to generate pools of the 3rd generation offspring. The pooled genomic DNA from these offspring was used for both PacBio HiFi and ONT sequence. The SNV data from the grandparents is then used to separate all the reads into haplotype bins and all 4 haplotypes are resolved simultaneously using the Verkko assembler.
