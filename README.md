# Single Cell RNAseq Analysis of Tabula Muris Data
I have made all the notebooks using Kaggle kernel and they can also be viewed there.

### Dataset link - https://www.kaggle.com/aayush9753/singlecell-rnaseq-data-from-mouse-brain
* [Tabula Muris](https://tabula-muris.ds.czbiohub.org/) is a compendium of single-cell transcriptome data from the model organism Mus musculus, containing nearly 100,000 cells from 20 organs and tissues. 
* The data allow for direct and controlled comparison of gene expression in cell types shared between tissues, such as immune cells from distinct anatomical locations.
* This data consists of:
 * An expression matrix where each column corresponds to a gene (or transcript) and each row corresponds to a single cell.
 * A table of metadata describing each cell.


### 0. Theory - Introduction to single-cell RNA-seq - [Kaggle Link](https://www.kaggle.com/aayush9753/theory-introduction-to-single-cell-rna-seq?scriptVersionId=74733387) 
- Covers most of the theoretical concepts about Bulk RNA-seq, scRNA-seq and Computational Analysis.

### 1. AnnData and Preprocessing spike-ins - [Kaggle Link](https://www.kaggle.com/aayush9753/1-anndata-and-preprocessing-spike-ins) 
- Theory behind AnnData objects
- Exploring a test anndata
- Creating Anndata from the csv files in the dataset
- Preprocessing the labeling spike-ins


### 2. Quality Control in Single cell RNA-seq data - [Kaggle Link](https://www.kaggle.com/aayush9753/2-quality-control-in-single-cell-rna-seq-data) 
- Calculated the quality control metrices across cells and genes.
- Quality control in cells by removing cells with less total gene count, less unique genes and giving more spike-ins.
- Quality control in genes by removing genes which occur in less unique cells as well as those genes having less total cells.

### 3. Normalization & PCA - [Kaggle Link](https://www.kaggle.com/aayush9753/3-normalization-pca-in-single-cell-rna-seq-data#Normalizing-gene-expression) 
- Directly applying PCA on quality controlled data
- Applying CPM normalization and then PCA
- Normalizing each cell by total counts over all genes and excluding highly_expressed genes and then PCA
- Removing offending gene Rn45s and then PCA
- Final, Normalization by log1p and scaling and then PCA.

### 4. Dimensionality reduction and Clustering - [Kaggle Link](https://www.kaggle.com/aayush9753/4-dimensionality-reduction-and-clustering) 
1. Dimensionality Reduction
* tSNE
* UMAP
2. Clustering
* k-Means on tSNE
  ** Evaluating the k-means clustering
  ** Playing with No of cluster in k-means
* Graph Based Clustering Method - Louvain
  ** Tuning thr resolution parameter
* Seeing clusters in cells of a perticular sybtissue

### 5. Differential expression - [Kaggle Link](https://www.kaggle.com/aayush9753/5-differential-expression-in-single-cell-rna-seq) 
- Building intuition of differential expression
- Ttest
- Working with whole dataset using original labels - "cell_ontology_class"
- Working with whole dataset using "louvain" clusters
- Comapring to known marker genes of call classes


![](https://github.com/aayush9753/Single-cell-RNA-seq-analysis/blob/main/imgs/msb188746-fig-0001-m.jpg)

