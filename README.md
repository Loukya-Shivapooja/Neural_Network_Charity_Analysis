# Neural_Network_Charity_Analysis
## Overview of the Analysis
Using Machine Learning and Neural Networks for this project, I used the features in the dataset to create a binary classifier that will help to predict if the applicants that will be funded by a Charitable organization called Alphabet Soup will be successful. For this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. This project compromised of the following 3 steps:

* Preprocessing the data for the neural network
* Compile, Train and Evaluate the Model
* Optimizing the model
### Resources
* Data Source: charity_data.csv
* Software: Python, Jupyter Notebook
## Results:
### Data Preparation:
* Variable that was considered as the target for the model is: `IS_SUCCESSFUL` Column.
* Variables that were considered features for the model are: `Every Column except for IS_SUCCESSFUL` which is our target and the ones we will drop.
* Variable that were neither targets or features for the dataset: Columns that can be droped are `EIN`, `NAME` because they will have little to no impact on the outcome.
### Compiling, Training and Evaluating the Model
1. The number of neurons, layers, and activation functions selected for the neural network model:
* Neural Network model had 2 hidden layers. My first layer had 80 neurons, the second has 30 there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."
<img width="1007" alt="Screen Shot 2022-10-26 at 9 52 42 PM" src="https://user-images.githubusercontent.com/107584361/198195122-ad39699f-11e3-483a-bcb5-d823404b8962.png">
2. Performance of the model:
* The model was not able to reach the target 75%. The accuracy for my model was 64%.
<img width="641" alt="Screen Shot 2022-10-26 at 9 56 46 PM" src="https://user-images.githubusercontent.com/107584361/198195634-f2c4eef3-41eb-4ef2-b875-053660562e31.png">
3. The steps taken to try and increase model performance
* Attempt 1: Removed additional feature, that is the 'STATUS', 'SPECIAL_CONSIDERATIONS' column. Rest of the model components stayed the same
<img width="905" alt="Screen Shot 2022-10-26 at 10 00 42 PM" src="https://user-images.githubusercontent.com/107584361/198196086-731e0f51-2cb1-4e4b-af9c-63d530efd917.png">
then the model accuracy improved to 68%.
<img width="634" alt="Screen Shot 2022-10-26 at 10 02 27 PM" src="https://user-images.githubusercontent.com/107584361/198196269-be17502a-4d57-4bc6-9b4c-8dfaf5eac7b4.png">

* Attempt 2: Adding Additional neurons to hidden layers and additional hidden layers are added. This time accuracy went down to 58%.

<img width="934" alt="Screen Shot 2022-10-26 at 10 05 00 PM" src="https://user-images.githubusercontent.com/107584361/198196604-631a9aac-16da-41fd-8dac-bfb0d17ca89c.png">

<img width="687" alt="Screen Shot 2022-10-26 at 10 06 17 PM" src="https://user-images.githubusercontent.com/107584361/198196743-eb7c9a48-fe0f-4a12-a9d2-b1ac3bd0b423.png">

* Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." The accuracy of the model went down even more to 47%.

<img width="956" alt="Screen Shot 2022-10-26 at 10 08 07 PM" src="https://user-images.githubusercontent.com/107584361/198196940-e6aac1b8-4cce-4178-8b49-56cdc38cf983.png">

<img width="657" alt="Screen Shot 2022-10-26 at 10 08 51 PM" src="https://user-images.githubusercontent.com/107584361/198197027-591a15dc-363a-4c42-975b-eece7126b615.png">

## Summary
The model ended up with the accuracy score of 47% after optimization. The initial neural network had a accuracy score of 64%. This loss in accuracy can be due model overfitting. Also we can optimize our neural network by removing more features from the dataset to increase accuracy. Since our accuracy score was not particularly up to the standard with neural networks, we could have used the Random Forest classifiers. This is because random forest is an accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and could have avoided the data from being overfitted.
