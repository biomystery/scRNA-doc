# Analysis  (Habib2017)

## PCA, Clustering and tSNE
1. find variable genes 
   * Fit `mean_counts ~ CV` using a gamma distribution on the data from all the genes 
   * Ranked genes by the extent of excess variation as a function of their mean expression. 
	 * threshold: >= 0.2 difference in CV between the empirical and the expected 
	 * mean_thranscript_count >=0.005 
2. Dimensionality reduction using PCA 
   * DGE matrix
	 * only variable genes 
	 * scaled 
	 * log 
   * `rpca function` in [R package rsvd](https://github.com/Benli11/rSVD)
   * choose most significant PCs 
	 * based on the largest eigen value gap 
3. Graph clustering 
   * input top PCs to a graph-based clustering algorithm 
	 1. compute k-NN graph 
	 2. connect nuc to nearest neightbhour 
	 3. k-NN input to Infomap algorithm 
		* `cluster_infomap function` in R 
	 4. visualization by tSNE 
		* k=100 for each full data set 
		* k=80 for human brain **subset clustering**
		  * to identify subtypes of cells 
	    * `Rtsne` package`:
		  * max-iter = 2000 
		  * disable init PCA step 
		  * `perplexity`:100 for major cluster; 60 for subcluster 
		  * coordinates only for visual (randomness in tSNE) 
4. testing for batch and technical effects 

## transcript and gene saturation analysis 
## cluster annotation, filtering,  DE and pathway analysis 

   
