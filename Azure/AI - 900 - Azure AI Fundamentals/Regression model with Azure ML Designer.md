# Create a regression model with Azure ML designer

## Identify regression ML scenarios
- Relationships between variables to predict a desired outcome

## Azure ML designer

Use to train, test and deploy ML models.

Drag and drop interface - can orchestrate pipelines

Each design project, known as pipeline
- organize, manage and reuse complex machine learning workflows across projects and users
- components - encapsulates one step in a ML pipeline
- datasets 

Azure ML jobs
- executes  a task against a specified compute target
- systematic tracking  for your ML experimentationa nd workflows
- maintains a run record 

## Understand steps for regression

- Prepare data
    - identify features and label in the dataset, pre process, transform and clean data as needed
- Train model
    - dataset with historical features
    - charecteristics of the entity for which you want to make a prediciton and known label values
    - label is the quantity you want to train a model to predict
    - use the score model component to generate the predict class label value
- Evaluate performance
    - Mean Absolute Error (MAE) 
        - average difference between predicted and true values
        - same units as the label 
        - lower the value the better
    - Root Mean Squared Error (RMSE)
        - square root of the mean squared diference between predicted and true
        - same units as the label
        - larger difference between MAE and RMSE indicates a greater variance in the individual errors
    -  Relative Squared error (RSE)
        - between 0 and 1
        - square of the difference between predicted and true
        - closer to 0 the better
        - can be compared to other models
    - Relative Absolute Error (RAE)
        - between 0 and 1
        - absolute differences between predicted and true
        - closer to 0 the better
        - can be compared to other models
    - Coefficient of determination (R²)
        - R-squared
        - summarizes how much of variance between predicted and true
        - closer to 1 the better 
- deploy a predictive service
    - Inference pipeline
        - convert trainign pipeline to a real-time inference pipeline
        - adds web services inputs and outputs to handle requests
        - perform the same data transformations as the training one
        - the model infer label values based on its features
        - Deployment
            - can be deployed as a endpoint
            - view deployment details, test pipeline and find credential to connect to a client app
