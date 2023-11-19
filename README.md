# Module 21 Deep Learning Challenge
# Overview of the Analysis

* The purpose of this analysis is to use the features in the provided dataset to create a binary classifer that can predict whether applicants will be successful if funded by Alphabet Soup.  

* The lending data provided a CSB containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.  Within the dataset we can see:  EIN and Name, Application_Type, Afffiliation, Classification, Use_Case, Organization, Status, Income_Amt, Special_Considerations, Ask_Amt, Is_Successful.

  Removed EIN and Name because they are neither target nor features.

* Objective of analysis was to predict which ventures will have the best chance of success in their venture.

* The stages of machine learning process
    - Preprocess the data
    - Compile, train and evaluate the model
    - Optimize the model

## Results
* Model: sequential_4
  * Layer(type)     Output Shape    Param#
    dense(Dense)    (None, 9)       414
    dense_1(Dense)  (None, 18)      180
    dense_2(Dense)  (None, 1)       19
  
  * Total params: 613
  * Traininable params: 613
  * Non-trainable params: 0
    

* Model results using test data:
  * Loss: 0.55
  * Accuracy: 0.72


## Summary
* Accuracy of test data is 72%.  
* Loss of test data is 55%
  
