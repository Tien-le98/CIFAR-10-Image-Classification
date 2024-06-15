# CIFAR-10 Image Classification

_Author: Clara Le_

_Date: 31/10/2023_

___

## Introduction
Image classification are becoming more important in various industry fields. For example, in autonomous automobile manufacture, image classification are necessary because it can support self-driving cars in detecting and recognizing other objects such as other vehicles, pedestrians, animals, traffic lights on the road. In healthcare system, image classification can support health professionals in diagnosing diseases such as lung disease, heart disease, and cancer. In addition, image classification can be used to automatically categorize products on e-commerce websites, which can result in better customer’s experience because customers can find relevant products quickly. Image classification also can promote the development of security sector such as surveillance, and facial recognition, since it can be used to identify person, objects, and then potential threats can be addressed quickly. Due to various applications of image classification, this project aims at developing a Convolution Neural Network (CNN) which can perform image classification task well, using CIFAR-10 dataset. Particularly, several CNN architectures were conducted, and a comparison between these architecture’s performance was carried out to find out a CNN model which can achieve the best performance, and generate good prediction on unknown datasets.

## Experiments
The CIFAR-10 dataset was downloaded from [https://www.cs.toronto.edu/ ̃kriz/cifar.html/], it comprises 60000 32x32x3 images, meaning that each image has 1024 pixels, along with three channels for red, green, and blue (RGB). The first layer of 1024 entries is the red channel, the second layer of 1024 entries represents for the green channel, and the last layer of 1024 entries represents for the blue channel. Among these images, 50000 images were used for training models, stored in 5 training batches, and 1 testing batch included 10000 images. Both training and testing dataset included 3072 columns, representing for 3072 image’s pixels, and 1 column showing image’s labels. Ten classes comprised in this dataset are vehicles such as airplane, automobile, ship, truck, and animals such as bird, cat, deer, dog, frog, and horse. Each class had 10000 images, their respective labels were shown in the below table, and their images were also shown in the below figure.
|Label|Class|Label|Class|
|:--|:--|:--|:--| 
|0|airplane|5|dog|
|1|automobile|6|frog|
|2|bird|7|horse|
|3|cat|8|ship|
|4|deer|9|truck|

<a href="url"><img src="https://github.com/Tien-le98/CIFAR-10-Image-Classification/blob/main/image_label.png" align="center" height="300" width="700" ></a>

This CIFAR-10 dataset was employed to perform data cleaning, data pre-processing, EDA, and data splitting before applying CNN models. Besides, various data augmentation methods for images such as flipping, rotation, and contrast were also utilised. In addition, many CNN architectures were applied on the dataset, including Visual Geometry Group (VGG16), GoogLeNet, InceptionV3, and ResNet-50.



