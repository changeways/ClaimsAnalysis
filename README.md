# PROJECT TITLE 
Claims Analysis

## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
Analysis of risks to determine if there are specific aspects of an insured risk that be used to determine if the risk has a higher probability of resulting in a claim.

## DATA
The dataset used for this project contains historical data on insurance claims, including information about the policyholders, their demographics, and other relevant features. The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/litvinenko630/insurance-claims).

## MODEL 
The purpose of the analysis was to identifty which parameters are significant within assessing the likelihood of claims with a insurance policy. To ease interpretability of the output and produced a model that clould be validated, a Decision tree was used for the analysis.

## HYPERPARAMETER OPTIMSATION
The approach to hyperparameter optimisation was to apply a grid search resulting in the following hyperparamters
criterion   gini
max_depth   None
max_features    sqrt
min_samples_leaf    10
min_samples_split   2

## RESULTS
The main learning was the impact of the subscription length with more claims in the first year and the 11 year.
The age of the vechicle (under 4 years) was the next grouping followed by drivers aged 34-50. The data set lacked any data for under 34 year old drivers, which would probably have had an impact.
