# Detect Object with Custom Vision

## What is a object detection

- class of the object indentified
- probabilty score
- coordinates of the bounding box for each object

Image tagging
- before yout train an object detect model
    - tag classes and bounding box coordinates in a set of training images
    - time consuming
        - custom vision provides graphical interface
        - suggests areas of the images where disre object are detected  
        - you can apply a class label to these suggested areas
        - drag and adjust the bounding boxes
    - can use smart tagging
        - suggest classes and bounding boxes
    - key consideration
        - sufficient images
        - varied angles
        - bounding boxes tighly around 
    