Wafer-Fault-Detection
Problem Statement:
To build a classification methodology to predict the quality of wafer sensors based on the given training data. The inputs of various sensors for different wafers have been provided. In electronics, a wafer (also called a slice or substrate) is a thin slice of semiconductor used for the fabrication of integrated circuits. There are two classes: +1 and -1.

+1 means that the wafer is in a working condition and it doesn’t need to be replaced.
-1 means that the wafer is faulty and it needs to be replaced.
Architecture

https://github.com/singhrahulbrijesh/Thyroid-Detection-main/blob/master/Thyroid-Detection-main/Images/architecture.jpg

Data Validation
In this step, we perform different sets of validation like filename validation, number of columns, name of the columns,data type of each columns and other kind of validations.

Data Insertion in Database
In this step we perform the following things

Database Creation and connection
Table creation in the database
Insertion of files in the table
Model Training
Data Export from Db - The data in a stored database is exported as a CSV file to be used for model training.
Data Preprocessing - Checking for null values, imputation for null values using KNNImputer, removing the features with zero standard deviation etc.
Clustering - The idea behind clustering is to implement different algorithms.To train data in different clusters. The Kmeans model is trained over preprocessed data and the model is saved for further use in prediction.
Model Selection - After clusters are created, we find the best model for each cluster. Two algorithms are used RandomForest and XGBoost
Model Prediction
Here also all the above steps like Data Validation, Data Insertion in Database, Data Preprocessing and Clustering is performed. Based on the cluster group, the model is loaded and prediction is made.

Wafer-Fault-Detection/README.md at master · Vinay-Kalmoodkar/Wafer-Fault-Detection · GitHub
