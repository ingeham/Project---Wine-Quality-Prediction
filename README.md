# Project: Wine Quality Prediction

Supervised classification of white wine quality using multiple machine learning algorithms.  
Team Members: Camilla Andersson, Amalie Omholt Ellestad, Ingeborg Hamnes.

## Goal

This project explores supervised classification models’ performances on imbalanced data. The methods utilized are *k-nearest neighbours (KNN), support vector machines (SVM)* and *random forests*. Applying various modifications to these methods, the project evaluates how much the standard classification models improve when predicting the quality of white wines. The performances are evaluated and compared based on the evaluation metrics, *accuracy, F1-score, AUC ROC* and *confusion matrices*.

## Prerequisites
### Install
This project requires Python and the following Python libraries installed:
* [seaborn](https://pypi.org/project/seaborn/)
* [imblearn](https://pypi.org/project/imblearn/)
* [NumPy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [matplotlib](https://matplotlib.org/)
* [scikit-learn](https://scikit-learn.org/stable/)

It also requires to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html).

### Code
Template code is provided in the [Wine-Quality-Prediction.ipynb](https://github.com/ingeham/Project---Wine-Quality-Prediction/blob/main/Wine-Quality-Prediction.ipynb) notebook file. You will also need to download the [winequality-white.csv](https://github.com/ingeham/Project---Wine-Quality-Prediction/blob/main/winequality-white.csv) dataset file, and change the path for importing the dataset in the code.

## Description of Data
The dataset used in this project is the [USI’s Wine Quality Dataset](http://archive.ics.uci.edu/ml/datasets/Wine+Quality?fbclid=IwAR27uuowpx_0cv3ms-J0oMG26JAc3YaGToyv_Il643NFmn-USlEJhNoE1_A). This dataset contains 4898 white wines described by 12 different features. 11 of these features are input variables based on physicochemical properties: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates and alcohol. The output feature is a quality score ranging from 0 and 10. For this project, this target is classified into three categories: good (>6), bad (<5), and average (5 and 6).

## Results
The best performing KNN model achieved an F1-score of 60.8%. In comparison,  SVM with SMOTE achieved an F1-score of 64.9%, while random forest with SMOTE achieved a score of 66.2%. Consequently, KNN had the poorest performance of the three methods. In fact, the best performing KNN performed worse than all seven SVM and random forest models. The differences in F1-scores can be explained by looking at the models’ confusion matrices. Although all models frequently fail to classify samples of the minority classes, random forest with SMOTE is clearly the best at predicting these samples. For instance, the weighted KNN only manages to classify 5 samples of the “bad” class correctly, compared to 14 for the random forest with SMOTE.

## Deliverables
The project report shows the analysis of our results. <br />
The [Wine-Quality-Prediction.ipynb](https://github.com/ingeham/Project---Wine-Quality-Prediction/blob/main/Wine-Quality-Prediction.ipynb) shows the code of our project. 
