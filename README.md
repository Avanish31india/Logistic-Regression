# Logistic-Regression
 Implementation  Logistic Regression with L1 regularization from scratch and predict the labels of the test data.
Implement Logistic Regression from scratch
In this assignment, you will implement Logistic Regression with L1 regularization from scratch and predict the labels of the test data. You will then verify the correctness of the your implementation using multiple "grader" functions/cells (provided by us) which will match your implmentation.

The grader functions would help you validate the correctness of your code.
Instructions:
Read in the train_data.
Vectorize train_data and test_data using sklearns built in tfidf vectorizer.
Ignore unigrams and make use of both bigrams & trigrams and also limit the max features to 2000 and minimum document frequency to 10.
After the tfidf vectors are generated as mentioned above, next task is to column standardize your data.
We want you to write in comments in your code, the reason you think for standardizing the data in the above step.
You can use sklearn StandardScaler to column standardize your data.
Write a function to initialise your weights & bias. And then run its corresponding grader function.
Write a custom function to calculate sigmoid of a value. And then run its corresponding grader function to cross check your implementation of sigmoid function.
Write a custom function to compute the total loss as the sum of log loss and l1 regularization loss based on true labels and predicted labels and weights. And you can crosscheck your implementation with its corresponding grader.
Write a function to compute gradients for your weights and bias terms, which you have to make use of in updating your weights and bias while training your model.
Implement a custom train function of logistic regression, wherein you take in the following inputs:

X_train which will be your vectorized text data
y_train which are the labels for your train data
alpha = 0.0001 which is the regularization factor (λ)
eta0 = 0.0001 which will be the learning rate
tolerance = 0.001
In the custom train function you should make use of a custom SGD function to update the weights and bias terms for each of your inputs.

The custom SGD implemented in the above train function for updating the weights and bias terms should run for many epochs until the difference in loss between two consecutive epochs is less than tolerance.

Here one epoch means a complete iteration of your entire train data.

Your train function should return the follwing:

the number of epochs it took to complete the training
train loss for all epochs
the values for final weights and bias terms.
Now run the grader function to check whether the weights and bias obtained from your custom implementation are close enough to that of sklearns implementation.

Next write a custom predict function which takes in as input the weights and bias values that you computed in your train function, and also takes in the test standardized data as input to predict its labels.
Now run the grader function to check the accuracy of your predictions.
