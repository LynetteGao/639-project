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

Target: 'Sadness'
![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/sadness.jpg?raw=true)

{'Surprise': 0.020001482, 'Fear': 0.00813411, 'Disgust': 0.03032325, 'Happiness': 0.021574635, **'Sadness': 0.44737974**, 'Anger': 0.009679649, **'Neutral': 0.4629071**}


**As we can see from the sample output above, in most of the conditions, our model is able to produce a correct output with a high confidence score.** However, there exist some extreme cases(e.g most of the facial features are covered) where our model fails to produce the most accurate prediction.

### (2) Feature map visualization

In order to better understand the effect of each convolution layer, we decided to visualize the activation maps which capture the the result of filters of each layer.

We can see that the result of applying the filters in the first convolutional layer is a lot of versions of the facial image with different features highlighted. For example, some highlight the general foreground features or the detailed features, like eyes and mouths.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer1.png?raw=true)

In the second main blocks(image below), we can see that as we progress deeper into the model, the feature maps show less details. This pattern was to be expected, as the model abstracts the features from the image into more general concepts that can be used to make a classification. However, in this case, we lose the ability to interpret these deeper feature maps.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer2.png?raw=true)


### (3) Real-time application

Combined with a pretrained HAAR cascade as a face detector(available in openCV), we are able to build a real-time facial expression program. In this case, the user is able to use their webcam as a detector for getting the real-time facial images.

The demo can be found on the [project presentation video](https://drive.google.com/file/d/1It5W_U9FhxjvdFRcfHL4kpkT3KWDyX7G/view?usp=sharing).(5'57" - 6'20")


As you can see, this program is able to generate a real-time prediction on the facial expression without much lagging. This also demonstrates the potential that how this model can be applied to the real life.
