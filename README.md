#### Marketing Campaign
**Purpose**: Using Machine Learning Models evaluate the effectiveness of Marketing campaign for bank customers
Find insights which can help in improving the effectiveness of the campaign

# Table of Contents
   1. Data Details
   2. Data Preperation
   3. Modeling
   4. Cross Validation of Model Results
   6. Feature Selection
   7. Conclusion
   8. Business Insights

### 1. Data Details :
1. Read data from the source file and stored in data frame
2. Data Quality Check -
        1. Checked Null values in the data - No null records found
        2. Checked duplicates - 12 duplicate records found- deleted duplicates
        
3. Checked unique values for each feature to visually check for any un realistic or un common value
  
 ### 2. Data Preperation ** 
   1. Deleted 12 duplicate records
   2. Train Test Split : Splitted data into Train Test Sets
   3. Dropped feature "Duration" as suggested in instructions because I am building predictive models
   4. Split data into Trainning and Test sets
   5. Applied One hot encoding on these features :  one_hot_features = ['job',  'marital', 'default', 'housing', 'loan', 'contact', 'poutcome']\
   6. Applied Ordinal encoding on these features:   ordinal_features = ['education', 'month', 'day_of_week']
   7. Did selective scaling using Standard Scaler : Scaled only the columns which were non binary
   8. Data Preperation Completed

### 3. Modeling
1. Logistic Regression
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE,
          RMSE etc.
       2. Plotted ROC Curve

   **Metrics and Curve for Logisct Regression**
   ![Logistic Regression Results]()
   
2. Decision Tree
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve

  **Metrics and Curve for Decision Tree**
   ![Decision Tree Results]()
       
3. KNN
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve
       
  **Metrics and Curve for KNN**
   ![KNN]()
       
4. SVM
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve

  **Metrics and Curve for SVM**
   ![KNN]()

   
   **Metrics  comparision of all the 4 Models**
   ![Metrics](https://github.com/viksaraw/Marketing-Campaign/blob/main/Metrics.png)

   ### 4. Cross Validation of Model Results
   1. Create a countplot to visualize the impact of various columns like 'marital' etc. on 'y'
   2. Applied Grid Search CV on all the Models above to find the best params.
   3. Metrics with best params for each model is displayed as belo
   4. 

