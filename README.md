# Gene-Expression-Classification

about the dataset:

This dataset comes from a proof-of-concept study published in 1999 by Golub et al. It showed how new cases of cancer could be classified by gene expression monitoring (via DNA microarray) and thereby provided a general approach for identifying new cancer classes and assigning tumors to known classes. These data were used to classify patients with acute myeloid leukemia (AML) and acute lymphoblastic leukemia (ALL).

Golub et al "Molecular Classification of Cancer: Class Discovery and Class Prediction by Gene Expression Monitoring"

There are two datasets containing the initial (training, 38 samples) and independent (test, 34 samples) datasets used in the paper. These datasets contain measurements corresponding to ALL and AML samples from Bone Marrow and Peripheral Blood. Intensity values have been re-scaled such that overall intensities for each chip are equivalent.

data cleaning steps:

changed the target variable from ALL, AML classes to 0 and 1
reordered and change name of the columns in train and test set
removed redundant columns named "call"
transponsed the feature space to have different genes as rows and data from different patients as columns
scaled dataset using standard scaler since the values for different gene expressions are widely different
used PCA method to reduce the number of features from 7129 to 28 most important

Training the dataset:
achieved accuracy of 73% using k-means clustering
using gaussian naive bayes, achieved accuracy of 91%
logistic regression with l1 regularization, resulted in 94% accuracy


