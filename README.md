# Plasma sterols and vitamin D are correlates and predictors of ozone-induced inflammation in the lung: A pilot study

Code was generated to support the manuscript titled 'Plasma sterols and vitamin D are correlates and predictors of ozone-induced inflammation in the lung: A pilot study', published in 2023 in PLOS One. 

> Perryman A, Hye-Young H, Payton A, Rager JE, McNell EE, Rebuli ME, Wells H, Almond M, Antinori J, Alexis NE, Porter NA, Jaspers I. Plasma sterols and vitamin D are correlates and predictors of ozone-induced inflammation in the lung: A pilot study. PLoS One. 2023 May 15;18(5):e0285721. doi: 10.1371/journal.pone.0285721. PMID: 37186612. PMCID: PMC10184915.

<p align="center">
<img src = 'https://user-images.githubusercontent.com/69641855/217161264-e8f1314b-b345-43a8-a6c2-5b7f09953ce4.png' width = '600'>
</p>

Exploratory analyses using sterol and cytokine data prior to ozone exposure to predict...
  > 1. Either inflammatory or lung response class
  > 2. Investigate the role Vitmain D plays in those models

All analyses in this respository are designated by their figure number or table number in the manuscript in parantheses. In the instance that the files are unable to rendered the NBViewer link can be viewed [here](https://nbviewer.org/github/UNC-CEMALB/Ozone-exposure-is-associated-with-alterations-in-lung-and-systemic-sterol-profiles-in-healthy-and-as/tree/main/).

<br>

# 1. Data imputation
Random Forest (RF) and the Quantile Regression Imputation of Left-Censored data (QRILC) method imputation on lung function data on cell differential, sterol, and cytokine data. Imputation was run within time points, sample types, and categories.
- Predictors and subjects were filtered for at least a 25% presence within aformentioned strata.
- Values were normalized (log 10) prior to imputing and converted back to their original scales.

# 2. Responder Prediction
- Inflammatory and Lung Response Prediction (Table 6 & Table S3-S5)
  - Using the supervised machine learning method, random forest (RF), support vector machine (SVM), or K Nearest Neighbor (KNN) to predict inflammatory or lung response class (non-responder or responder) based on sterol and cytokine concentrations derived from plasma prior to ozone exposure
  - Variable importance rankings were extracted from RF models

# 3. ML Visualisations
- Confusion Matrix Figure (Figure 5)
  - Visualization of confusion matrix metrics from all supervised machine learning models tested (KNN, SVM, and RF)
- Decision Boundary Plot (Figure 6)
  - Visualization of two of the most significant predictors in lung response RF models (ie. Chol and Vitamin D) to determine how well those variables could predict lung response status
- Variable Importance Plot (not in manuscript)
  - Shows the top predictors in random forest models relative to random noise
 
# 4. Oxysterol Correlation
- Correlogram for Baseline Sterols and Post Exposure Sputum Endpoints (Figure 6)
  - Running spearman correlations to determine if there are associations between sterol plasma samples prior to ozone exposure and cytokine sputum samples after ozone exposure
  - This same analysis was further stratified by disease status


