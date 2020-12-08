---
header_title: Discussion
header_intro: 
layout: page
permalink: /:basename/
---
# Comparison
The real-time prediction test is running with 2.6 GHz 6-Core Processor with 16 GB 2400 MHz memory.

- **Model Size:**

- **Real-time detector Speed:** 4 frames/seconds(0.71 second) vs 1.4 frame/second(0.25 second)

- **Memory consumption:** 62.96947MB; Peak was 103.873334MB vs memory usage is 525.965954MB; Peak was 700.50903MB

These statistics demonstrate a good potential of embedding our devised model into a real-time classification task.


# Pros
Here are some of the advantages of our light-vgg model:
1.	The running time is good compared to other models .It’s faster and smaller, thus more suitable for the real time facial expression. Detection
2.	It can achieve a relatively satisfied accuracy even with such a shallow network
3.	It is easy to implement and it does not need expensive hardware, which is ideal.

# Cons
Although the results (images and videos) show that our model is very robust to some of the extreme conditions, there are still certain cases where this model cannot work very well.

As you can see from the examples in the result section, if lots of facial features are blurred or covered in the image, our model fails to identify the result correctly. This may due to nature of the low-complexity model, which may cause trouble when it comes to some complicated scenes.

# Conclusions
In conclusion, from this project, we have a better understanding of the learning-based computer vision and some of its techniques. In addition, we gained more insights into deep learning models, including architecture and tuning of the model. 

Some of the further improvements may include image augmentation in the first phase. Also, we can think about using some pre-trained model and then apply transfer learning to further increase accuracy. 


<span class="fa-stack">
  <i class="fa fa-circle fa-stack-2x"></i>
  <i class="fa fa-download fa-stack-1x fa-inverse"></i>
</span> <a href="/documents/example.pdf">&nbsp;Example (pdf)</a>
