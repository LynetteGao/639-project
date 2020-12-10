---
header_title: Approach
header_intro:
layout: page
permalink: /:basename/
---
## Phase 1: CNN

Firstly, we took a look at a very fundamental CNN model. This model had much simpler architecture than state-of-art models. It turned out to be composed of two convolutional layers, one maxpooling layer, and one fully connected layer. Each convolutional layer had 128 filteres, a kernel with size of 3, and ReLU activation. After some tuning, a drop-out layer with a frequency of 0.1 was added between the maxpooling layer and the fully connected layer. The model cost **200 epoches** to train until convergence and its test accuracy turned out to be **0.65**.

We tried some other ways of tuning, but those did not seem to be effective. We added L1 regularizer in each convolutional layer. The effect of overfitting was indeed reduced, but the test accuracy was decreased to 0.61, which was not we want. Also, we tried to change the optimizer from Adadelta to Adam, but this largely amplified overfitting.

The best test accuracy can be achieved by this model was **0.65**, but this was not very satisfying. We expected that some other models could perform better.

## Phase 2: VGG

With a basic understanding of how deep learning network works from our previous step, we decided to take a step forward to take a look at the very-deep network in order to further improve our model’s accuracy. Therefore, in the second step of our project, we adopted one of the classic state-of-art image classification  framework – VGG16. VGG16 is proposed by University of Oxford in the paper “Very Deep Convolutional Networks for Large-Scale Image Recognition”, which is the winner of 2014 ImageNet competition.

![Cannot display](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/vgg16.png?raw=true)

Above is the architecture of VGG 16. The fundamental idea behind VGG is to pass the input image through a stack of small convolution layers, followed by maxpooling and fully connected layer at the end. 

We deployed this VGG-16 architecture as our benchmark model and it achieves an accuracy of 68%. However, there is one major **drawback** of this setup. Due to the the depth of VGG and number of fully-connected nodes, the resulting model is over 533 MB. **This makes it super slow to deploy when it comes to a real-time detection  task.**

Therefore, we decided to propose a model based on vgg, but more lightweight and at the same time with an improved accuracy.

The reasoning behind this idea is that the original purpose of the VGG is to fit into ImageNet, a dataset of over 14 million high-resolution images, and it is able to classify 22,000 categories. However, in our case, we only need segmentation of 7 facial expression classes. **That's why we decided to design our own version of modified vgg that it’s faster and smaller, thus more suitable for the real time facial expression detection task.**

## Phase 3: Light-VGG

There are 4 major steps for our training:

First of all, we tried to lighten the weight of the model by reducing the number of **CNN stacks**. As we can see from the table below, when we reduce the number of CNN layers from 5 to 2, not only the test accuracy increases a bit, but also the size of the model shrinks tremendously. Given the results from this trial, we decided to pick 2 as our initial layers of cnn stacks.

![Cannot display](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/table1.png?raw=true)

Secondly, we tried to modify the fully connected layers to see if it can help to improve the accuracy from the previous step. We conducted experiments on different number of **dense blocks**.

|#Dense blocks   	| Accuracy 	| Size  	|
|---	|----------	|-------	|
| 4 	| 71%      	| 262Mb 	|
| 3 	| 72%      	| 65Mb  	|
| 2 	| 74%      	| 62Mb  	|
| 1 	| 72%      	| 7Mb   	|

As we can see from the table above, neither a model with excessively amount of dense blocks nor  a too simple model will help the model accuracy. The sweet spot for our task is to use 2 fully connected layers.

Once we figure out the central setup of our light-vgg model, the next step is **hyperparameter tuning**.  For example, we tuned different combinations of learning rate and optimizer in order to achieve the best learning rate decay setup. The final best parameter is to use RMsprop with learning rate of 1e-5. In addition, batch normalization is used with a batch size of 64.
Finally, we trained the models with enough epochs until convergence. At this step, in order to prevent overfitting, we added L2 regularization and dropout. 


Before adding L2            |  After adding L2
:-------------------------:|:-------------------------:
![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/before.png?raw=true)  |  ![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/after.png?raw=true)

(From this example traing, we can see that without regularization , the model would suffer a lot from overfitting.)

At the end, we trained the model for 60 epochs until convergence. Below is the **model architecture** of our devised model.


![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/architecture.png?raw=true)

                    Model architecture of Light-vgg 