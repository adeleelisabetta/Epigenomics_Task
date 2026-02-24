Identification and characterization of distal regulatory elements (enhancers) in Stomach and Sigmoid Colon tissues.
By integrating ATAC-seq and Histone ChIP-seq data, I mapped the active regulatory landscape and calculated the spatial 
relationship between enhancers and protein-coding genes.

Data was retrieve from ATAC-seq and ChIP-seq (H3K27ac, H3K4me1) bigBed files from ENCODE.
Quality Control was validated using md5sum checks against ENCODE metadata.

ATAC-seq peaks were categorized by genomic location using GENCODE v24.

Isolated intergenic open regions (peaks outside the gene body) were identified.

Identified high-confidence distal regulatory elements by selecting intergenic ATAC peaks that overlap both H3K27ac and H3K4me1 marks.

To analyze the regulatory architecture of Chromosome 1, the GENCODE annotation was refined to focus on protein-coding genes (ENSG IDs) 
for feature extraction, get.distance.py was created to find the nearest gene and calculate the absolute distance (in bp) from the enhancer to the TSS, 
accounting for strand orientation, and an R script to compute the spatial distribution, in terms of mean and median.
