---
header_title: State-of-art
header_intro: Current deep learning networks useful in the deep facial expression recognition task include CNN, DBN, DAE, RNN, and GAN. The methods that are good at the face detection task include Haar Cascade and YOLO.
layout: page
permalink: /:basename/
---
# Deep Learning Networks

## Convolutional Neural Network (CNN)

CNN is a popular deep learning network that has been widely in many tasks in the field of computer vision, including the facial expression recognition task. Basically, a CNN consists of three types of layers: convolutional layers with activation, pooling layers, and fully connected layers. The benefits of convolution include learning correlations among adjacent pixels in the image and sharing weights throughout the whole image. The latter reduces the parameters to be computed and hence increases the speed of training. The pooling layers serve to decrease the size of feature maps and to increase the computing speed. The fully connected layers convert feature maps from 2D to 1D for the final label classifications.

Scholars have researched on CNN since it was released, and many specific CNN models with great performances have appeared. These models include AlexNet, VGGNet, GoogleNet, and ResNet. AlexNet was proposed in 2012. VGGNet and GoogleNet were proposed in 2014. ResNet was proposed in 2015. The newer the model is, the more layers it has. Among these models, the newest model, ResNet, appears to have the best performances in many tasks. Since we were not very professional in this area, we chose a relatively simple model, VGGNet, to investigate in this project.

## Deep Belief Network (DBN)

DBN is a deep learning model that makes use of graphs. It can be useful in extracting hierarchical information of the training data. It is usually composed of several Boltzmann machines, each of which has two layers, one with visible units and the other with hidden units, that form a bipartite graph. The two steps to train a DBN is firstly pre-training the network in an unsupervised manner and then fine-tuning parameters with gradient descents in a supervised manner.

## Deep Autoencoder (DAE)

DAE was first proposed for the task of dimensionality reduction. Training DAE is not like training other deep learning networks. Instead of being trained to give favorable outputs, DAE is trained to reconstruct the input so that the reconstruction errors are minimized. Tasks in which it can be applied include recovering undistorted data from partially distorted data.

## Recurrent Neural Network (RNN)

RNN can collect temporal information in data and is useful in analyze sequential data. RNN has recurrent edges that utilize same parameters for multiple times. The traditional RNN has the problems of gradient vanishing and exploding. Long-short term memory (LSTM) is a speical form of RNN proposed to solve these two problems. LSTM is widely used in facial expression recognition in videos.

## Generative Adversarial Network (GAN)

GAN is a model trained through a minimax two-player game between a generator and a discriminator. Either the generator or the discriminator is trained and is improved based on the binary cross entropy. Extensions of GAN utilize techniques to make alterations on the generator or the discriminator or both.

# Face Detection Methods

## Haar Cascade

Haar Cascade method is one of the most popular methods that have been chosen for the object detection tasks. It uses Haar-like features, which are good at extracting featured information from a given image at a high speed. Haar-like fearture can be computed efficiently with the help of the integral image. Then AdaBoost algorithm is used remove unrelated features from all calculated Haar-like features. At last, cascade classifer is used to speed up the process of detection.

## You Only Look Once (YOLO)

YOLO has been a very popular system used for the object detection tasks since it was proposed in 2016. It can provide end-to-end predictions given raw images. One of its advantages is that it is very fast, since it uses its own convolutional network instead of a complicated pipeline of several algorithms. Also, instead of making predictions based on several windows from the image, YOLO considers the whole image when making predictions, so it produces relatively less errors on the background than most of other methods. However, one drawback of YOLO is that it is not so good at localization of objects in the image, especially small objects in groups.