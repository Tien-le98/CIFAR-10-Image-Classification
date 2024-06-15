# CIFAR-10 Image Classification

_Author: Clara Le_

_Date: 31/10/2023_

___

## Introduction
Image classification are becoming more important in various industry fields. For example, in autonomous automobile manufacture, image classification are necessary because it can support self-driving cars in detecting and recognizing other objects such as other vehicles, pedestrians, animals, traffic lights on the road. In healthcare system, image classification can support health professionals in diagnosing diseases such as lung disease, heart disease, and cancer. In addition, image classification can be used to automatically categorize products on e-commerce websites, which can result in better customer’s experience because customers can find relevant products quickly. Image classification also can promote the development of security sector such as surveillance, and facial recognition, since it can be used to identify person, objects, and then potential threats can be addressed quickly. Due to various applications of image classification, this project aims at developing a Convolution Neural Network (CNN) which can perform image classification task well, using CIFAR-10 dataset. Particularly, several CNN architectures were conducted, and a comparison between these architecture’s performance was carried out to find out a CNN model which can achieve the best performance, and generate good prediction on unknown datasets.

The CIFAR-10 dataset was downloaded from [https://www.cs.toronto.edu/ ̃kriz/cifar.html/], it comprises 60000 32x32x3 images, meaning that each image has 1024 pixels, along with three channels for red, green, and blue (RGB). The first layer of 1024 entries is the red channel, the second layer of 1024 entries represents for the green channel, and the last layer of 1024 entries represents for the blue channel. Among these images, 50000 images were used for training models, stored in 5 training batches, and 1 testing batch included 10000 images. Both training and testing dataset included 3072 columns, representing for 3072 image’s pixels, and 1 column showing image’s labels. Ten classes comprised in this dataset are vehicles such as airplane, automobile, ship, truck, and animals such as bird, cat, deer, dog, frog, and horse. Each class had 10000 images, their respective labels were shown in the below table, and their images were also shown in the below figure.
|Label|Class|Label|Class|
|:--|:--|:--|:--| 
|0|airplane|5|dog|
|1|automobile|6|frog|
|2|bird|7|horse|
|3|cat|8|ship|
|4|deer|9|truck|

<a href="url"><img src="https://github.com/Tien-le98/CIFAR-10-Image-Classification/blob/main/image_label.png" align="center" ></a>

This CIFAR-10 dataset was employed to perform data cleaning, data pre-processing, EDA, and data splitting before applying CNN models. Besides, various data augmentation methods for images such as flipping, rotation, and contrast were also utilised. In addition, many CNN architectures were applied on the dataset, including Visual Geometry Group (VGG16), GoogLeNet, InceptionV3, and ResNet-50.

## Experiments

__Experiment 1__

The first experiment was carried out to compare model’s performance on the original dataset and the pre-processed dataset, in order to figure out if pre-processing steps are necessary for models to perform better.

A baseline CNN model was built with 1 input layer, 1 output layer with 10 neurons, using Softmax function and Sparse categorical crossentropy loss function. This baseline model contained 1 convolutional layer with 64 filters and kernel size of 3x3, followed by a 2x2 max pooling layer, a fully connected layer with 256 neurons and two Dropout layers. SGD optimizer with learning rate of 0.001 was employed in this baseline CNN model. Additionally, this model ran through 300 epochs, and batch size of 100. Early stopping method was also employed to prevent models from potential overfitting problem. The baseline model was trained on the original dataset, a dataset pre-processed with Standard scaling method, Max-Min scaling method, and other data augmentation methods (flipping, rotation, and contrast). The training accuracy score and validation accuracy score of the baseline model were shown in the below figure.

<a href="url"><img src="https://github.com/Tien-le98/CIFAR-10-Image-Classification/blob/main/baseline.png" align="center" height="300" width="700" ></a>




In terms of the original dataset, the baseline CNN model converged after around 5 epochs with the accuracy score on the training set and the val- idation set of only 10%. However, this baseline model performed better on the dataset pre-processed by only Standard scaling method, with the maximum accuracy score on the training set was about 81%, and the max- imum accuracy score on the validation set was nearly 67%, after 43 epochs. Because this accuracy score on the training set was around 14% higher than the figure for the validation set, this gap can raise a signal for po- tential overfitting problem. On the pre-processed data using only Max-Min scaling method, after 127 epochs, this baseline model obtained the accuracy score on the training dataset of about 79%, and the figure for the val- idation dataset of nearly 66%. Through this experiment, the dataset should be pre-processed before training CNN models in order to improve the model’s performance because accuracy score of models trained on the pre- processed dataset were significantly higher than the fig- ure for the original dataset. However, according to this Tab. 2, when a CNN model only contains several layers, its capability is low, data augmentation methods applied on this model can make it perform worse, which was shown by the decrease in the training accuracy score and validation accuracy score. Hence, these data augmenta- tion methods only should be considered in deeper and more complicated neural networks. Because the accu- racy score of models trained on standard scaled dataset was the highest among other methods, the pre-processed training data using Standard scaling method was used to train other CNN architectures and analyze further.

__Experiment 2__
The second experiment was implemented to find out the CNN architecture that achieved highest accuracy score for this image classification task, using the CIFAR-10, among several different architectures. 

__Experiment 3__
The third experiment was executed by applying data augmentation methods on this best architecture to figure out if these methods can improve model’s performance. 

__Experiment 4__
The last experiments was carried out by training the best CNN architecture with various values of chosen hyperparameter, to define the optimal hyperparamenters which can lead to better model’s performance.



