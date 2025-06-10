# A complete sequence of zebrafish reference genome
## About the author
  <figure>
   <div align="center">
   <img src="javanokendo.jpeg" width="400" height="400" alt="image explanation"/>
   <figcaption></figcaption> 
   </figure>
Javan Ochieng Okendo achieved a significant milestone by providing the first complete and gapless sequence of the zebrafish reference genome. This advancement represents a major breakthrough in zebrafish genomics, as it overcomes the limitations of previous assemblies, such as the widely used GRCz11 reference genome, which contained gaps and unresolved regions. By delivering a highly accurate and contiguous genome assembly, this new reference genome serves as a valuable resource for the entire zebrafish research community. It enhances our ability to identify previously undetected genes and genetic variants, which were missing in earlier versions due to sequencing and assembly constraints. This improved genomic framework will facilitate functional genomics studies, comparative evolutionary research, and precision genetic engineering, thereby advancing zebrafish as a model organism in biomedical and developmental biology. Furthermore, it will accelerate discoveries in areas such as disease modeling, regulatory genomics, and evolutionary biology, ultimately benefiting a wide range of scientific disciplines.

### Genome assembly
We used a powerful genome assembly tool called Verkko to piece together the complete zebrafish genome. This process combined two types of long DNA sequencing data: PacBio HiFi reads (25× coverage) and ultra-long Oxford Nanopore (ONT) reads (300× coverage, each at least 100,000 bases long). The result was a highly accurate 1.4 billion base-pair genome. Over half of the chromosomes were assembled from end to end (telomere-to-telomere) on the first attempt. For the remaining chromosomes, which contained complex repetitive regions (tangles), we used the ultra-long ONT reads to resolve these areas. We also applied a semi-manual method to clean up the most difficult regions. To do this, we re-aligned the long ONT reads using a tool called GraphAligner, which helped us trace the correct paths through the tangled regions. We then fed these reads back into Verkko to fill the remaining gaps and finalize the assembly. All the scripts and tools used for this work are openly available here:
👉 https://github.com/Jokendo-collab/T2T_Zebrafish

### Data downloads
- Genome assembly annotation file can be grabbed from [GRCz12tu](https://www.ncbi.nlm.nih.gov/datasets/genome/?taxon=7955).
- PacBio long reads RNAseq data can be downloaded from [here](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1232602)


