---
header_title: Result
header_intro: At the end, we have a model of 78% test accuracy and as small as 62 Mb.
layout: page
permalink: /:basename/
---
### (1) Example Prediction

Now let's see several predictions from our model.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/happy.jpg?raw=true)

Prediction: {'Surprise': 2.3320655e-07, 'Fear': 5.58155e-05, 'Disgust': 2.374874e-06, 'Happiness': 3.5501657e-06, 'Sadness': 5.6060514e-07, 'Anger': 0.99993706, 'Neutral': 3.3376318e-07}

Target: 'Happy'

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/anger.jpg?raw=true)

Prediction: {'Surprise': 2.3320655e-07, 'Fear': 5.58155e-05, 'Disgust': 2.374874e-06, 'Happiness': 3.5501657e-06, 'Sadness': 5.6060514e-07, 'Anger': 0.99993706, 'Neutral': 3.3376318e-07}

Target: 'Angry'

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/surprise.jpg?raw=true)

Prediction: {'Surprise': 0.8675977, 'Fear': 0.022418853, 'Disgust': 0.011015029, 'Happiness': 0.0014342658, 'Sadness': 0.060660016, 'Anger': 0.036131866, 'Neutral': 0.0007421497}

Target: 'Surprise'

From the example output above, we can tell that

### (2) Feature map visualization

In order to better understand the effect of each convolution layer, we decided to visualize the activation maps which capture the the result of applyting the filters to the input.

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer1.png?raw=true)

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/layer2.png?raw=true)

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.

## Person 3

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.