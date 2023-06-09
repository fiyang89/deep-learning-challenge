# Deep Learning Challenge
*(This project was created in Google Colab.)*

## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you'll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup's business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.

## Report on Neural Network Model
### Overview of Analysis: Explain the purpose of this analysis.
The purpose of this analysis is to predict how successful applicants will be if they are funded by Alphabet Soup with a goal of above a 75% accuracy score.

### Results: Using bulleted lists and images to support your answers, address the following questions:
- #### Data Preprocessing
      a. What variables are the targets for your model? 
            - For all Models 1-3, the target variable is "IS_SUCCESSFUL"
      b. What variables are the features for your model? 
            - For Model 1, the feature variables were: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE",  
              "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT" 
            - For Model 2, the feature variables were: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE",  
              "ORGANIZATION", "STATUS", "SPECIAL_CONSIDERATIONS"
            - For Model 3, the feature variables were: "NAME", "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE",  
              "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT"
      c. What variables should be removed from the input data because they are neither targets nor features?
            - For Model 1, the variables that were removed were: "EIN" and "NAME"
            - For Model 2, the variables that were removed were: "EIN", "NAME", "INCOME_AMT", and "ASK_AMT"
            - For Model 3, the variable that was removed was: "EIN"

- #### Compiling, Training, and Evaluating the Model
      a. How many neurons, layers, and activation functions did you select for your neural network model, and why?
            - For Models 1-3, there were two layers and the activation function used was sigmoid.
            - For Model 1, the number of neurons selected were 80 and 30
            - For Model 2, the number of neurons selected were 60 and 20
            - For Model 3, the number of neurons selected were 90 and 40
      b. Were you able to achieve the target model performance?
            - For Model 3, the target model performance was achieved with an accuracy score of 76.83%
      c. What steps did you take in your attempts to increase model performance?
            - After conducting the analysis for the baseline performance, Model 1. I manipulated the data by removing more 
              variables at first. Then, decided to remove even less once realizing that the accuracy score for Model 2 was 
              less accurate than Model 1.

### Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
The final optimization, Model 3, achieved an accuracy score of 76.83% using a sigmoid activation function. Using a different model such as the tanh function would be more preferable than sigmoid because the output using tanh will allow for more accurate data points on the entirety of the matrix.

- #### Model 1 resulted in an accuracy score of 72.66% with: [Starter Code](Starter_Code.ipynb)
      a. layer 1 = 80 neurons and layer 2 = 30 neurons
      b. epochs = 100


![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/6094a8d4-6107-4d32-905e-5a3a37b15650)

![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/c2f5678f-886e-46a1-9602-ddb096668e2b)

- #### Model 2 resulted in an accuracy score of 72.45% with: [AlphabetSoupCharity_Optimization](AlphabetSoupCharity_Optimization.ipynb)
      a. layer 1 = 60 neurons and layer 2 = 20 neurons
      b. epochs = 100


![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/bf333864-265b-4f99-9af9-719ae45ec1f0)

![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/7b094e2d-6b79-4676-a29f-83b4f265adb0)

- #### Model 3 resulted in an accuracy score of 76.83% with: [AlphabetSoupCharity_Optimization_2](AlphabetSoupCharity_Optimization_2.ipynb)
      a. layer 1 = 90 neurons and layer 2 = 40 neurons
      b. epochs = 20


![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/93d37cb3-085e-45f6-b08a-dfa493fd04de)

![image](https://github.com/fiyang89/deep-learning-challenge/assets/120594187/02ca2b60-6071-4381-90bb-2682a49fb78c)



