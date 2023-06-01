# deep-learning-challenge

### Summary
We are using machine learning for nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 
In the data frame we can see some information and predict how applicants will be successful if funded by Alphabet Soup. We used customer provide "charity_data.csv" dataset and use "APPLICATION_TYPE" to start predict in machine learning.
Also we use ['CLASSIFICATION'].value_counts() to support counts in the data frame and using "sklearn.model_selection and sklearn.preprocessing" to support nonprofit foundation predict.

### Result
Total params: 5,981 Trainable params: 5,981 Non-trainable params: 0.    
In Result, the model achieved a loss of 0.5616 and an accuracy of 0.7312 on the test data. 
This means that the model performed reasonably well in predicting the target variable for the unseen test samples, with an accuracy of 73.12%. The selecting applicants for funding may not easy success, 
because 73.12% is not a high rate.  
If Alphabet Soup has a more lenient approach and is willing to accept a certain level of risk or wants to cast a wider net to support a larger number of potential successful ventures, 
a 73.12% accuracy could be considered reasonable.

### Data Preprocessing
**Variable(s) are the target(s) in model**

Based on the provided script, The model aims to predict this target represents a success of the ventures for which Alphabet Soup is considering funding. The model can be assumed  where 1 indicates a successful venture and 0 indicates an unsuccessful venture.

**Variable(s) are the features in model**

Under the "pd.get_dummies" and y = Convert_cat_dummies.IS_SUCCESSFUL.values , X = Convert_cat_dummies.drop(columns="IS_SUCCESSFUL").values that 2 section,  features include all the encoded categorical variables, as well as any other numerical or categorical variables that were present in the original dataset and were preprocessed before creating dataFrame.

**Variable(s) should be removed from the input data because they are neither targets nor features**

In my line "application_df.drop(['EIN', 'NAME'], axis=1, inplace=True)", the variables should be removed "EIN" and "NAME" from the input data that column.  Because they are not targets nor features for model to use.

**Neurons, layers, and activation functions select for your neural network model**

The number of input features is determined dynamically based on the training data and Scale the data. The "X_train_scaled = X_scaler.transform(X_train)" and "X_test_scaled = X_scaler.transform(X_test)" is a good start to use define model. In this analysis is import tensorflow for First and second hidden layer. Also use "Output layer" and activation="sigmoid" = sigmoid(x) = 1 / (1 + exp(-x)) for binary classification. Experimentation and tuning of these parameters may be necessary to achieve the best model performance.

**Were you able to achieve the target model performance**
it is difficult to determine whether the target model performance has been achieved or not. Because the model performance calculates answer is loss and accuracy on the test data using the evaluate method.

