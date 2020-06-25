# Use of commercially available blocking oligos to suppress hemolysis related miRNAs in a large whole blood RNA cohort

**Analyzing the effect of a multiplexed pool of blocking oligos on two groups: **

1. 16 pilot whole blood samples- paired, extracted/sequenced in same batch
2. 901 samples from large cohort of whole blood samples- 150 paired, extracted/sequenced in 11 batches


This analysis is split into 4 major steps corresponding to Figures 2-5:

1. Effect of blocking oligos on target detection (Figure 2)
    a. Percent of total reads mapping to any of the 3 targets
    b. Percent of total reads mapping to each of the 3 targets
    c. Percent of total reads mapping to each of the 3 targets OR their precursors/isomiRs
    
2. Impact of blocking oligos on global miRNA expression patterns (Figure 3)
    a. Pilot only: PCA
    b. Paired differential expression + hierarchical clustering visualized with heatmap
    c. Removal of target species --> Paired DE
    d. Comparison of log2 counts per million in unblocked libraries vs blocked libraries
    
3. Analysis of off-target effects of blocking oligos (Figure 4)
    a. Plotting non-target DE miRs analysis to determine those of "high confidence": log2FC/pvalue/CPM
    b. Pilot only: Sequence similarity of off targets compared to target sequences
    
4. Benefits of using blocking oligos during small RNA library construction (Figure 5)
    a. Increase in number of low count species in blocked libraries
    b. Pilot only: increased DE sensitivity in blocked libraries

Each main step is performed for both the pilot samples and the large cohort, for a total of 8 files describing these analyses. 
