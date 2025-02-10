# Model Card
Analysis of risks to determine if there are specific aspects of an insured risk that be used to determine if the risk has a higher probability of resulting in a claim.

## Model Description

**Input:** Insurance data set that comprises historical data on insurance policies, with a variety of information about the policyholders, their demographics, past claim history, and other pertinent features. The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/litvinenko630/insurance-claims). After initial run through the model the dataset was pruned to only include the features that contributed to the outcome.
subscription_length The duration for which the insurance policy is active.
customer_age    Age of the insurance policyholder, which can influence the likelihood of claims.
vehicle_age Age of the vehicle insured, which may affect the probability of claims due to factors like wear and tear.
region_code The code representing the geographical region of the policyholder, as claim patterns can vary regionally.
region_density  Population density of the policyholder’s region, which could correlate with accident and claim frequencies.

**Output:** The resultant model produced a classification model

              precision    recall  f1-score   support

           0       0.93      1.00      0.97     16434
           1       1.00      0.00      0.00      1144

    accuracy                           0.93     17578
   macro avg       0.97      0.50      0.48     17578
weighted avg       0.94      0.93      0.90     17578

It also identified the importance of the key features

     Feature	Importance

16      subscription_length_group_11-12   0.089228
 5      subscription_length_group_0-1     0.078053
 2      age_group_34-50                   0.072818
36      vehicle_age_group_1-2	            0.054169
35      vehicle_age_group_0-1	            0.050215
37      vehicle_age_group_2-3	            0.048432
15      subscription_length_group_10-11   0.044190


This highlighed that the significance of the subscription, the age of the insured and the age of the vechile

**Model Architecture:** 

In order to focus in the interpretability of the output the model utilises a DecisionTreeClassifier which it run through a grid search.

## Performance

The performance initially was poor, but after pruning and grouping of the source data the whole model runs in a few minutes.

## Limitations

Due to the choice of model the accruacy of the model is not as good as a alternatives, however the objective was interpretability to understand the impact of the features.
