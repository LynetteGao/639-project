---
header_title: Data Description
header_intro: 
layout: page
permalink: /:basename/
---
## Dataset

The dataset we used was the Real-world Affective Face Database (RAF-DB). RAF-DB contains 29672 diverse facial images downloaded from the Internet. These images are mannullay given labels. These labels include 7 basic facial expressions - surprise, fear, disgust, happiness, sadness, anger, and neutral - as well as 11 compound facial expression labels. Considering the complexity and the goal of our project, we thought the compound facial expression labels were not necessary for our project and decided to use only basic facial expression labels. We got the authorization for the use of this database from its authors.

(Image to put here)

## Data Pre-processing

RAF-DB has 15339 facial images among which each is labeled with only one of seven basic facial expressions. These images are divided into 12271 training samples and 3068 testing samples. Firstly, we resized each image into 100 x 100 pixels. Then we applied Gaussian smoothing to remove noise as well as normalization. At last, we converted the processed images and the label information into numpy arrays in the shapes of (size of the datasets, width, height, 3) and (size of the datasets, 7).