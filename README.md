# Customer Churn Prediction using ANN

## Overview

This project uses an Artificial Neural Network (ANN) to predict customer churn for a bank. The model is built using TensorFlow and Keras. It is trained on a dataset containing customer information such as demographics, credit score, and transaction history. To prevent overfitting and improve generalization, techniques like dropout and early stopping are employed during the training process.

## Dataset

The dataset used in this project is the "Churn_Modelling.csv" file. It contains information about 10,000 bank customers. The target variable is "Exited", which indicates whether the customer churned (1) or not (0).

## Methodology

1. **Data Preprocessing:** The dataset is cleaned and preprocessed, including handling categorical variables using one-hot encoding and scaling numerical features using StandardScaler.
2. **Model Building:** An ANN is built using the Keras Sequential API. The model consists of an input layer, two hidden layers with ReLU activation, and an output layer with a sigmoid activation function. Dropout layers are added to the hidden layers to randomly drop out neurons during training, reducing overfitting.
3. **Model Training:** The model is trained using the `fit` method with a batch size of 10 and 50 epochs. Early stopping is implemented to monitor the validation loss and stop training if it starts to increase, preventing overfitting and saving training time.
4. **Model Evaluation:** The model's performance is evaluated using metrics such as accuracy and the confusion matrix.
5. **Prediction:** The trained model is used to predict customer churn on a test dataset.

## Results

The model achieved an accuracy of approximately 86% on the test dataset. By utilizing dropout and early stopping, the model demonstrates good generalization capabilities and avoids overfitting to the training data.