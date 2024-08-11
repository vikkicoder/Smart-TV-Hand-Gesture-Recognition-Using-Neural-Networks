# Gesture Recognition using Artificial Neural Networks

by 

Vishnu Vardhan Gudla

# Problem Statement:

Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

* Thumbs up:  Increase the volume
* Thumbs down: Decrease the volume
* Left swipe: 'Jump' backwards 10 seconds
* Right swipe: 'Jump' forward 10 seconds  
* Stop: Pause the movie

## Data Understanding:

* The training data consists of a few hundred videos categorised into one of the five classes.
* Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images).
*  videos have two types of dimensions - either 360x360 or 120x160 (depending on the webcam used to record the videos)


* Data can be downloaded from: https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL



## Table of Contents
* Importing Necessary Libraries
* Importing Video Data
* Generator Function for sending data through N.N in batches 
* Visualize the Data
* Modelling the Neural Network
	i) 3D CNN
	ii) 2D CNN + ConvLSTM
* Conclusions


## Technologies Used
* TensorFlow
* keras
* NumPy
* Imageio 
* Scikit - Image



## Conclusions
* After iterations with trail and error, two models are considered Conv3D and combination of Conv2D and ConvLSTM. various Iterations of batch_size , Epochs, learning rate are considered to get the best outcome

* 3D CNN has a training accuracy of 74.7% and low validation accuracy of 40.6% with batch siz. 

* It is observed that, Conv2D + ConvLSTM gives the best results with maximum training accuracy of 94% and validation accuracy of 84%.

* Hence, Conv2D + ConvLSTM model with batch_size of 32, number of epochs as 50, learning rate of 0.01 with Adam as optimizer is best choice for the problem statement.


