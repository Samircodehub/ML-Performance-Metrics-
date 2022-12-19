# Performance Metrics for in Machine Learning

Simply building a predictive model should not our motive. It’s about creating and selecting a model which gives high accuracy on out of sample data. Hence, it is crucial to check the accuracy of your model prior to computing predicted values.

Machine learning metrics are techniques used to check machine learning model performance on the input data that was supplied to it and how well the model generalizes on new data. This way, the performance of the model can be improved by tuning the hyper parameters or tweaking features of the input dataset. 

There are separate perforance mertices for regression and classification problems

Specific metrics need to be used on specific learning models, and not all metrics can be used on a single model. Just a specific metric or a set of metrics can be taken as point of reference and improved upon. 

### Performance Metrics for Classification problems 

Accuracy
Confusion Matrix
Precision
Recall
F-Score
AUC(Area Under the Curve)-ROC\
Confusion Matrix
Log Loss

#### Accuracy
Accuracy :  total number of predictions that were correct out of total number of predictions.
![image](https://user-images.githubusercontent.com/108605935/208358051-1be712f6-f49b-47d4-9ac1-e7086d69cf63.png)
When to Use Accuracy?
It is good to use the Accuracy metric when the target variable classes in data are approximately balanced. For example, if 60% of classes in a fruit image dataset are of Apple, 40% are Mango. In this case, if the model is asked to predict whether the image is of Apple or Mango, it will give a prediction with 97% of accuracy.

When not to use Accuracy?
It is recommended not to use the Accuracy measure when the target variable majorly belongs to one class. For example, Suppose there is a model for a disease prediction in which, out of 100 people, only five people have a disease, and 95 people don't have one. In this case, if our model predicts every person with no disease (which means a bad prediction), the Accuracy measure will be 95%, which is not correct.

So accuracy metrice use when you have balance data (like in proportion of 40:60, 50:50, 55:45)

#### Confusion Matrix
A confusion matrix is a tabular representation of prediction outcomes of any binary classifier, which is used to describe the performance of the classification model on a set of test data when true values are known

![image](https://user-images.githubusercontent.com/108605935/208359579-e2c7a979-2b78-4687-aeaf-39dac2476f13.png)

* In the matrix, columns are for the prediction values, and rows specify the Actual values. Here Actual and prediction give two possible classes, Yes or No. So, if we are predicting the presence of a disease in a patient, the Prediction column with Yes means, Patient has the disease, and for NO, the Patient doesn't have the disease.
* In this example, the total number of predictions are 165, out of which 110 time predicted yes, whereas 55 times predicted No.
* However, in reality, 60 cases in which patients don't have the disease, whereas 105 cases in which patients have the disease.

1. True Positive(TP): In this case, the prediction outcome is true, and it is true in reality, also.
2. True Negative(TN): in this case, the prediction outcome is false, and it is false in reality, also.
3. False Positive(FP): In this case, prediction outcomes are true, but they are false in actuality.
4. False Negative(FN): In this case, predictions are false, and they are true in actuality.


###### Precision
It can be calculated as the True Positive or predictions that are actually true to the total positive predictions (True Positive and False Positive).

![image](https://user-images.githubusercontent.com/108605935/208360699-d2e5d7c0-201e-4b8b-9d9a-b4e08ef867fc.png)


###### Recall or Sensitivity

It is also similar to the Precision metric; however, it aims to calculate the proportion of actual positive that was identified incorrectly. It can be calculated as True Positive or predictions that are actually true to the total number of positives, either correctly predicted as positive or incorrectly predicted as negative (true Positive and false negative).

The formula for calculating Recall is given below:
![image](https://user-images.githubusercontent.com/108605935/208361030-7b9a38be-e143-4094-b665-32905957c718.png)


###### When to use Precision and Recall?

From the above definitions of Precision and Recall, we can say that recall determines the performance of a classifier with respect to a false negative, whereas precision gives information about the performance of a classifier with respect to a false positive.

So, if we want to minimize the false negative, then, Recall should be as near to 100%, and if we want to minimize the false positive, then precision should be close to 100% as possible.

In simple words, if we maximize precision, it will minimize the FP errors, and if we maximize recall, it will minimize the FN error.

###### F-Scores
F-score or F1 Score is a metric to evaluate a binary classification model on the basis of predictions that are made for the positive class. It is calculated with the help of Precision and Recall. It is a type of single score that represents both Precision and Recall. So, the F1 Score can be calculated as the harmonic mean of both precision and Recall, assigning equal weight to each of them.

The formula for calculating the F1 score is given below:

![image](https://user-images.githubusercontent.com/108605935/208361421-7c4dab07-b22d-4a26-8a00-5ac750cd944d.png)


###### When to use F-Score?

As F-score make use of both precision and recall, so it should be used if both of them are important for evaluation, but one (precision or recall) is slightly more important to consider than the other. For example, when False negatives are comparatively more important than false positives, or vice versa.


### Performance Metrics for Regression
Mean Absolute Error
Mean Squared Error
R2 Score
Adjusted R2

III. R Squared Score
R squared error is also known as Coefficient of Determination, which is another popular metric used for Regression model evaluation. The R-squared metric enables us to compare our model with a constant baseline to determine the performance of the model. To select the constant baseline, we need to take the mean of the data and draw the line at the mean.
The R squared score will always be less than or equal to 1 without concerning if the values are too large or small.
![image](https://user-images.githubusercontent.com/108605935/208362508-7c447c97-80f3-4369-8d6f-153c74e34a40.png)


Adjusted R Squared
Adjusted R squared, as the name suggests, is the improved version of R squared error. R square has a limitation of improvement of a score on increasing the terms, even though the model is not improving, and it may mislead the data scientists.

To overcome the issue of R square, adjusted R squared is used, which will always show a lower value than R². It is because it adjusts the values of increasing predictors and only shows improvement if there is a real improvement.

We can calculate the adjusted R squared as follows:

![image](https://user-images.githubusercontent.com/108605935/208362602-bbe7331b-b7e0-4313-9024-b761767035eb.png)



Source: https://www.javatpoint.com/performance-metrics-in-machine-learning
