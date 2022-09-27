# Tree Bark Image Classification
This is a multi-class image classification challenge to classify tree barks from 50 categories of bark texture images.

## About Dataset
BarkVN-50 consists of 50 categories of bark texture images. Total number is 5,578 images with 303× 404 pixels. Image classification task can be performed on this dataset.

DataSource :- https://www.kaggle.com/datasets/saurabhshahane/barkvn50

## Creating required directory structure
Before we can go through with training our deep learning models, we need to create the required directory structure for our images.
We need our images to be contained in 2 folders train and test. Train folders contain directory of different bark image categories which are used to train the model.
Test folder cantain the directory of different bark image categories which are used to validate and test the model.

## Data Augmentation
By dividing the dataset into train and test by 80:20, the amount of data to train the model decreases. There are some categories which have less number of images in it. Inorder to increase the number of images we use ImageDataGenerator, to generate new image data from existing images.
Several operations are perfomed : -
* horizontal_flip : - used to filp image horizontally
* rotation_range : - used to rotate image to specific degree
* zoom_range :- zoom the image to specific range
* height_shift_range :- shift the height to specific range

## Model Training

### VGG19 Model

* VGG19 is used for image feature extraction along with CNN layers and pre-trained weights are used for model initiation.
* Four layers of fully connected layers along with relu activation function inorder to add non-linearity
* Dropout layers and earlystopping are also added to prevent overfitting
* Finaly layers has 50 neurons for 50 categories and softmax activation function for multi classification
* VGG19 model secured an accuracy of **59%**

### ResNet101V2

* ResNet101V2 is used for image feature extraction along with CNN layers and pre-trained weights are used for model initiation.
* Four layers of fully connected layers along with relu activation function inorder to add non-linearity
* Dropout layers and earlystopping are also added to prevent overfitting
* Finaly layers has 50 neurons for 50 categories and softmax activation function for multi classification
* ResNet101V2 model secured an accuracy of **70%**
