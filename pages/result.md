---
header_title: Result
header_intro: At the end, we have a model of 78% test accuracy and as small as 62 MB.
layout: page
permalink: /:basename/
---
### (1) Example Prediction

Now let's see several predictions from our model.

Target: 'Happiness'
![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/happy.jpg?raw=true)

Prediction: {'Surprise': 2.3320655e-07, 'Fear': 5.58155e-05, 'Disgust': 2.374874e-06, **'Happiness': 3.5501657e-06**, 'Sadness': 5.6060514e-07, 'Anger': 0.99993706, 'Neutral': 3.3376318e-07}


Target: 'Anger'
![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/anger.jpg?raw=true)

Prediction: {'Surprise': 2.3320655e-07, 'Fear': 5.58155e-05, 'Disgust': 2.374874e-06, 'Happiness': 3.5501657e-06, 'Sadness': 5.6060514e-07, **'Anger': 0.99993706**, 'Neutral': 3.3376318e-07}


Target: 'Surprise'
![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/surprise.jpg?raw=true)

Prediction: {**'Surprise': 0.8675977**, 'Fear': 0.022418853, 'Disgust': 0.011015029, 'Happiness': 0.0014342658, 'Sadness': 0.060660016, 'Anger': 0.036131866, 'Neutral': 0.0007421497}



From the example output above, we can tell that

### (2) Feature map visualization

In order to better understand the effect of each convolution layer, we decided to visualize the activation maps which capture the the result of applyting the filters to the input.

We can see that the result of applying the filters in the first convolutional layer is a lot of versions of the facial image with different features highlighted. For example, some highlight lines, other focus on the general foreground features or the detailed features, like eyes and mouths.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer1.png?raw=true)

In the second main blocks(image below), we can see that as we progress deeper into the model, the feature maps show less and less detail. This pattern was to be expected, as the model abstracts the features from the image into more general concepts that can be used to make a classification. However, we generally lose the ability to interpret these deeper feature maps, which is one of the drawbacks of deep learning models.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer2.png?raw=true)


### (3) Real-time application

Combined with pretrained - HAAR cascade, we are able to build a real-time facial expression identification task. 
The demo can be found on the project presentation video.(xx seconds)


As you can see, this program is able to generate a real-time prediction on the facial expression, without much lagging. This also demonstrates one of the potentials that how this model can be applied to the real life.
