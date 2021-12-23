# Data Preprocessing
## Input
The input files can be upload by clicking the "Open" button. You can select one
 or multiple files at one time. If you select multiple files, you should
 guarantee the files are from the technical replicates. The output will be only one
 file which combine the quantitative information of proteins.   
 
After selecting the input files, it will ask you to choose the columns which contain
 the protein abundances. Make sure that the columns you select only include numeric
 values. All the other values will be regarded as zero. 
 
If you are processing TPP datasets including temperture information, you should input
 the corresponding tempertures in the "Temperture Setting" table. It is essential for
 the subsequent procedures. If you are processing iTSA/NPA datasets, you can ignore
 this step.
 
## Parameters
- *PSM column name*: You can select the column which indicate the number of PSM. This will
 be used for PSM filter. If you do not need the filter, keep it as *None*. 
- *PSM filter threshold*: The thershold for PSM filter. Proteins with PSM number bellow
 this number will be removed.
- *Merging metrics*: If more than one files are input, how to combine the abundances
 of the same protein in different files. If onle one file is input, ignore this.
- *Normalization*: Method for normalization. *Reference* means all the quantitative values 
 are divided by the reference sample. This is usually used for the TPP analysis; *Median*
 means normalize all the samples to the same median value. *None* means no normalization is
 applied.
- *Missing value imputation*: Method for impute missing values. *KNN* means the iterative [KNN
 method](https://academic.oup.com/bioinformatics/article/17/6/520/272365) for the imputation;
 *Zero* means all the missing values to zero are replaced to zero; *None* means no imputation are
 applied, which the protein group with missing values will be discarded in the following steps.
 If TMT-labeled quantitative method is used in your experiment, *None* is recommended. If label-free
 quantitative method is used, *KNN* is recommended.
- *Missing value filter ratio*: The cut-off threshold for missing value. If the ratio of samples
 with missing value are more than this value, the protein group will be discarded.
- *RSD filter threshold*: If you have technical replicates, protein group with RSD over this threshold
 will be discarded.
- *Reference column*: If you are using *Reference* as normalization method, this is which column you are 
 used as the reference.
 
 
## Display
- *File list*: The input files for preprocessing. If you want to remove the files, please click the
 *clear* button.
- *Temperture*: The table used for input the tempertures corresponding to the samples.
- *RSD distribution*: Density plot of the RSDs of the technical replicates.
- *Data Viewer*: The output of the preprocessed data. Click *Save* to write to csv file.
 
 
 





