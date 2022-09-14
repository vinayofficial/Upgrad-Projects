# Project Name
> Melanoma Detection Using CNN


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Project: Melanoma Detection
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


- The business probem that your project is trying to solve and Dataset Used?
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion
 

## Conclusions
- ### Model 1 :
The first Model 
- The input to the network is an image of dimensions (180, 180, 3). The first two layers have 32 channels of a 3*3 filter size and the same padding. 
- Then after a max pool layer of stride (2, 2), 
- Then a convolution layer of 32 filter size and filter size (3, 3). This is followed by a max-pooling layer of stride (2, 2) 
- Then a convolution layer of filter size (3, 3) and 64 filters.This is followed by a max-pooling layer of stride (2, 2) 
- Then a convolution layer of filter size (3, 3) and 64 filters.This is followed by a max-pooling layer of stride (2, 2)
- Then We flatten this output. After this there is a fully connected layer. fully connected layer is used to implement softmax function to classify 9 classes. All the hidden layers use ReLU as its activation function. ReLU is more computationally efficient because it results in faster learning and it also decreases the likelihood of vanishing gradient problems.

- #### Key Observations
*   The training 69% and validation 51% accuracy are different 
*   Validation Accuracy is much lesser than Training accuracy.


*   The difference in training and validation accuracy shows the clear case of model being overfit
*   The training accuracy increases with increase in epochs. 
*   The validation accuracy shows is stable and decreases with increase in epochs. 
*  The Validation loss and follows the training loss till 10 epochs approx and then validation loss increases and training loss further decreases with number of epochs


- ### Model Revision with Data Augmentation:
- Problem Identification
Uneven dataset: The training dataset the distribution of image are uneven.
seborrheic keratosis:77
squamous cell carcinoma:181
vascular lesion:139
actinic keratosis:114
The samples in above cases are very less in comparison to 
the other cases. So we need to increase the samples in each case.
**we attempt to use DATA AUGMENTATION tecbhnique**
* After Data Augmentation *
- #### Key Observations
The training accuracy and validation accuracy are almost equal
They follow similar trends
Although the training accuracy 52%
And validation accuracy 53% has decreased.
The problem of overfitting has been addressed with data augmentation as both accuracies almost follow each other.
But we have the decreased accuracies with needs to be addressed

- ### Model 3,With Model Augmentor
This is the final model created by adding more images. 500+ images to each dataset.
With Augmentor we increased the number of samples by 500 in each of the classes. This make the difference in ratio less and between each each class.

- #### Final Model Observations
- The accuracy of test set is 90%
- Accuracy of validation dats set is 80%
- Here we went for some extra epochs to try if the model gets improved. But, infact the model tend to increase the overfitting once we for extra epochs.
- The model with the above accuracy shows an increased performace of the model when we get a class balanced training data.
- As we can see from the model performace on the augmented data. 




## Technologies Used
- Google Colab
- Python
- Tensorflow