# Use of commercially available blocking oligos to suppress hemolysis related miRNAs in a large whole blood RNA cohort

## Summary of study:
Hemolysis of red blood cells commonly occurs during RNA extraction, leading to huge quantities of RBC miRNAs detected in small RNA sequencing libraries- roughly 70% of all total reads in our samples. These miRs are generally unwanted and cause a huge waste in sequencing costs as well as reduced sensitivity- especially an issue for miRNA biomarkers, which are often expressed at miniscule levels within samples. Here, we implement and validate a commercially available (Perkin Elmer) pool of blocking oligonucleotides that targets three of the most commonly detected RBC miRNAs: miR-486, miR-92a, and miR-451a. These oligos bind completely to their target and prevent 5' ligation during library construction, effectively removing them from libraries. 

We confirm the efficacy of these blocking oligos, their specificity (i.e., off target analysis), and the improvements on sensitivty and DE that these blocking oligos provide. Importantly, we confirm the effect of blocking oligos on a large cohort of samples (n=901) which are more suseptible to batch effects, variable RNA quality, and varying levels of hemolysis than small pilot groups that have been used to evaluate blocking oligos in previous studies.

**Two sets of samples are used in our analysis:**

1. 16 pilot whole blood samples- paired, extracted/sequenced in same batch
2. 901 samples from large cohort of whole blood samples- 150 paired, extracted/sequenced in 11 batches


Prior to the analysis performed here, small RNA library construction was performed for all RNA samples. Libraries were sequenced on a HiSeq 2500, followed by standard adapter trimming, Bowtie2 alignment to hg19, and count matrix generation. All preprocessing was performed using the BaseSpace Sequencing Hub Small RNA App.


## This analysis is split into 4 major steps corresponding to Figures 2-5:

**1. Effect of blocking oligos on target detection (Figure 2)**

    a. Percent of total reads mapping to any of the 3 targets
    b. Percent of total reads mapping to each of the 3 targets
    c. Percent of total reads mapping to each of the 3 targets OR their precursors/isomiRs
    
    
**2. Impact of blocking oligos on global miRNA expression patterns (Figure 3)**

    a. Pilot only: PCA
    b. Paired differential expression + hierarchical clustering visualized with heatmap
    c. Removal of target species --> Paired DE
    d. Comparison of log2 counts per million in unblocked libraries vs blocked libraries


**3. Analysis of off-target effects of blocking oligos (Figure 4)**

    a. Plotting non-target DE miRs analysis to determine those of "high confidence": log2FC/pvalue/CPM
    b. Pilot only: Sequence similarity of off targets compared to target sequences
    
    
**4. Benefits of using blocking oligos during small RNA library construction (Figure 5)**

    a. Increase in number of low count species in blocked libraries
    b. Pilot only: increased DE sensitivity in blocked libraries

