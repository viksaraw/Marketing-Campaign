#### Marketing Campaign
**Purpose**: Using Machine Learning Models evaluate the effectiveness of Marketing campaign for bank customers.
Find insights which can help in improving the effectiveness of the campaign

# Table of Contents
   1. Data Details
   2. Data Preperation
   3. Modeling
   5. Cross Validation of Model Results
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
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve
2. Decision Tree
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve
3. KNN
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve
4. SVM
       1. Applied Logistic Regression and calculated metrics like - Accuracy score, Recall Score, Precision Score, MSE, RMSE etc.
       2. Plotted ROC Curve

   **Metrics  comparision of all the 4 Models**
   ![Metrics](https://github.com/viksaraw/Marketing-Campaign/blob/main/Metrics.png)

   |               Model | Accuracy |  Recall  | Precision | F1 Score   |
0  |               KNN   | 0.886987 | 0.275936 | 0.503906  |  0.356600  | 
1  |    Decision Tree    | 0.832848 | 0.325134 | 0.289524  | 0.306297   |
2  |             SVM     | 0.897037 | 0.232750 | 0.686930  | 0.347692   |
3  |Logistic Regression  | 0.893031 | 0.187436 | 0.664234  | 0.292369   |

  |        Model        ROC AUC Score         Log Loss          Mean Absolute Error   Mean Squared Error          R2 Score  
0           KNN        0.710789              1.756601             0.113013            0.113013                  -0.123204  
1 Decision Tree        0.613728              5.982041             0.167152            0.167152                  -0.661280  
2           SVM        0.681948              0.320381             0.102963            0.102963                   0.009950  
3 Logisctic Regression 0.777897              0.291530             0.106969            0.106969                  -0.028578  
   
