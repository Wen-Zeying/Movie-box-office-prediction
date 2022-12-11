# Movie box office prediction 
Movie box office prediction based on ensemble learning and big data analysis
## Overview
Here is a Movie box office prediction including some preprocessing modules in Movie box office prediction (e.g., Statistic, Prediction and Causal Inference),and Ensemble learning algorithm, to build a predictive model, including Gradient Boosting Decision Tree and Random Forest model, and common classification algorithm decision trees. The results show that the Gradient Boosting Decision Tree gives the best performance, of which the regression evaluation criterion R^2 is higher than 0.995. 
## Boosting
Boosting, which uses a number of weak learners to create a strong learner, is an idea widely used in Ensemble learning. The principle of the Boosting algorithm is to gve priority to the training set to give the same weight, and train a weak learner according to the training set. The flowchart of boosting method as follwing.

<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/Boosting%20flowchart.png" height=100%>
</p>

## Bagging
Bagging (Bootstrap Aggregating) uses Boostrap sampling for the training data, that is, the data is sampled back. Each time the sampled data is utilized to train a weak learner. T weak learners are obtained after T re-sampling sampling, and then a strong learner is synthesized according to the combined strategy weak learner. The flowchart of baggting method as follwing.

<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/flowchart/bagging%20flowchart.png" height=100%>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/Wen-Zeying/Movie-box-office-prediction-/main/figures/GBDT/plt_grb6.png" height=100%>
</p>
