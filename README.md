Final Notes project WGCNA Evaluation:

The document WGCNA_comparison.pdf contains the results obtained from the analysis code. The code for the original paired WGCNA pipeline and for methods 1 to 4 was uploaded separately, each with a corresponding HTML output file, and these methods were run on both datasets as described in the analysis plan. Limma, DiffCoExp, and Glasso were implemented and evaluated in a separate script, again run separately for each dataset, and uploaded together with their corresponding HTML files. DiffCoEx was excluded from this analysis because it represents another variation of the WGCNA workflow. Since methods (1)–(5) already examine several WGCNA-based adaptations in detail, adding DiffCoEx would not have added much new insight.

Note: We recommend looking at the html files (make sure to download the images as well) instead of running the code, especially for the second dataset as some codes need 4.5 hours to run. If you still prefer running the code yourselves, please make sure to pay attention to the following: 
Due to its large size, the file: GSE62043_clean_noOutliers_20251223.RData cannot be uploaded. It's the output of the Dataset2_preprocessing file and input for all Dataset2 methods. The Dataset2 methods specifically need this file name (with the 23rd December 2025) while the output of the Dataset2_preprocessing is based on the particular day the code is run. To run the Dataset2 methods, make sure to rename the output file of the preprocessing or change the code of the preprocessing slightly to return the needed name.
Also, similarly, for the comparison of different methods with paired WGCNA on Dataset2, the file: paired_wgcna_export_GSE62043_20260102.rds (which is the output of Dataset2_paired) is crucial. You can find it on GitHub. If you do not download it, please note that the output of Dataset2_paired is named according to the day the code was run. Thus, please redate it to the 2nd of January 2026, so that the other methods get the input they are looking for.

---------------------------------------------------------------


STA426 Project Proposal (Francine Diethelm, Florian Hellwig) 

 

Our Journal Club paper discussed WGCNA on paired data. It did however not compare the results with other methods. Our plan is to perform these comparisons.   

 

What we have: WGCNA performed on the dataset GSE45238.  

We would like to perform the following methods on the same data:  

  

- Naïve WGCNA  

  -> treating the data as independent   

- WGCNA on the log ratios (WGCNA on tumour–normal differences)  

- Separate tumour vs healthy WGCNA + module preservation  

  -> Building two separate Networks on the healthy and sick samples and applying model preservation analysis  

- Pair-aware WGCNA  

  -> Using repeated-measures correlation instead of Pearson  

- Limma  

- DiffCoEx  

- Diffcoexp  

- Graphical lasso  

  

If we manage to implement it successfully, we would like to perform these methods on another, larger dataset GSE62043. Otherwise, we will find a different one. 

  

Explicit research Questions:  

- How well does WGCNA perform compared to other methods?
  
- Which method detects phenotype-associated modules most reliably?  

- Defining a ground truth 
