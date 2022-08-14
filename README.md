# Neural_Network_Charity_Analysis
## Overview
Alphabet Soup's business team has provided a list of ~34,000 organizations that have received funding over the years.  Utilizing neural networks, analysis was requested of the dataset to create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup.  Data required preprocessing to eliminate superfluous data columns, scale outsized data, and ensure data is formatted correctly for compiling, training and evaluating.  After establishing the model and testing, Tensorflow was utilized in an attempt to improve the efficiency of the model to greater than 75%.

## Results
### Data Preprocessing
  * Target Variable
    * IS_SUCCESSFUL
  * Feature Variables
    * APPLICATION_TYPE
    * AFFILIATION
    * CLASSIFICATION
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT
  * Variables to remove from Data Set
    * EIN
    * NAME

### Compiling, Training and Evaluating the Model
The initial model had two hidden layers with 80 and 30 neurons, respectively.  Utilized Relu activation functions for the hidden layers and Sigmoid for the 
output layer.

![Screen Shot 2022-08-14 at 5 28 04 PM](https://user-images.githubusercontent.com/98665941/184557153-9531ee07-b8e8-447f-8f34-304dd648c700.png)
