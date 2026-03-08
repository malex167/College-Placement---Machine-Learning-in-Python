# Executive Summary

 Through an examination of college admissions for graduate students targeting programs in Marketing, HR, or Finance at Jain University Bangalore via the campus recruitment data set gathered from Kaggle, variables including high school performance, undergraduate specialization, undergraduate performance, degree, and more were targeted in predicting prospective student placement. This was conducted through Python with the Visual Studio Code environment via pandas, numpy, matplotlib, and scikit learn. Overall, the initial random forest model was approximately 84% accurate in predicting admissions; after conducting hyperparameter tuning, the model improved to 86% along with yielding a precision of 85% and a recall of 97%. Practical recommendations observed from the model include tailoring its applications towards a specific individual as a predictor of admissions based on existing credentials. Additional work could be conducted exploring alternative models with improved accuracy.  

## Problem

For individuals looking to pursue higher education, applying to college can be a daunting task. Through an analysis of various contributing factors potentially influencing college admissions, a model predicting acceptance would be a worthwhile tool for an individual to utilize and assess whether their current credentials are viable towards getting accepted or if additional work might be required. 

## Methodology

The primary variable in question from the data set is "status" indicating whether an individual placed or didn't place when applying to schools. Accordingly, this served as the predicted variable while the remainder of the data set in question were the predictors. The ensemble machine learning algorithm Random Forest was targeted as high performing system capable of developing classification models. This was achieved by performing an 80:20 split of the data in Python, training the respective model with the majority of the split, testing the model's accuracy via the remaining data portion along with a confusion matrix, and then tuning the hyperparameters and visualizing the most influential components. 

## Skills

1. Python (pandas, numpy, matplotlib, scikit learn)
2. Visual Studio Code
3. Machine Learning Models (Random Forest)
4. Data Wrangling
5. Data Visualization

## Results and Recommendation

From the 80/20 split performed towards training and predicting college placement, the initial Random Forest model resulted in an accuracy of 83.7%. This was improved upon through hyperparameter tuning in which an estimator of 472 decision trees yielded the optimal max depth of 13 per tree, along with a minimum leaf sample of 3 and a minimum sample split of 9. This improved accuracy to 86% while also resulting in a precision of 85% and a recall of 97%. 

From a visual assessment of a confusion matrix, 43 observations where reported. 29 observations accurately predicted placement when placement occured, 5 accurately predicted rejection when rejection occured, while 5 produced false positives (Type I) in which an invidual was rejected when they actually got accepted, and 1 false negative (Type II) where an individual was accepted when they actually got rejected. 

<img width="498" height="432" alt="image" src="https://github.com/user-attachments/assets/ba887c1d-c20b-47a3-a157-525f5bd42244" />

**Figure 1: Confusion matrix of tuned Random Forest model.**

Through an examination of feature importance, scoring percentage for the 12th grade was the largest indicator of admissions followed by undergraduate degree and 10th grade scoring percentages, this is followed by the scoring percentage when receiving an MBA. 

<img width="556" height="494" alt="image" src="https://github.com/user-attachments/assets/4f443521-fdad-41dd-9c73-e52afdc774df" />

**Figure 2: Feature importance from Random Forest model.**

## Next Steps

Practical recommendations observed from the model include tailoring its applications towards a specific individual as a predictor of admissions based on existing credentials. Additional work could be conducted exploring alternative models with improved accuracy and performance. 
