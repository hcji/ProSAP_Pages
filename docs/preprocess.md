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
- *Normlization*: 





