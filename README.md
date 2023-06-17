Wafer-Fault-Detection
Problem Statement:
To build a classification methodology to predict the quality of wafer sensors based on the given training data. The inputs of various sensors for different wafers have been provided. In electronics, a wafer (also called a slice or substrate) is a thin slice of semiconductor used for the fabrication of integrated circuits. There are two classes: +1 and -1.

+1 means that the wafer is in a working condition and it doesn’t need to be replaced.
-1 means that the wafer is faulty and it needs to be replaced.
##Architecture

![](https://github.com/singhrahulbrijesh/Waferfault-detection/blob/main/architecture.jpg)

Data Validation
In this step, we perform different sets of validation like filename validation, number of columns, name of the columns,data type of each columns and other kind of validations.

Data Insertion in Database
In this step, we perform the following things


## Data Insertion in Database - For Prediction Data
1) Database Creation and connection - Create a database with the given name passed. If the database is already created, open the connection to the database. 
2) Table creation in the database - Table with name 
3) Insertion of files in the table

## Prediction 
 
1) Data Export from Db
2) Data Preprocessing   
   a) Drop columns not useful for training the model. Such columns were selected while doing the EDA.
   b) Replace the invalid values with numpy “nan” so we can use imputer on such values.
   c) Encode the categorical values
   d) Check for null values in the columns. If present, impute the null values using the KNN imputer.
3) Clustering - KMeans model created during training is loaded, and clusters for the preprocessed prediction data is predicted.
4) Prediction - Based on the cluster number, the respective model is loaded and is used to predict the data for that cluster.
5) Once the prediction is made for all the clusters, the predictions along with the original names before label encoder are saved in a CSV file at a given location and the location is returned to the client.

## Deployment
We will be deploying the model to the any Cloud Based Service Platform for example, AWS, Azure, GCP, Heroku or Pivotal Web Services. 
This is a workflow diagram for the prediction of using the trained model.     
