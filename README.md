## EmberScan
A project by John Mansfield
![EmberScan Logo](https://github.com/JohnMansfield23/HouseFireIdentificationProject/blob/main/EmberScan%20Icon.png?raw=true)
### EmberScan's Mission
EmberScan is developed with the idea of using A.I image processing to identify housefires using the Alexnet.

EmberScan is a company dedicated to utilizing AI imaging technology for the vital task of identifying house fires. This approach holds significant importance because traditional smoke detectors can sometimes fail, leaving homes vulnerable to fires. EmberScan's mission is to offer a fail-safe solution to this problem by enabling home security cameras, or development cameras to detect house fires and promptly alert the appropriate authorities. This innovative use of AI image processing not only enhances fire safety but also ensures a more reliable and proactive response to fire threats, potentially saving lives and property.

## What EmberScan is trained to differentiate
![House on fire](https://www.wkrn.com/wp-content/uploads/sites/73/2021/07/thumbnail_image2.jpg) ![Normal House](https://images.ctfassets.net/n2ifzifcqscw/3HyfuHM3kAP4uLFkVYJimW/ba13d734701b3260c92376115b410c81/farmhouse.png)
## Structure of an Alexnet
![Alexnet](https://i0.wp.com/thecleverprogrammer.com/wp-content/uploads/2021/12/alexnet.png?resize=623%2C302&ssl=1)
### What is EmberScan trained off of
EmberScan is trained off the following data deck
[House Fires Data Deck](https://docs.google.com/presentation/d/1FMFFaQ2mH5CjzEbom0rSkPAUsbNTiWbb9yrRzbhVGGY/edit#slide=id.g206f8279a60_0_0)
## Filters and Feature Maps
![Filters and Feature Map](https://github.com/JohnMansfield23/EmberScan/blob/main/filters%20and%20feature%20maps.png?raw=true)
## Training accuracy and loss
![train and loss](https://github.com/JohnMansfield23/EmberScan/blob/main/Alexnet%20loss%20and%20training%20data.png?raw=true)
## Working Model utilizing Alexnet and explanation of code
[working model & high level explanation](https://colab.research.google.com/drive/1pFjAZAxK_rtj0g7iHVnzXaRSbNexpw0w?usp=sharing)
Introduction

### Code Overview

The provided code performs several tasks and utilizes various Python libraries to achieve its objectives. Here's a high-level overview of the code's functionality:

### Importing Libraries

The code starts by importing necessary Python libraries, including wandb for experiment tracking, pdf2image for PDF to image conversion, and torch for deep learning functionalities. Additionally, it imports pre-trained models from torchvision.models and other utilities.

### GPU Setup

The code checks for the availability of a GPU and assigns the computing device accordingly. This is important for leveraging GPU acceleration in deep learning tasks, which can significantly speed up model training.

### Utility Functions

Several utility functions are defined to simplify various tasks within the code, such as data preprocessing, plotting, and random data generation. These functions enhance code readability and maintainability.

### Loading a Pretrained AlexNet Model

A pretrained AlexNet model is loaded using the torchvision.models.alexnet function. This model is a deep convolutional neural network designed for image classification tasks and is known for its effectiveness in such applications.

### Loading and Preprocessing Images

The code retrieves slides from a Google Slides URL and converts them into images. These images are then preprocessed and loaded into PyTorch tensors for use with the AlexNet model. This step prepares the data for classification.

### Making Predictions

The pretrained AlexNet model is employed to make predictions (classifications) on the preprocessed images. The model's predictions are based on its understanding of the features present in the images.

### Handling Predicted Labels

The code extracts the predicted class labels from the model's output and prints them. These labels are mapped to meaningful categories using the ImageNet labels provided in the code.

### Creating Training Data

The code creates training data (X and Y) for a linear model. The data consists of 50 images divided into two classes, with 25 images in each class. One set is of houses on fire, and the other houses not on fire.

### Defining Softmax and Cross-Entropy Functions

Functions for calculating softmax and cross-entropy loss are defined. These are fundamental components for training and evaluating classification models.

### Generating Random Data

The code includes functions for generating random data, particularly truncated normal random numbers and a truncated normal distribution. These functions might be used for data augmentation or synthetic data generation.

### Training a Linear Model

The code initializes hyperparameters and weight matrices for a linear model. It then uses the Adam optimizer to train the linear model for a specified number of epochs. During training, loss and accuracy metrics are logged and tracked using Weights and Biases (wandb).

### Experiment Tracking with Weights and Biases (wandb)

Throughout the training process, the code uses Weights and Biases (wandb) to log and visualize training progress. This includes tracking loss and accuracy to monitor how the linear model is learning from the data.
## Yolo Example image and code link
![yolo example](https://github.com/JohnMansfield23/EmberScan/blob/main/yolo%20example.jpg?raw=true)
[Yolo Model Link](https://colab.research.google.com/drive/1w4r-sHo3AsEz7c60bI-0RdPIVZE3LOL_?usp=sharing)

## LLava Test
![Llava Test](https://github.com/JohnMansfield23/EmberScan/blob/main/LLaVA%20photo%20test.png)

It can be seen that LLava will make up information if it does not undesstand everything about the photo. Llava was however able to identify that the house was on fire.
