# Drowsiness-Detection

Drowsiness detection is a safety technology that can prevent accidents that are caused by drivers who fell asleep while driving.
The majority of accidents happen due to the drowsiness of the driver. So, to prevent these accidents we will build a system using Python, OpenCV, and Keras which will alert the driver when he feels sleepy.

![image](https://user-images.githubusercontent.com/64821137/184025929-40d85261-4e3c-4c80-9485-e9624feae1ac.png)

## What are Haar Cascades? 

Haar Cascade is a machine learning-based approach where a lot of positive and negative images are used to train the classifier. 

* Positive images – These images contain the images which we want our classifier to identify.

* Negative Images – Images of everything else, which do not contain the object we want to detect.

In our case, we are detecting the face and eyes of the person.

## Model Architecture

The CNN model architecture consists of the following layers:

* Convolutional layer; 32 nodes, kernel size 3
* Convolutional layer; 32 nodes, kernel size 3
* Convolutional layer; 64 nodes, kernel size 3
* Fully connected layer; 128 nodes
* The final layer is also a fully connected layer with 2 nodes. A Relu activation function is used in all the layers except the output layer in which we used Softmax.

## Detection Approach

* Step 1 – Take image as input from a camera.

* Step 2 – Detect the face in the image and create a Region of Interest (ROI).

* Step 3 – Detect the eyes from ROI and feed it to the classifier.

* Step 4 – Classifier will categorize whether eyes are open or closed.

* Step 5 – Calculate score to check whether the person is drowsy.
