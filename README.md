This is a course project (hw-560-project two)

### Background/requirement 

- Project Type: End to End  Data Mining Project

- Project Goal
  - Use different classifiers to create several classification models
  - Compare the predictive performance for each model. 
  - Combining the output from the models in an ensemble fashion

- Deliverables
  - Documented R Markdown Output
  - Github repository
  - Canvas submission 
  
### Dataset 

BreastCancer {mlbench} Wisconsin Breast Cancer Database

Description
The objective is to identify each of a number of benign or malignant classes. Samples arrive periodically as Dr. Wolberg reports his clinical cases. The database therefore reflects this chronological grouping of the data. This grouping information appears immediately below, having been removed from the data itself. Each variable except for the first was converted into 11 primitive numerical attributes with values ranging from 0 through 10. There are 16 missing attribute values. See cited below for more details.

Format
A data frame with 699 observations on 11 variables, one being a character variable, 9 being ordered or nominal, and 1 target class.

[,1]	Id	Sample code number
[,2]	Cl.thickness	Clump Thickness
[,3]	Cell.size	Uniformity of Cell Size
[,4]	Cell.shape	Uniformity of Cell Shape
[,5]	Marg.adhesion	Marginal Adhesion
[,6]	Epith.c.size	Single Epithelial Cell Size
[,7]	Bare.nuclei	Bare Nuclei
[,8]	Bl.cromatin	Bland Chromatin
[,9]	Normal.nucleoli	Normal Nucleoli
[,10]	Mitoses	Mitoses
[,11]	Class	Class

### Process

- Load required packages  
- Data preparation
  - the dataset is cleaned
- EDA - not required
- Modeling 
  - logistic regression - not required 
  - knn() - not required
  - naive bayes : e1071::NaiveBayes(),  klaR::NaiveBayes()
  - classification tree: caret::rpart()
    - with cross-validation (LOOCV)
  - conditional reference tree: party::ctree()
  - random forest: randomForest::randomForest(), party::cforest()
  - bagging (bootstrap aggregating): ipred::bagging() 
  - svm: e1071::svm()
  - neutral network: nnet:nnet()
  - Quadratic Discriminant Analysis: MASS::qda()
  - Regularised Discriminant Analysis: klaR::rda()
- Plot the ROC curves for each model
- Ensemble 
