# PISA and iTSA analysis

Although the experimental protocol of PISA and iTSA are different, the statistical analysis
 can be similar. ProSAP implements four different statistical methods for this purpose,
 which are t-test, Limma, edgeR, and DESeq2.

## Input
Data should be upload via *Data* menu, and select the columns which include the protein abundances.
 Meanwhile, the data table should also include *Accession* column, but do **not** select this column
 in the selection dialog. This column represents the ID of the protein, which can be uniprot id
 or/plus gene name or anything else. After input, you should appoint the samples with binary labels.
 The most simple labels can be 0 and 1.


## Parameters
- *Select methods*: Statistical method for identifying the significant proteins.  
- *Log2 transformed*: Whether the data values are transformed.  
- *Fold change threshold*: The threshold of the fold change for target identification.  
- *P-value threshold*: The threshold of the p-value for target identification.    
- *Balance data*: Whether to make the control samples and case samples balanced by randomly undersampling.  

## Display
- *Data viewer*: The data table of the upload data (before processing) and the corresponding result table (after processing).   
- *Label setting*: This panel is used for assiting the users to set the labels of the samples.  
- *Volcano plot*: The volcano plot which displays the target identification results.    
- *Heatmap*: The heatmap which displays the correlation between the samples.  
- *Barchart*: The barchart which displays the distribution of the protein abundances.  
- *PCA plot*: The scatter plot which displays the PCA results, which emphasizes variation and brings out strong pattern of the samples.  
