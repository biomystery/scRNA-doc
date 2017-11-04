# Analysis  (Habib2017 & Saurat )
## Guided pipeline
1. [Alignment](http://satijalab.org/seurat/Seurat_AlignmentTutorial.html)
2. [Clustering](http://satijalab.org/seurat/Seurat_AlignmentTutorial.html)
3. Code can be found http://satijalab.org/seurat/Seurat_AlignmentTutorial.html

## Standard clustering pipeline ([tutorial](http://satijalab.org/seurat/pbmc3k_tutorial.html))
updated: *2017-10-12*

1. Setup the Seurat Object
2. Standard pre-processing workflow
3. QC and selecting cells for further analysis
4. Normalizing the data
5. Detection of variable genes across the single cells
6. Scaling the data and removing unwanted sources of variation
7. Perform linear dimensional reduction
8. Determine statistically significant principal components
9. Cluster the cells
10. Run Non-linear dimensional reduction (tSNE)
11. Finding differentially expressed genes (cluster biomarkers)
12. Assigning cell type identity to clusters
13. Further subdivisions within cell types

## Gene detection 

## PCA, Clustering and tSNE
1. find variable genes `FindVariableGenes`
   * Fit `mean_counts ~ CV` using a gamma distribution on the data from all the genes 
   * Ranked genes by the extent of excess variation as a function of their mean expression. 
	 * threshold: `>= 0.2` difference in CV between the empirical and the expected 
	 * mean_thranscript_count `>=0.005` 
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

   
