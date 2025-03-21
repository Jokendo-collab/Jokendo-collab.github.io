# The complete sequence of zebrafish reference genome

In this project, we sequenced zebrafish, Danio rerio genome usong both PacBio and Oxford Nanopore  (ONT) sequencing technologies. We used both Tubingen (TU) and AB strains of zebrafish. The genomic DNA was extracted from the fibroblast and from the tissues. The data includes 25X PacBi HiFi and 300x coverage of ONT. The Raw DNA data from PacBio HiFi and ONT has been deposited on [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra) with the BioProject ID: PRJNA1159317.

### Genome assembly
We performed hybrid assembly using Verkko assembler (version 2.2) [PMID: 36797493], using 25X PacBio HiFi and 300x ONT ultra-long sequencing data (reads lengths >= 100kb), producing the final assembly of size 1.4 Gb. More than 50% of the chromosomes were telomere-to-telomere as they were resolved in during the first Verkko assembly run. The remaining chromosomes had complex tangles which were then resolved using the ONT reads of more than 100kb. A semi-manual repeat resolution strategy was employed to further resolve the tangles.  The re-alignment of the ultra-long ONT reads was done using GraphAligner v1.0.17 [PMID: 32972461], the resultant alignment graph was then used to identify the correct traversals. The reads traversing the correct paths were extracted and supplied to Verkko for gap patching. The script used to do the downstream analysis are available [here](https://github.com/Jokendo-collab/T2T_Zebrafish). 

### Data downloads
- Genome assembly annotations for the two animals can be grabbed from [NHGRI_TU_Fish6](https://submit.ncbi.nlm.nih.gov/subs/wgs/SUB14903102) and [NHGRI_TU_Fish11](https://submit.ncbi.nlm.nih.gov/subs/wgs/SUB15155178 ).
- The annotation for the two assemblies can be downloaded from here: [NHGRI_TU_Fish11](https://github.com/Jokendo-collab/Jokendo-collab.github.io/blob/main/NHGRI_Fish11.gtf.tar.gz) and [NHGRI_TU_Fish6](https://github.com/Jokendo-collab/Jokendo-collab.github.io/blob/main/NHGRI_Fish6.gtf.tar.gz)
- PacBio long reads RNAseq data can be downloaded from [here](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1232602)

## Zebrafish pangenome
The strategy we termed the “3 generations” approach. One fish from each of the 4 most commonly used zebrafish laboratory strains: TU, AB, WIK, and TL were used as the 4 “grandparents” and were short read sequenced to document all unique, identifying structural nucleotide variants [SNV] for each parent. One fish from each of the 2 grandparent pairings was used to generate pools of the 3rd generation offspring. The pooled genomic DNA from these offspring was used for both PacBio HiFi and ONT sequence. The SNV data from the grandparents is then used to separate all the reads into haplotype bins and all 4 haplotypes are resolved simultaneously using the Verkko assembler.

## About the author
  <figure>
  
   <img src="javanokendo.jpeg" width="300" height="300" alt="image explanation"/>
   <figcaption></figcaption> 
   </figure>
Javan Ochieng Okendo achieved a significant milestone by providing the first complete and gapless sequence of the zebrafish (Danio rerio) reference genome. This advancement represents a major breakthrough in zebrafish genomics, as it overcomes the limitations of previous assemblies, such as the widely used GRCz11 reference genome, which contained gaps and unresolved regions. By delivering a highly accurate and contiguous genome assembly, this new reference genome serves as a valuable resource for the entire zebrafish research community. It enhances our ability to identify previously undetected genes and genetic variants, which were missing in earlier versions due to sequencing and assembly constraints. This improved genomic framework will facilitate functional genomics studies, comparative evolutionary research, and precision genetic engineering, thereby advancing zebrafish as a model organism in biomedical and developmental biology. Furthermore, it will accelerate discoveries in areas such as disease modeling, regulatory genomics, and evolutionary biology, ultimately benefiting a wide range of scientific disciplines.
