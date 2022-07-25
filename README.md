# Titanic_Project

## Overview of Project
-  The well-known Data website, Kaggle, offers a Titanic Machine Learning competition, and the goal is to use machine learning to create a model that predicts which passengers survived the Titanic shipwreck. They provide a dataset of passengers and you are to train the data to then try and determine if the test data would correctly predict if passengers would survive the wreck based on the data provided. 

### Description of the Dataset

- The training dataset gives 891 passengers that included survival, name, fare, cabin, sex, location of embarkment, passenger class, if they traveled with a passenger, and age. 

- The test dataset has 418 passengers with the same data except for the survival.

#### Machine Learning

##### Description of preliminary data preprocessing
- The first step in our Machine Learning phase was preprocessing and to check to see if any data was missing. Then I decided to bin the age and fare groups into groups of 0,1,2, etc. I considered normalizing the data, but decided against it as our model standardizes the data prior to testing. I also took the cabin number and took the initial letter from known cabin numbers and put those into groups (A = 1, B = 2, etc.). Then I took passengers who were unknown for their cabin, but in the 3rd passenger class, and put them in a group, and same with the 1st and 2nd class passengers. 

- I also engineered a couple additional groups due to age. I binned known ages by multiples of 10(0-10, 11-20), and then I included unknown aged child who were on the passenger list as master (a term known for children under the age of 18) as their own group, and unknown aged married women as another group. While the age wasn't available I hoped grouping them, might help the machine.  

##### Splitting the training and testing sets 

- The data was split into the standard 75-25% split that skllearn defaults to. I used the survived feature as the one for testing.

### Model Choice

- I chose a classification model and specifically Logistic Regression as I needed to answer the question of whether our model could classify someone as having survived or not. The simplistic nature and application of a Logistic Regression Model led me to go towards this direction. I felt that our data would struggle to find a way to pinpoint a numerical prediction, but the data could answer classification questions better.

  - Pros of logistic regression models

    - The most beneficial aspect of this model, similarly to its Linear counterpart, is its simplicity. This means it needs less computing power, and due to this it can be often a model to initially measure performance.

    - The model allows for the importance of features to be viewed. We can see how important a feature might be or if it lacks a connection with the question. 
    
    - Classification is used quite often with these types of model and it can be used effectively in singular class as well as with multi-class classification when needed.  

  - Cons of logistic regression models

    - Non-linear problems can't be solved with logistic regression due to its linear nature, and this often leads to engineering more features and transforming the data to answer the questions someone might pose.

    - Logistic regressions requires a large dataset and also an ample amount of training examples for it to succeed in classification.

    - Due to the simplistic nature of the model, it struggles with complex relationships. This model can be outperformed quite easily by Neural Networks if you are willing to invest the time and capital to create one.


