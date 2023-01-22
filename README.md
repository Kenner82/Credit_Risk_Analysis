# Credit Risk Analysis

## Overview

Using credit card data from Lending Club, 6 different machine learning models were compared to determine which was best at predicting credit risk. As the dataset has a greater number of low-risk loans than high-risk loans, the models used a variety of techniques (oversampling, undersampling, combination sampling, and ensemble learning) to handle the unbalanced classes. 

## Results

* **Naive Random Oversampling**
  * Balanced Accuracy Score: 0.63
  * Precision: This model is highly precise when predicting low-risk users, but very imprecise when predicting high-risk users. This means that when it predicts a user is low-risk it will be correct 100% of the time, but when it predicts a user is high-risk it will only be accurate 1% of the time. 
  * Recall: This model will correctly identify 69% of low-risk users and 57% of high-risk users. 
    
    <img width="313" alt="naive_random_oversampling" src="https://user-images.githubusercontent.com/111674383/213121823-d0e3b0e9-2dc0-4489-bdd7-4cff2ce7e16e.png">
---
* **SMOTE Oversampling**
    * Balanced Accuracy Score: 0.65
    * Precision: This model is also highly precise when predicting low-risk users but very imprecise when predicting high-risk users. When it predicts a user is low-risk it will be correct 100% of the time, but when it predicts a user is high-risk it will only be correct 1% of the time. 
    * Recall: This model will correctly identify 65% of low-risk users and 66% or high-risk users.
    
      <img width="313" alt="SMOTE_oversampling" src="https://user-images.githubusercontent.com/111674383/213121847-fbad7ed5-0ce0-4044-b26c-d78f9850146f.png">
---
* **Cluster Centroid Undersampling**
  * Balanced Accuracy Score: 0.52
  * Precision: This is another model that is highly precise when predicting low-risk users but very imprecise when predicting high-risk users. When it predicts a user is low-risk it will be correct 100% of the time, but when it predicts a user is high-risk it will only be correct 1% of the time. 
  * Recall: This model will correctly identify 43% of low-risk users and 60% of high risk users.
  
    <img width="314" alt="cluster_centroid_undersampling" src="https://user-images.githubusercontent.com/111674383/213121877-10f6563b-e024-4a33-8a30-b007d5e22004.png">
---
* **Combination Sampling With SMOTEENN**
  * Balanced Accuracy Score: 0.64
  * Precision: When this model predicts that a user is low-risk, it will be correct 100% of the time. When it predicts a user is high-risk, though, it will only be correct 1% of the time. 
  * Recall: This model will correctly identify 58% of low-risk users and 70% of high-risk users.
  
    <img width="310" alt="SMOTEENN_combination_sampling" src="https://user-images.githubusercontent.com/111674383/213121906-11977aa3-7acb-43ba-9bd4-09ae41e74d32.png">
---
* **Balanced Random Forest Classifier**
  * Balanced Accuracy Score: 0.78
  * Precision: This model is also highly precise for low-risk users, and while it's still not very precise for high-risk users, it's better than its predecessors. When it predicts a user is low-risk it will be correct 100% of the time, and when it predicts a user is high-risk it will be correct 3% of the time.
  * Recall: This model has a greater average recall than any of the undersampling/oversampling methods, and will correctly identify 89% of low-risk users and 68% of high-risk users.
  
    <img width="314" alt="balanced_random_forest" src="https://user-images.githubusercontent.com/111674383/213121928-51d51dd9-8aee-48c6-9761-6c47c0f64b21.png">
---
* **Easy Ensemble AdaBoost Classifier**
  * Balanced Accuracy Score: 0.93
  * Precision: This model has the highest precision for both classes of all the models tested. When it predicts a user is low-risk it will be correct 100% of the time, and when it predicts a user is high-risk it will be correct 7% of the time.
  * Recall: This model has the highest recall for both classes of all the models tested. It will correctly identify 94% of low-risk users and 91% of high-risk users. 
  
    <img width="311" alt="easy_ensemble" src="https://user-images.githubusercontent.com/111674383/213121951-cefc6753-0708-4cef-9f42-e55081385f9e.png">

## Summary

Oversampling, undersampling, and combination sampling methods all had identical precision scores. The ensemble models performed slightly better for high-risk users, with the Easy Ensemble method producing the highest score of all.

Average recall scores of ensemble models were also higher than oversampling, undersampling, and combination models. The Easy Ensemble model outperformed all other models across both classes. 

As the Easy Ensemble model had the highest scores for both precision and recall across both classes, it is recommended that it be used moving forward.
