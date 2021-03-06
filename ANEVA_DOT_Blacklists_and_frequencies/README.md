# ANEVA-DOT occurrence frequencies
This folder contains reports from running ANEVA-DOT on different datasets. Depending on the analysis occurrence rate of ANEVA-DOT genes in general population can be used to produce black lists that exclude "commonly occurring" genes from ANEVA-DOT analysis. We recommend using a 1%-5% threshold on C6 and excluding all genes exceeding this threshold. 

Different folders correspond to specific Vg estimate source and test populations:

|Vg source dataset | Folder |Date added|
|- | - | - |
|GTEx v7 ([Ref.](https://science.sciencemag.org/content/366/6463/351.abstract)) | [ANEVA_DOT_frequencies_gtex_v7](https://github.com/PejLab/ANEVA-DOT_reference_datasets/tree/master/ANEVA_DOT_Blacklists_and_frequencies/ANEVA_DOT_frequencies_gtex_v7)|Apr. 2019|
|GTEx v8 ([Ref.](https://www.biorxiv.org/content/10.1101/786053v1.abstract)) | [ANEVA_DOT_frequencies_gtex_v8](https://github.com/PejLab/ANEVA-DOT_reference_datasets/tree/master/ANEVA_DOT_Blacklists_and_frequencies/ANEVA_DOT_frequencies_gtex_v8)|Sep. 2019|


The ANEVA variance estimates file, Vg, used for each folder is included in the folder. 

The summary files are formatted as follows:

|Index | ColumnName | Description |
|- | - | - |
|C1 | IDs | Ensembl ID|
C2 | Gene_name | Gene name|
C3 | total_tested | The number of individual samples in the dataset in which this gene was tested by ANEVA-DOT|
C4 | total_DOTs | The number of individual samples in which this gene was an ANEVA-DOT outlier under 5% FDR|
C5 | DOT_frq | The ratio between columns C4 and C3|
C6 | DOT_frq_LowerBound | Lower bound for 95% confidence interval for column C5 |
C7 | DOT_frq_UpperBound | Upper bound for 95% confidence interval for column C5 |
C8 | Is_over_1perc | This column is 1 when C6 > 0.01, that is when the lower bound for a gene appearing as ANEVA-DOT outlier is higher than 1% in GTEx population. These genes were excluded from the analysis.|
