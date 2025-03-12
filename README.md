# The complete sequence of zebrafish reference genome

In this project, we sequenced zebrafish, Danio rerio genome usong both PacBio and Oxford Nanopore  (ONT) sequencing technologies. We used both Tubingen (TU) and AB strains of zebrafish. The genomic DNA was extracted from the fibroblast and from the tissues. The data includes 25X PacBi HiFi and 300x coverage of ONT. The Raw DNA data from PacBio HiFi and ONT has been deposited on [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra) with the BioProject ID: PRJNA1159317.

#### _Commonly used model systems in molecular biology_
![image](https://github.com/user-attachments/assets/5e952195-ff0f-4e67-8025-a1df0846c81e)

### Genome assembly
We performed hybrid assembly using Verkko assembler (version 2.2) [PMID: 36797493], using 25X PacBio HiFi and 300x ONT ultra-long sequencing data (reads lengths >= 100kb), producing the final assembly of size 1.4 Gb. More than 50% of the chromosomes were telomere-to-telomere as they were resolved in during the first Verkko assembly run. The remaining chromosomes had complex tangles which were then resolved using the ONT reads of more than 100kb. A semi-manual repeat resolution strategy was employed to further resolve the tangles.  The re-alignment of the ultra-long ONT reads was done using GraphAligner v1.0.17 [PMID: 32972461], the resultant alignment graph was then used to identify the correct traversals. The reads traversing the correct paths were extracted and supplied to Verkko for gap patching.

### Supporting data
PacBio long reads RNAseq data can be downloaded from [here](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1232602)

## Zebrafish pangenome
The strategy we termed the “3 generations” approach. One fish from each of the 4 most commonly used zebrafish laboratory strains: TU, AB, WIK, and TL were used as the 4 “grandparents” and were short read sequenced to document all unique, identifying structural nucleotide variants [SNV] for each parent. One fish from each of the 2 grandparent pairings was used to generate pools of the 3rd generation offspring. The pooled genomic DNA from these offspring was used for both PacBio HiFi and ONT sequence. The SNV data from the grandparents is then used to separate all the reads into haplotype bins and all 4 haplotypes are resolved simultaneously using the Verkko assembler.
