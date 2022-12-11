# Movie box office prediction

Movie box office prediction based on ensemble learning and big data analysis

## Overview

Here is a Movie box office prediction including some preprocessing modules in Movie box office prediction (e.g.,
Statistic, Prediction and Causal Inference),and Ensemble learning algorithm, to build a predictive model, including
Gradient Boosting Decision Tree and Random Forest model, and common classification algorithm decision trees. The results
show that the Gradient Boosting Decision Tree gives the best performance, of which the regression evaluation criterion
R^2 is higher than 0.995.

## Ensemble Learning Algorithm

### Boosting

Boosting, which uses a number of weak learners to create a strong learner, is an idea widely used in Ensemble learning.
The principle of the Boosting algorithm is to gve priority to the training set to give the same weight, and train a weak
learner according to the training set.

Boosting algorithms can differ in how they create and aggregate weak learners during the sequential process. Three
popular types of boosting methods include:Adaptive boosting or AdaBoost,Gradient boosting,Extreme gradient boosting or
XGBoost.

The flowchart of boosting method as follwing.

<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/Boosting%20flowchart.png" height=100%>
</p>

### Bagging

Bagging (Bootstrap Aggregating) uses Boostrap sampling for the training data, that is, the data is sampled back. Each
time the sampled data is utilized to train a weak learner. T weak learners are obtained after T re-sampling sampling,
and then a strong learner is synthesized according to the combined strategy weak learner. The flowchart of baggting
method as follwing.

<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/bagging%20flowchart.png" height=100%>
</p>

### Gradient Boosting Decision Tree

Gradient Boosting Decision Tree (GBDT) is a machine learning technique for regression and classification problems, which
produces a prediction model in the form of an ensemble of weak prediction models, typically decision trees. GBDT uses a
forward distribution algorithm in which weak learners use only CART. The purpose of the alternate iteration of GBDT is
to find a weak learner such that the loss function is smaller than the loss function obtained by the weak learner of the
previous iteration. Therefore, it is necessary to use CART of each iteration to fit the negative gradient of the loss
function on the weak learner obtained in the previous iteration. This ensures that the overall loss of the model is
declining.The GBDT gives the best performance, of which the regression evaluation criterion R^2 is higher than 0.995.

The prediction results provided by the GBDT as follwing:
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/GBDT/pt_grb6.png" height=100%>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/GBDT/plt_grb6.png" height=100%>
</p>

### Evaluation Criterion

Mean Absolute Error (MAE) : MAE is the average of the absolute errors between all predicted and true values, and can
visually reflect the error between them.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/GBDT/MEA.png" height=100%>
</p>