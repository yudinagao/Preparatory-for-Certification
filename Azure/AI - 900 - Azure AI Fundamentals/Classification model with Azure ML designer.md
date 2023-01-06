# Classification model  with Azure ML designer

Classification
- form of ML used to predict the which category, or class and item belgons to
- can be applied to binary and multi-class
- supervised ML technique

## Steps for classification

- Prepare data
    - identify features and label in the dataset, pre process, transform and clean data as needed
- Train model
    - dataset with historical features
    - charecteristics of the entity for which you want to make a prediciton and known label values
    - label is the quantity you want to train a model to predict
    - use the score model component to generate the predict class label value
- Evaluate performance
    - Confusion Matrix
        - show cases where both predicted value and true values were 1 ( true positives) at top left
        - show cases where both predicted an true values were 0 (true negeatives at bottom right)
        - the other cells predicted and true are different  
        - metrics evaluated
            - accuracy - most intuitive (need careful examination)
                - ratio of correct predictions (true negatives na dpositives) to the total number of predictions
            - precision 
                - the fraction of cases classifies as positive that are actually positive
                - number of true positives divided by number of total positives
            - Recall
                - fraction of positive cases correctly identified
                - number of true positives divided by tru positives + true negatives
            - F1 Score
                - overall metric that essentially combines precision and recall
        - Choosing a threshold
            -  predicts the probability for each possible class
        - ROC curve and AUC metric
            - recall = true positive rate
            - corresponding true negative rate
            - plotting the metrics agaisnt each other for every possible threshold results in a curve knows as ROC curve ( receiver operating characteristics)
            - ideal model
                - the curve would go all the way up to the left side across the top so it cover all the chart
            - the larger the area under the curve, of AUC metric the beeter the model
- deploy a predictive service
    - Inference pipeline
        - convert trainign pipeline to a real-time inference pipeline
        - adds web services inputs and outputs to handle requests
        - perform the same data transformations as the training one
        - the model infer label values based on its features
        - Deployment
            - can be deployed as a endpoint
            - view deployment details, test pipeline and find credential to connect to a client app