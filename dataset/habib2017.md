# DroNc-Seq data set 
Time-stamp: "2017-11-08 10:52:14"
## sources 
1. [GTEx](https://www.gtexportal.org/home/datasets)
   * only human @ additional datasets (Wed Nov 08 10:30:47 PST 2017, V7) and only the processed data set (`GTEx_droncseq_hip_pcf.tar`,i.e. umi_counts) 
     1. GTEx_droncseq_hip_pcf.clusters.txt 
     2. GTEx_droncseq_hip_pcf.tsne.txt 
     3. GTEx_droncseq_hip_pcf.umi_counts.txt
   * the raw data is not released yet *PHS00424.V8.P1*   
   * *The reference files could be useful*
2. [SC portal](https://portals.broadinstitute.org/single_cell)
   * [Human data (Wed Nov 08 10:28:48 PST 2017)](https://portals.broadinstitute.org/single_cell/study/dronc-seq-single-nucleus-rna-seq-on-human-archived-brain) **14693 cells** 
     1. Human_Data_for_Portal.tSNE_coordinate.txt (All clusters)
     2. Human_DroNc-seq_Regions.txt	
     3. Human_Processed_GTEx_Data.DGE.UMI-Counts.txt.gz	
   * [Mouse data (Wed Nov 08 10:26:19 PST 2017)](https://portals.broadinstitute.org/single_cell/study/dronc-seq-single-nucleus-rna-seq-on-mouse-archived-brain), **13313 cells**
     1. Mouse_Coordinates2.txt (Mouse Brain)	
     2. Mouse_Meta_Data_with_cluster.txt	
     3. Mouse_Processed_GTEx_Data.DGE.log-UMI-Counts.txt.gz	
     4. 20 fastq.gz files
3. GEO: (*no human raw Wed Nov 08 10:48:28 PST 2017*)
   * [mouse@GSE104525](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE104525) - *new, 2017-10-06*
     * [GSE104525_Mouse_Processed_GTEx_Data.DGE.UMI-Counts.txt.gz](https://www.ncbi.nlm.nih.gov/geo/download/?acc=GSE104525&format=file&file=GSE104525%5FMouse%5FProcessed%5FGTEx%5FData%2EDGE%2EUMI%2DCounts%2Etxt%2Egz)
     * 10 samples (fastq.gz) 
     * 4 mouse brain tissue on two different brain regions 
   * [mouse@GSE85721](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE85721) - *old, 2016-08-16*

No Diff in umi counts file  between human@GTEx with human@sc_protal. 

## Data list 
1. 1710 cells from  2 replicates from 3T3 cell (by Drop-seq)
2. 5636 3T3 nuclei (6 replicates) 
3. 19561 nuclei from mouse brain:
   * 4 PFC samples 
   * 4 hip samples (hippocampus) from 4 mice 
   * 8 cortical samples from 4 mice for QC experiments 
4. 19550 nuclei from human brain:
   * 3 PFC samples 
   * 4 hip samples (hippocampus) from 5 donors
   
   
   
   
