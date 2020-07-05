# Donor-Choose-Project-Data-Science
This is for the assignments of Applied AI Online Course

## Project Background


The project started with and details can be found in below:
https://www.donorschoose.org/donors/search.html

DonorsChoose.org receives hundreds of thousands of project proposals each year for classroom projects in need of funding. Right now, a large number of volunteers is needed to manually screen each submission before it's approved to be posted on the DonorsChoose.org website.
Next year, DonorsChoose.org expects to receive close to 500,000 project proposals. As a result, there are three main problems they need to solve:
How to scale current manual processes and resources to screen 500,000 projects so that they can be posted as quickly and as efficiently as possible
How to increase the consistency of project vetting across different volunteers to improve the experience for teachers
How to focus volunteer time on the applications that need the most assistance
The goal of the competition is to predict whether or not a DonorsChoose.org project proposal submitted by a teacher will be approved, using the text of project descriptions as well as additional metadata about the project, teacher, and school. DonorsChoose.org can then use this information to identify projects most likely to need further review before approval.


There are some other Kaggle competitions on the very same dataset :

https://www.kaggle.com/c/donorschoose-application-screening
https://www.kaggle.com/donorschoose/io



## Model Solution

### For each assignment, pre-processing has been done on text using methods like TFIDF. Below features then have been chose to train the model:

Set 1: categorical, numerical features + project_title(BOW) + preprocessed_essay (BOW)
Set 2: categorical, numerical features + project_title(TFIDF)+ preprocessed_essay (TFIDF)
Set 3: categorical, numerical features + project_title(AVG W2V)+ preprocessed_essay (AVG W2V) Set 4: categorical, numerical features + project_title(TFIDF W2V)+ preprocessed_essay (TFIDF W2V)


### Then Hyper paramter tuning to find best K
Find the best hyper parameter which results in the maximum AUC (https://www.appliedaicourse.com/course/applied-ai-course-online/lessons/receiver-operating- characteristic-curve-roc-curve-and-auc-1/) value
Find the best hyper paramter using k-fold cross validation (or) simple cross validation data
Use gridsearch-cv or randomsearch-cv or write your own for loops to do this task



## Algorithms and Models

The repo listed both .ipython and .pdf file for each below assignment. The ending number of the file shows the assignment number. For example, Com2 = compulsary 2.

Assignment Name
1 Exploratory Data Analysis   - Com1
2 T-SNE                       - Com2 
3 KNN                         - Com3
4 Naive Bayes                 - Com4
5 Logistic Regression         - Com5
6 SGD for Linear Regression   -SGD
7 SVM                         -SVM
8 Decision Tree               -DT
9 Random Forest and GBDT       -GBDT
10 K-means, Agglomerative, DBSCAN     - Kmeans
11 Truncated SVD              -TruncateSVD





##  Model Result Interpretation

Plotted the performance of model both on train data and cross validation data for each hyper
parameter, as shown in the figure.
![Image](https://github.com/wwzjustin/Donor-Choose-Project-Data-Science/blob/master/train_test_auc.JPG)


Based on the best parameter, the AUC of each model is listed:

![Image](https://github.com/wwzjustin/Donor-Choose-Project-Data-Science/blob/master/summary.JPG)
