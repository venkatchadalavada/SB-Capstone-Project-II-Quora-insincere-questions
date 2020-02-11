# Quora Insincere Questions Classification
### Spring Board  Capstone Project II

#### Overview
Quora is a service that helps people learn from each other by asking and answering questions - and a key challenge in providing this type of service is filtering out insincere questions.  Quora is attempting to filter out toxic and divisive content to uphold their policy of “Be Nice, Be Respectful”.

#### Data Source
https://www.kaggle.com/c/quora-insincere-questions-classification/data

#### Goals
1. Identify and flag insincere questions using machine learning.
2. Maximize F1 score by accurately predicting whether a question is sincere or not.

#### Specializations
* Advanced NLP
* TensorFlow and Keras

#### Value of Solution
An accurate solution can help Quora develop more scalable methods to detect toxic and misleading content and combat online trolls at scale 

This solution will help Quora to uphold their policy of ‘Be Nice, Be Respectful”

#### Baseline Models Used
* Logistic Regression
* Naive Bayes
* XGBoost
* Voting Classifier

#### Deep Learning Models Used
* Convolutional Neural Network
  * Self-Trained Embedding
  * Google News Vectors
* Long Short Term Memory Network
  * Google News Vectors
  
   Here we allow the pre-trained embeddings to be updated during training and use a LSTM model.
   To date, this is the best performing model.

#### Evaluation of Models
The best performing model is the LSTM using pre-trained embeddings that we continue to update during the training of the model.  This was determined by comparing F1 scores.  All neural network models, including CNN with self-trained and pre-trained embeddings, outperform the shallow learning scikit-learn and XGBoost models.  

#### Production and Beyond
In a production environment, this model can be used to evaluate new questions as they are asked.  When the user submits a new question on Quora the model will be used to predict the sincerity of the question.  If the question is determined to be sincere it will be posted online, if insincere the user will be prompted to edit their question and resubmit.  To continue to improve the model going forward new questions and labels will be added to the training data and the model will be updated with the new information.

