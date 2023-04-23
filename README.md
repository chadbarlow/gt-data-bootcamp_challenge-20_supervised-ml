<h1 align="left">SUPERVISED MACHINE LEARNING<br><i>Topic: Credit Risk Classification</i> </h1> 

<p>This project aims to build a machine learning model that can identify the creditworthiness of borrowers using historical lending data from a peer-to-peer lending services company.</p>
 
## Methodology
1. Split data into training and testing datasets using train_test_split
2. Fit a logistic regression model using the training data 
3. Forecast credit risk

## Conclusions
The logistic regression model predicts both healthy loans (0) and high-risk loans (1) with moderate accuracy. 

## Limitations and Further Development
- The model's accuracy, precision, and recall scores may not be optimal for real-world applications. Investigate alternative classification algorithms to improve model performance.
- The dataset may not be representative of all borrowers or loan situations. Collect additional data to create a more representative dataset.
- Perform feature engineering to identify the most important features for credit risk prediction.
- Conduct hyperparameter tuning to optimize the logistic regression model.
