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

### Random Forest
Random forests (RF) are an ensemble learning method
for classification, regression and other tasks that operates by
constructing a multitude of decision trees at training time and
outputting the class that is the mode of the classes (classification)
or mean prediction (regression) of the individual trees.
In the regression problem, the weak learner always is CART.
Usually, when the subtree of CART is divided, it will find the
best feature among all the features to divide. The difference of
RF is that it firstly randomly selects some features, and then
finds the optimal feature from these features to divide. This
enhances the generalization capability of the model.
The prediction results provided by the RF as follwing:
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/RandomF/pt_rf4.png" height=100%>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/RandomF/plt_rf4.png" height=100%>
</p>

### Evaluation Criterion

Mean Absolute Error (MAE) : MAE is the average of the absolute errors between all predicted and true values, and can
visually reflect the error between them.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/MAE.png" height=100%>
</p>

Mean Square Error (MSE) : The MSE is the average of the sum of the squares of the errors between all predicted and true
values. It is a commonly used indicator for evaluating regression tasks.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/MSE.png" height=100%>
</p>

Coefficient of determination(R^2) : R^2 represents the degree of fitting of the predicted value to the curve formed by
the
true value.The closer to 1 the better the degree of fit.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/R2.png" height=100%>
</p>

Adjusted R^2 : Adjusted R^2 is an extended criterion based on R2 to solve the inaccuracy of the evaluation value caused
by the increase in the value of R^2 as the number of samples increases. If a useful variable is added to the model,
Adjusted R^2 will increase and vice versa.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/A%20R2.png" height=100%>
</p>

Median absolute error (MAD) : MAD is a robust regression assessment indicator. It is more adaptable to outliers in the
results than RMSE and MSE.
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/MAD.png" height=100%>
</p>
where median(.) represents the median value.