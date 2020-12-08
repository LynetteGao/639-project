---
header_title: Approach
header_intro: Lorem ipsum dolor sit amet, vel feugiat nunc. Non libero ornare lectus, id in ante nam erat sollicitudin ut, ac mi. Adipisicing at euismod ac. Id eleifend massa morbi, odio dis, mauris elit facilisi. Ultrices purus, leo suscipit lorem nulla vitae hendrerit nam, ut non.
layout: page
permalink: /:basename/
---
## Person 1

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

## VGG

With a basic understanding of how deep learning network works from our previous step, we decided to take a look at the very-deep network in order to further improve our model’s accuracy. Therefore, in the second step of our project, we adopted one of the state-of-the-art image classification  framework – VGG16. VGG16 is proposed by University of Oxford in the paper “Very Deep Convolutional Networks for Large-Scale Image Recognition”, which is the winner of 2014 ImageNet competition.

![Cannot display](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/vgg16.png?raw=true)

Above is the architecture of VGG 16. The fundamental idea behind VGG is to pass the input through a stack of small convolution layers, followed by maxpooling and fully connected layer at the end. 

We deployed this VGG-16 architecture as our benchmark model and it achieves an accuracy of 68%. However, there is one major drawback of this setup. Due to the the depth of VGG and number of fully-connected nodes, the resulting model is over 533 MB. This makes it super slow to deploy when it comes to a real-time detection  task.

Therefore, we decided to propose a model based on vgg, but more lightweight and at the same time with an improved accuracy. 

As a reminder, the original purpose of the VGG is to fit into ImageNet, a dataset of over 14 million high-resolution images, and is able to classify 22,000 categories. 

However, in our case, we only need segmentation of 7 facial expression classes. Therefore, we decided to design our own version of modified vgg that it’s faster and smaller, thus more suitable for the real time facial expression detection task.

## Light-VGG

There are 4 major steps for our training:

First of all, we tried to lighten the weight of the model by reducing the number of CNN stacks. As we can see from the table below, when we reduce the number of CNN layers from 5 to 2, not only the test accuracy increases a bit, but also the size of the model shrinks tremendously. Given the results from this trial, we decided to pick 2 as our initial layers of cnn stacks.

![Cannot display](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/table1.png?raw=true)
