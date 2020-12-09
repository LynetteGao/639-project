---
header_title: Discussion
header_intro: 
layout: page
permalink: /:basename/
---
# Comparison
Here we are comparing our light-version vgg with the vgg16 model. The real-time prediction test is running with 2.6 GHz 6-Core Processor with 16 GB 2400 MHz memory.

- **Model Size:** 62MB vs 533MB, **1/10 of the size**

- **Real-time processing Speed:** 4 frames/second vs 1.4 frame/second, **x3 faster**

- **Average Memory consumption:**  62.96947MB vs 525.965954MB, **90% less memory consumption**

These statistics demonstrate a good potential of embedding our devised model into a real-time classification task comparing to a very-deep vgg.


# Pros
Here are some of the advantages of our light-vgg model:
1.	The running time is good compared to other models. It’s faster and smaller, thus more suitable for the real time facial expression detection.
2.	It can achieve a relatively satisfied accuracy even with such a shallow network
3.	It is easy to implement and train since it does not need expensive hardware.

# Cons
Although the results (on images and real-time) show that our model is very robust to most of the normal conditions, there are still certain cases where this model cannot work very well.

As you can see from the examples in the result section, if lots of facial features are blurred or covered in the input image, our model fails to identify the facial expression correctly. This may due to nature of such a low-complexity model, which may cause trouble when it comes to some complicated scenes.

# Conclusions
In conclusion, from this project, we gain a better understanding of the learning-based computer vision and some of its techniques. In addition, we gained more insights into deep learning models, including architecture and tuning of the model. 

Some of the further improvements may include image augmentation in the first phase. Also, we can think about using some pre-trained model and then apply transfer learning to further increase accuracy. 

![](https://github.com/LynetteGao/639-project/blob/LynetteGao-main-page/pages/thankyou.png?raw=true)
