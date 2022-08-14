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

After 50 epochs, the model was able to achieve an accuracy of 73.3% using the test data, short of the target 75%.

![Screen Shot 2022-08-14 at 5 31 46 PM](https://user-images.githubusercontent.com/98665941/184557218-5ec61dad-d0c1-4a91-9d2d-3b443ce23291.png)

In an attempt to reach the target 75%, 3 modifications were made to the model with the following results:
* Remove additional variables from features
  * Removed USE_CASE and ORGANIZATION in addtion to EIN and NAME
  * ![Screen Shot 2022-08-14 at 5 39 33 PM](https://user-images.githubusercontent.com/98665941/184557432-bd29cda5-39fa-4e5c-874d-64d96b0ad1b6.png)
  * Accuracy dropped to 72.8%
  *  ![Screen Shot 2022-08-14 at 5 40 02 PM](https://user-images.githubusercontent.com/98665941/184557441-0a2bdc20-6de9-40be-b838-7e890af0fd2a.png)
* Added additional neurons to the hidden layers
  *  ![Screen Shot 2022-08-14 at 5 42 11 PM](https://user-images.githubusercontent.com/98665941/184557508-307eb94e-8947-4d35-b7d2-e52a17d3fa8d.png)
  *  Accuracy for the model was 72.9%
  *  ![Screen Shot 2022-08-14 at 5 43 48 PM](https://user-images.githubusercontent.com/98665941/184557545-561e5361-ed05-451d-ab3b-9a173e3ffa4c.png)
* Added additional layers and used TanH for the first hidden layer
  *  ![Screen Shot 2022-08-14 at 5 45 27 PM](https://user-images.githubusercontent.com/98665941/184557602-58f65597-79d5-415d-8573-31ff604c2ecb.png)
  *  Accuracy for the model was 72.9%
  *  ![Screen Shot 2022-08-14 at 5 48 07 PM](https://user-images.githubusercontent.com/98665941/184557677-9c8d91fa-e5c7-4077-b195-e2df50055dab.png)
* Target accuracy of 75% was not acheived with the modifications to the model

## Summary
Our model was able to acheive an accuracy of just over 73% at peak performance.  This is below the target of 75%, but not a poor performance overall.  Would recommend utilizing the Keras Tuner to evaluate for the ideal model structure.  Suspect that the model has been overfit with the high number of neurons used.



