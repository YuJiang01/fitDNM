This directory contain scripts and examples to run fitDNM

Files included in this directory:

fitDNM.R: R program which implement fitDNM and the Poisson test

EE_denovo.txt: an example de novo mutation file for input of fitDNM

fit_DNM_dat_denovo_predict_2_4_mu.lis: Example of mutation rate file

fit_DNM_dat_denovo_predict_2_4_polyphen2_table.lis: Example of Polyphen-2 file

double_saddle_point_approx_8_7_2014.R: contain R functions for saddlepoint approximation. Called in fitDNM.R 

test.txt, test.out: subset of EE_denovo.txt and result file



To run the program:

In command line
R --no-save --slave --args 156 108 EE_denovo.txt fit_DNM_dat_denovo_predict_2_4_mu.lis fit_DNM_dat_denovo_predict_2_4_polyphen2_table.lis EE_denovo.out <fitDNM.R 1>&log 2>err&



The arguments passed to fitDNM.R
nmale: # of males in the study. e.g. 156 in Example

nfemale: # of females in the study.e.g. 108 in Example 

DNMFile: file contains the De novo mutation information with title line (chr pos ref alt gene) Note: we cannot process chromosome Y now. e.g. EE_denovo.txt

gene_mu_rate_file: mutation rate for each locus. Note, the reference position is labeled as mutation rate 0. e.g. fit_DNM_dat_denovo_predict_2_4_mu.lis

gene_polyphen_file: The polyphen-2 score for all loci of genes used in analysis. (-0.001 refer to Polyphen-2 score is not availabe, synonymous mutations are coded as 3, LOF mutations are coded as 2) e.g. fit_DNM_dat_denovo_predict_2_4_polyphen2_table.lis 

resultFile : file to output results. e.g. test.out



