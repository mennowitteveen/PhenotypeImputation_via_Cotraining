# PhenotypeImputation_via_Cotraining

In silico phenotyping via co-training for improved phenotype prediction from genotype

#Summary
 
This work provides the proof-of-principle  that co-training can successfully be used to augment training datasets for improved phenotype prediction from genotype.

A beta version of the co-training pipeline can be accessed here on github
 
For a partition of the dataset into: set I = 10%, set II = 70% and set III = 20%, the results generated by our co-training pipeline can be found <a href="https://www.bsse.ethz.ch/content/dam/ethz/special-interest/bsse/borgwardt-lab/Projects/Co-training/experiment_10_70_20.tar.gz">here</a>. Some additional details about the subdirectory structure of the results are:
cv_set : this directory contains the 100 random permutations of the data into sets I, II and III. In each random fold, patients are assigned a value of {1, 2, 3} to indicate in which set they are placed
pheno_imp: contains the imputed labels in set II for all random folds. The labels are soft (not binary) becaused the Bagged predictor returns a probability of sample beloging to class 1 (migraine with aura)
random_forest: contains the final results of the hg classifier when applied to set III. The file roc_auc.csv has the the AUC scores for all the 100 random folds. Additionally, the files mean_tpr.csv and mean_fpr.csv contain the averaged values used to plot the ROC curves.
Contact damian.roqueiro@bsse.ethz.ch or menno.witteveen@bsse.ethz.ch for questions regarding usage of the pipeline or to report bugs. 

#Reference
Damian Roqueiro, Menno Witteveen, Verneri Anttila, Gisela Terwindt, Arn van den Maagdenberg, Karsten Borgwardt.
In silico phenotyping via co-training for improved phenotype prediction from genotype. 
ISMB 2015, Bioinformatics (2015) 31 (12): i303-i310.
