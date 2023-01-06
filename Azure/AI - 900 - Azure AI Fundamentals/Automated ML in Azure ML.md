# Automated ML in Azure ML

## What is Machine Learning
Technique that uses mathematics and statistics to create a model that can predict unknown values

General approaches to ML> Supervised and Unsupervised

Types of Supervised ML
- Regression
    -   predict a continous value
- Classification
    - determine a class label
Types of Unsupervised ML
- Clustering
    - determine labels by using grouping similar information

## Azure Machine Learning Studio
Cloud-based service that helps simplifies some of the tasks it takes to prepare data, train a model and deploy a predictive service

Automating many consuming tasks associated with trainign models

Create a workspace to manage data, compute resources, code, models and other artifacts

Azure ML Studio is a web portal for ML solutions
- 4 types of compute resourecs
    - Compute Instances - dev workstations for Data sCientists can use to work with data and models
    - Compute clusters - scalable clusters of VM for on-demand processing experimental code
    - Inference Clusters - deployment targets for predictive services
    - Attached compute - links to existing Azure Compute resources - azure databricks or VM

## Azure Automated ML

Capability that automatically tries multiple pre-processing techniques and model-training algorithms in parallel - to find the best supervised ML model for your data

Jobs - configure multiple settings for your job before starting an automated ML run. The run configuration provides information needed to specify your training script, compute target and azure Ml environment

Steps in ML:
- Prepare the data
    - Identify the features and label in a dataset, Pre-process, clean and transform the data as neeeded
    - 
- Train Model
    - Split the data in 2 groups: training and validation set. Train and validate using the respective dataset
    - supports supervised models
        - Classification
        - regression
        - Time series forecasting
    - can select configurations for the primary metric, type of model used for training, exit criteria and concurrency limits
- Evaluate performance
    - Compare how close the model's predictions are to know label
    - afeter finished, you can review the best performing model - note: you find the best model within the time you allowed for you exit criteria
    - The best model is identified using the evaluation metric: normalized root mean squared error
    - cross-validation is used to calculate the evaluation metric - comparing the predicted value and the actual know value
    - residuals = known value - predicted value - indicates the amount of errorin the model
    - RMSE squaring the errors of all the test cases, mean of the sqaures, then taking the root sqaure - meaning the smaller this value the more accurate is the model
    - Residual Histogram shows the frequency of residual values ranges. Better to see more ocurring residuals values clustered around zero
    - Predicted vs true chart:
        - diagonal trend in which the predicted value correlates to the true value

- Deploy a predictive service
    - after evaluated, you can deploy the model as an application on a server or device for others to use
    - Deploy a service as an Azure Container Instance (ACI) or as an Azure Kubernetes Service (AKS)
        - for production scenarios - AKS
        -