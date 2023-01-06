# Clustering model with Azure ML Designer

Clustering
- used to group similar item into clusters based on their features
- unsupervised ml technique

# Steps for clustering
- Prepare data
    - identify features and label in the dataset, pre process, transform and clean data as needed
    - for clustering need a dataset that includes multiple observations of the items you want to clsuter
    - numercis features that can be used do determine similarities between individual cases that will help separate them into clusters
- Train model
    - K-means Clustering algorithm groups item into the numbers of clusters, or centroids you specificy, - vaue known as k
        - Initializing k  coordinates as randomly selected points called centroid in n-dimensional space
        - plotting the features vectors as points in the same space, and assiging each poitn to the closest centroid
        - moving the centroids to the middle of the points acllocated to it (mean distance)
        - Reassinging the points to the closest centroid after the move
        - repeate the same process until stabilize orthe specified number of iterations
- Evaluate performance
    - Average distance to other center
        - this indicates how close, on average,     each point in the cluster is to the centroids of other clusters
    - Average distance to cluster center
        - how close, on average, each point in the cluster is to the it's centroid
    - Number of points
        - number of point assigned to the cluster
    - Maximal distance to cluster center
        - maximum distances between each point and the centroid 
        - high number = cluster may be widely dispersed
        - statistic combination with average distance to cluster center helps determine cluster spread
- deploy a predictive service
    - Inference pipeline
        - convert trainign pipeline to a real-time inference pipeline
        - adds web services inputs and outputs to handle requests
        - perform the same data transformations as the training one
        - the model infer label values based on its features
        - Deployment
            - can be deployed as a endpoint
            - view deployment details, test pipeline and find credential to connect to a client app