# Preprocess 
## barcodes
1. first 12 bp: id cell
2. next 8 bp: UMI 

## Steps 

1. Read filtering and alignment 
2. Digital gene expression 
   * barcode correction [^1],[^2]
	 * filter low reads cells/barcodes
     * <= 1bp distance to core barcodes
   * amplification bias estimate 
   * Gene counts: collapse to UMI (<= 1bp substitution distance) within sample 
   * Expression counts (# of transcripts): DGE matrix (a given gene in a given nucleus) 
   * DEG matrix normalization:
	 * scaled by total  UMI counts * mean_number_transcript_per_dataset
	 * log transformation 
	 * `RegressOut@Seurat`: regress out effects of the number of transcripts and genes detected per nucleus 
3. Gene detection and QC 
   * additional filtering the expression matrix 
	 * Nuclei should be: >= 200 detected genes and >=10,000 usable reads 
	   * cut-off is cell-type dependent 
	   * detected gene: >= 2 unique UMIs 
	 * genes were detected >=10 nuclei (keep) 
   * QC experiments have **different gene-detection thresholds**

## Ref
* Habib et al. 2017 

[^1]: Macosko, E.Z. et al. Cell 161, 1202–1214 (2015).
[^2]: Shekhar, K. et al. Cell 166, 1308–1323 (2016).
