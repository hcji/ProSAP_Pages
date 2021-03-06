# TPCA Analysis
TPCA analysis module is designed for identifying protein complexes with significant changing
 between case and control groups with melting curves as presented in Tan et al. Currently,
 TPCA analysis **cannot** identify any novel protein complexes.

## Input
Quantitative proteomics Data should be upload via *Data* menu, and click *Load proteomics*. You can upload
 multiple files in the same time. The data table can be the output of the preprocessing
 procedure. If not, please make sure the format is consistent to the example files. The data table 
 should also include *Accession* column, but do **not** select this column in the selection dialog.
 Only choose the columns including protein abundances is OK.
 
Then, please appoint each file as *group #1* and *group #2*. Next, protein complex database should be
 upload via *Data* menu, and click *Load PPI database*. We provide the database extracted from *CORUM* at
 [here](https://github.com/hcji/ProSAP/blob/master/data/TPCA/database/TPCA_TableS3_Protein_Complex.csv).
 If you want to use other database, please make sure the format is consistent to it. You can upload
 multiple files in the same time, but you can only choose one and click *Confirm* for each analysis. 
 
After that, you can click *Calc Change*, and the program will run for several miniutes. When finised,
 the protein complexes will be sorted by the significant score. You can choose one complex and click
 *Show Curve* to view the changing in different groups, and save the result table by click *Save Result*.


## Display

- *Protein complex table*: The table of changing significance the protein complexes.
    - *Complex ID*: The index of the input protein complex, which is also essential in the input table.    
    - *Complex Name*:The name of the input protein complex, which is also essential in the input table.
    - *Subunits Uniprot ID*: The Uniprot ID of each protein in the complex, which is also essential in the input table.
    - *p-value change*: The significance of the dynamic changing of the protein complex between the two groups.
    - *Avg distance change*: The average distance changing of the protein curves between subunits.
    - *TPCA Sig 1*: The score of TPCA signature of the group #1.
    - *Avg distance 1*: The average distance of the subunits of the group #1.
    - *TPCA Sig 2*: The score of TPCA signature of the group #2.
    - *Avg distance 2*: The average distance of the subunits of the group #2.    
- *Melting curve*: Display the fitted melting curve and the original data points.  