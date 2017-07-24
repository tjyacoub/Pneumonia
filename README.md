# Pneumonia
Analysis of transcriptomic data related to the presence of bacterial vs. non-bacterial pneumonia in human patients. 

The Agg_Data file shows database manipulation merging. The key was to create a unique identifier for each sample, and merge on that ID. There are two databases for different next-generation sequencing runs (each containing ~50 samples with 60,000 features (gene expression levels). One database contains meta data concerning the quality of the experimental data. One database contains meta data about and the quality of conversion of the raw data to gene counts. And the fifth database contains meta data on the human patients (demographics, overall wellness, etc.) 

These meta databases are used for filtering data, detecting outliers, and creating custom visualizations, such as the principal component analysis with the circle size reflecting patient wellness scores. 

The PLSR file contains Partial Least Squares Regression (a linear, supervised machine learning algorithm) for prediction of pneumonia, including leave-one-out cross-validation.PLSR is used because it offers a VIP score (variable importance in projection) which is an objective measure of the predictive power for each feature. Finally, we could use the Q^2 value, which measures the prediction error in the model, to choose the most optimal number and identity of the genes to be used in the most predictive model.

