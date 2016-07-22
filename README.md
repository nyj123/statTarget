# statTarget
==============
Description
-----------------
A graphical user interface, easy to use tool provide quality control based signal correction, integration of metabolomic data from multiple batches, and the comprehensive statistic analysis for non-targeted and targeted approaches.

Link: https://cran.r-project.org/web/packages/statTarget/

The main GUI of statTarget has two basic components. The first is shift correction. It includes quality control-based robust LOESS signal correction (QC-RLSC) that is a widely accepted method for quality con trol based signal correction and integration of metabolomic data from multiple analytical batches (Dunn WB., et al. 2011; Luan H., et al. 2015).

statTarget - Shift Correction provide QC-RLSC algorithm that fit the QC data, and each metabolites in the true sample will be normalized to the QC sample. Additionally, LOESS based generalised cross-validation (GCV) would be automatically applied to avoid overfitting of the observed data, when the QCspan was set at 0 (Default value).

statTarget - Statistical Analysis provide features including Data preprocessing, Data descriptions, Multivariate statistics analysis and Univariate analysis.

Data preprocessing : 80-precent rule, glog transformation, KNN imputation, Median imputation and Minimum values imputation.
Data descriptions : Mean value, Median value, Sum, Quartile, Standard derivatives, etc.
Multivariate statistics analysis : PCA, PLSDA, OPLSDA, VIP, Random forest.
Univariate analysis : Student T-test, Shapiro-Wilk normality test and Mann-Whitney tests.
Biomarkers analysis for Clinical research : ROC, Odd ratio.


Requirements
-----------------

Dependent on R (>= 3.3.0)

Packages should be installed:
randomForest,plyr,pROC,rrcov,RGtk2,pls,gWidgets2,gWidgets2RGtk2,pdist,impute

Steps and Data Frame
-----------------
![github](https://github.com/13479776/Picture/blob/master/main_gui8.jpg "13479776")


Usage
-----------------

1 If you did not install the R software yet,you can download R >= 3.3.0  from https://www.r-project.org

2 Install the package "statTarget" at the CRAN
 
  For Windows PC, copy this code into R 
  
  > source("https://bioconductor.org/biocLite.R")
  
  > biocLite("impute")

  > install.packages("statTarget") 
  
  For mac PC, XQuartz should be installed. Download it from https://www.xquartz.org
  
  Copy this code into R
  
  > source("https://bioconductor.org/biocLite.R")
  
  > biocLite("impute")

  > install.packages("statTarget") 

4 Input data and run

Author
-----------------

Hemi Luan, hemi.luan@gmail.com

References
-----------------
Dunn, W.B., et al.,Procedures for large-scale metabolic profiling of serum and plasma using gas chromatography and liquid chromatography coupled to mass spectrometry. Nature Protocols 2011, 6, 1060-83.

Luan H., LC–MS-Based Urinary Metabolite Signatures in Idiopathic Parkinson’s Disease. J Proteome Res., 2015, 14 (1),467–478.

Luan H., Non-targeted metabolomics and lipidomics LC–MS data from maternal plasma of 180 healthy pregnant women. GigaScience 2015 4:16
