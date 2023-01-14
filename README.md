

# Introduction
This repository contains the various AI and interactive graphics project files.

First Exploratory Data Analysis will be done on the dataset, then various convolutional neural networks capable of performing facial expression recognition will be implemented and their performances will be compared.

To run the files from this repository you need to add this [folder](https://drive.google.com/drive/folders/1WnDjOJArsUH-G_ffOXXO7D7dZCs9lLyH?usp=sharing) to your Google Drive.\
The folder contains the dataset (which can be downloaded from [here](https://www.kaggle.com/competitions/challenges-in-representation-learning-facial-expression-recognition-challenge/data)) and the files relating to the various previously trained CNNs.

# Exploratory Data Analysis
Exploratory data analysis is an essential tool for analyzing the dataset and understanding its peculiarities.\
Thanks to it, it's possible to grasp important aspects of the dataset such as imbalances between classes, missing values, etc.

The `Exploratory_Data_Analysis.ipynb` file implements the EDA on the dataset, displaying among other things a sample of images and the histogram of the classes, which allows us to understand how these are distributed.

![EDA_image1](https://github.com/matteo-bertini/Facial-Expression-Recognition/blob/main/data/EDA.png)

In particular, looking at the generated histogram of the classes, it can be seen that the "disgust" class has far fewer images than the other classes, so it will be necessary to do data augmentation to balance the dataset and efficiently train the implemented models.

# Five-Layers-CNN

# ResNet


