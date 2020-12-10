---
header_title: State-of-art
header_intro: Current deep learning networks useful in the deep facial expression recognition task include CNN, DBN, DAE, RNN, and GAN. The methods that are good at the face detection task include Haar Cascade and YOLO.
layout: page
permalink: /:basename/
---
# Deep Learning Networks

## Convolutional Neural Network (CNN)

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

## Deep Belief Network (DBN)

## Deep Autoencoder (DAE)

## Recurrent Neural Network (RNN)

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

## Generative Adversarial Network (GAN)

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

# Face Detection Methods

## Haar Cascade

Haar Cascade method is one of the most popular methods that have been chosen for the object detection tasks. It uses Haar-like features, which are good at extracting featured information from a given image at a high speed. Haar-like fearture can be computed efficiently with the help of the integral image. Then AdaBoost algorithm is used remove unrelated features from all calculated Haar-like features. At last, cascade classifer is used to speed up the process of detection.

## You Only Look Once (YOLO)

YOLO has been a very popular system used for the object detection tasks since it was proposed in 2016. It can provide end-to-end predictions given raw images. One of its advantages is that it is very fast, since it uses its own convolutional network instead of a complicated pipeline of several algorithms. Also, instead of making predictions based on several windows from the image, YOLO considers the whole image when making predictions, so it produces relatively less errors on the background than most of other methods. However, one drawback of YOLO is that it is not so good at localization of objects in the image, especially small objects in groups.