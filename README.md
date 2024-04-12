# Breast Cancer Detection using Supervised and Unsupervised methods
This is an attempt to create a breast cancer prediction model using various machine learning approaches. The goal is to classify these samples as either benign or malignant, aiding in the diagnosis of breast cancer.
#### Dataset: 
Downloaded the Breast Cancer Wisconsin (Diagnostic) Data Set from the UCI Machine Learning Repository, containing IDs, classes, and attributes.
 https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

![bsd](https://github.com/niharikaabhange/Breast-Cancer-Detection-using-Supervised-and-Unsupervised-methods/assets/73836890/caf13a87-e3a5-4aad-b73c-845084a0ec95)


#### 1. Supervised, Semi-Supervised, and Unsupervised Learning
####  Monte-Carlo Simulation
Conducted a Monte-Carlo simulation 30 times, using different learning methods, and compared their performance using various metrics. 

i. Supervised Learning
-> Trained an L1-penalized SVM using normalized data and 5-fold cross-validation to select the penalty parameter.
-> Evaluated the model's performance by calculating average accuracy, precision, recall, F1-score, and AUC for both training and test sets.
-> Plotted the ROC curve and reported the confusion matrix for one run.

ii. Semi-Supervised Learning/Self-training
-> Selected 50% of the data from each class as labeled, using the rest as unlabeled.
-> Iteratively trained an L1-penalized SVM, starting with the labeled data and progressively labeling the unlabeled data based on their distance from the SVM's decision boundary.
-> Tested the final SVM model, reporting average metrics, plotting the ROC, and detailing the confusion matrix for one run.

iii. Unsupervised Learning (k-means)
-> Ran the k-means algorithm multiple times on the training set, ignoring the true labels and assuming two clusters.
-> Labeled each cluster based on a majority poll from the closest 30 data points to each cluster center.
-> Classified test data based on proximity to cluster centers, reporting average metrics, ROC, and confusion matrix for one run.

iv. Spectral Clustering
-> Used spectral clustering with an RBF kernel to cluster the training data.
-> Did not label data based on proximity to centers but used a fit-predict method, ensuring cluster sizes reflect the original class proportions.
-> Assessed performance using standard metrics and provided detailed results for one run.

v. Method Comparison
-> Compared the results of supervised, semi-supervised, and unsupervised learning methods to understand their effectiveness in different scenarios.
