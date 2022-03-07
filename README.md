# Failure analysis of parameter-induced simulation crashes in climate models

This FAILURE_ANALYSIS_IN_CLIMATE_MODELSreadme.md file was generated on 2021-04-15 by Gioana Teora (me) and Tommaso Toso.

## General information

1. Title of Dataset: Failure analysis in climate models

2. Author Information:

	 A. Principal Investigator Contact Information
      - Name: Gioana Teora
      - Institution: Politecnico di Torino
      - Address: Corso Duca degli Abruzzi, 24 (10129), TO
      - Email: gioana.teora@gmail.com

	B. Co-investigator Contact Information
      - Name: Tommaso Toso
      - Institution: Politecnico di Torino

3. Date of data collection: Data were collected between 2021-03-18 and 2021-04-15.

4. Geographic location of data collection: Data were produced in Turin (Piedmont, Italy).
    
## SHARING/ACCESS INFORMATION

1. Licensing: These data are freely aivalable for re-use.

2. Data Source: All data/codes are available on Git Hub at the link (...).

3. Recommended Citation: The csv file "pop_failures_V2_20210319.csv" (POP stands for Parallel Ocean  Program) is a modified version (we delete some columns that we do not need for our analysis) of the dataset available at link http://archive.ics.uci.edu/ml/datasets/Climate+Model+Simulation+Crashes#. Please, to use it cite:
   "Lucas, D. D., Klein, R., Tannahill, J., Ivanova, D., Brandon, S., Domyancic, D., and Zhang, Y.:  
   Failure analysis of parameter-induced simulation crashes in climate models, Geosci. Model Dev.
   Discuss., 6, 585-623, [Web Link], 2013. [[Web Link]]".
   Furthermore, the image "Example_of_RSLS.png" (RSLS stands for Relocating safe-level SMOTE) is 
   taken by:
   "Siriseriwan W and Sinapiromsaran K 2016 The effective redistribution for imbalance dataset :
   Relocating safe-level SMOTE with minority outcast handling. Chiang Mai Journal of Science. 1 234
   46". Please, cite it if you want to re-use this image.
   Finally, in the "references.bib" you can find the list of all our quotes.
   
## DATA & FILE OVERVIEW

1. File List: 
   -  "FailureAnalysisInClimateModels_V9_20210415.Rmd": This is the Rmarkdown file which contains the code used for conducting our analysis.
   -  "FailureAnalysisInClimateModels_V9_20210415.html": The html version of "FailureAnalysisInClimateModels_V9_20210415.Rmd" which includes the R code and its output.
   -  "pop_failures_V2_20210319": The analysed data set. All information about its structure and the original version of this dataset are available at link http://archive.ics.uci.edu/ml/datasets/Climate+Model+Simulation+Crashes#.
   -  "references.bib": The bibtex file which contains all our quotes.
   -  "requirements.txt": The text file which contains the list of all specific packages that you need to excute our code.
   -  "Example_of_RSLS.png": An image that shows an example of how generating new synthetic data throughout the Relocating safe-level SMOTE technique, taken by    "Siriseriwan W and Sinapiromsaran K 2016 The effective redistribution for imbalance dataset : Relocating safe-level SMOTE with minority outcast handling. Chiang Mai Journal of Science. 1 234 46".
   
2. Additional related data collected that was not included in the current data package: To excute our code you need to download also
  - the Citation Style Language file "2d-materials.cls" from https://editor.citationstyles.org/styleInfo/?styleId=http%3A%2F%2Fwww.zotero.org%2Fstyles%2F2d-materials, which is needed for generating the html version of our analysis;
  - the "DMwR_0.4.0.tar" R package from R archive https://cran.r-project.org/src/contrib/Archive/DMwR/.

## DATA-SPECIFIC INFORMATION FOR: [FILENAME]
<repeat this section for each dataset, folder or file, as appropriate>

1. Number of variables: 

2. Number of cases/rows: 

3. Variable List: 
<list variable name(s), description(s), unit(s)and value labels as appropriate for each>

4. Missing data codes: 
<list code/symbol and definition>n

5. Specialized formats or other abbreviations used:  

## METHODOLOGICAL INFORMATION

1. Description of methods used for collection/generation of data: The analysed dataset "pop_failures_V2_20210319" is a modified version of the relating dataset publicly available at link http://archive.ics.uci.edu/ml/datasets/Climate+Model+Simulation+Crashes#. Our dataset is derived from the latter by deleting the integer number present in all the 14-th , 15-th and 16-th columns from row 362 (heading included) to the end.

2. Methods for processing the data: the aim of our research is to try to understand the relation between the probability of a simulation crash within the Parallel Ocean Program (POP2) component of the Community Climate System Model (CCSM4) and some of POP2 parameters. For this purpose, we will use some classification algorithms, namely Logistic Regression,  k-Nearest Neighbors (k-NN), Support-Vector Machines (SVM), Kernel-SVM and Random Forest, applied to the dataset "pop_failures_V2_20210319". Furthermore, since this dataset is unbalanced, we will use some sampling methods that can allow us to re-balance the dataset, i.e. Random Oversampling, SMOTE and Relocating Safe-Level SMOTE. At the end, all the generated model are tested and the results show that ths SVM classifier performs the best, regardless of the kernel or the training set used to train it.

3. Instrument- or software-specific information needed to interpret the data: The analysis is carried out on RStudio, which is an Integrated Development Environment (IDE) for R. The R version used here is 4.0.0 with platform "x86_64-w64-mingw32". To execute code you need to install all packages listed in the "requirements.txt" file and the DMwR package that you must download from the R archive https://cran.r-project.org/src/contrib/Archive/DMwR/. Remember that some of the algorithms aformentioned use some random procedure. In order to make reproducible our experiment we have fix the seed. However, we have evidence that even if the seed is fixed, if you change platform or the R version, you result can be change. However, this fact should not change the overall results.
