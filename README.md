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
