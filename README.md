# credit_card_fraud_detection
## Problem statement
To build a classification methodology to predict whether the person repays his creditcard bill or not.<br>
## Data Description
Data contains 24 Independent features and 1 dependent feature.<br>
The last column will have the "Default_payment" value for each wafer.<br>
"1" represents the person who is not repaying the creditcard bill.<br>
"0" represents the person who repays the bill .<br>
## Steps
1.<b>"Data validation"</b>:
The name of the dataset, number of columns,datatype,and whether the whole column in a dataset is empty or not are validated.<br>
The datasets which gets passed in the above validations are moved to <b>"Good Data"</b> folder and the rest of the datasets are moved to <b>"Bad Data"</b> folder.<br>
The datasets in the <b>"Good Data"</b> folder are transformed and stored in a database and then all the datasets exported as a <b>"Input.csv"</b>file.<br>
2.<b>"Data Preprocessing"</b>:
The missing values are handled by using KNN imputer.<br>
The Columns which are having zero standard deviation are removed.<br>
3.<b>"Clustering"</b>:
The dataset is grouped in the form of clusters and it is done by using <b>"Kmeans++"</b> algorithm and for each cluster a seperate model is created.<br>
4.<b>"Model creation"</b>:
The model creation is done by using <b>"Decision Tree"</b> algorithm and <b>"Logistic Regression"</b> algorithm and the model which is having the highest <b>"AUC_ROC"</b> score is selected.Hyperparameter tuning is also done to avoid the overfitting problem<br>.
5.<b>"Model Prediction"</b>:
Once the test data is given then  <b>"Data validation"</b> and <b>"Data Preprocessing"</b> are done depending upon the cluster the model is chosen and prediction is done using that model and the results are stored in "Prediction.csv" file.
