<h1 align="left">SUPERVISED MACHINE LEARNING<br><i>Topic: Credit Risk Classification</i> </h1> 

<p>This project aims to build a machine learning model that can identify the creditworthiness of borrowers using historical lending data from a peer-to-peer lending services company.</p>
 
## Methodology
1. Split data into training and testing datasets using train_test_split
2. Fit a logistic regression model using the training data 
3. Resample imbalanced data
3. Forecast credit risk

## Conclusions
See file [report.md]([url](https://github.com/chadbarlow/gt-data-bootcamp_challenge-20_supervised-ml/blob/main/report.md))

## Limitations and Further Development
- Perform feature engineering (e.g. PCA Analysis) to identify the most important features for credit risk prediction.
- Oversampling helped improve the performance of our model on the minority class. Other resampling techniques, such as under-sampling the majority class or using a combination of over- and under-sampling, might be able to improve the performance even more.
