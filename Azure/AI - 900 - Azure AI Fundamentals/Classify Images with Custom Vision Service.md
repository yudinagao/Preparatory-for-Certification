# Classify Images with Custom Vision Service

## Understand classification

Predict which category something belons to

Classification ML models use a set of inputs, features, to calculate the probability score for each possible class and predict a label that indicates the most likely class

Image classification 
- to create an image classification model, you need data that consists of features and thier labels
- existing data is a set of categorize images
- images are made of array of pixel values, and these are used as features to train the model based on the image classes
- model is trained to match the patterns in the pixel values to a set of class labels
- after it's trained, you can use it with new sets to predict unknown label values

## Azure Custom Vision Service

- based on Deep Learning techiniques that use convolutional neural Networks (CNN) to uncover patterns in the pixels that correspond to particular classes.
- Commom tech used in image classification are encapsulated int Custom vision
- make it easier to train models and publish as a software service

- Custom Vision
    - dedicated service 
        - training
        - prediction
- Cognitive service
    - general service
        - includes other cognitive services
        - training 
        - prediction
Separate training and prediction to track resources utilization

- Model Training
    - upload images to training resources and label them
    - perform these tasks in the Custom Vision portal or you can use the SDK
    - key consideration: sufficient images of the objects in question and images should be in different angles
- Model Evaluation
    - Precision
        - what percentage of the class prediction made by the model were correct
    - Recall
        - what percentage of the class predicion did the model correctly identify
    - Average Precision (AP) 
        - overall metric that takes in account both precision and recall
- Model prediction
    - ProjectID
    - Model Name
    - Prediction endPoint
    - Prediciton Key
    