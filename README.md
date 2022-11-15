# Project Name
> Multiclass classification model using a custom convolutional neural network in TensorFlow.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- **About the project:** In this project, I have built a multiclass classification model using a custom convolutional neural network in tensorflow
- **Problem statement:** To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- What is the dataset that is being used?
- **Dataset:** The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

 - Actinic keratosis
 - Basal cell carcinoma
 - Dermatofibroma
 - Melanoma
 - Nevus
 - Pigmented benign keratosis
 - Seborrheic keratosis
 - Squamous cell carcinoma
 - Vascular lesion

[Data can be found here](https://drive.google.com/file/d/1xLfSQUGDl8ezNNbUkpuHOYvSpTyxVhCs/view?usp=sharin)

**NOTE:**

- You don't have to use any pre-trained model using Transfer learning. All the model building processes should be based on a custom model.
- Some of the elements introduced in the assignment are new, but proper steps have been taken to ensure smooth learning. You must learn from the base code provided and implement the same for your problem statement.
- The model training may take time to train as you will be working with large epochs. It is advised to use GPU runtime in Google Colab.
 

**Project Pipeline**
- **Data Reading/Data Understanding** → Defining the path for train and test images 
- **Dataset Creation** → Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- **Dataset visualisation** → Create a code to visualize one instance of all the nine classes present in the dataset 
- **Model Building & training :**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training.
  - Train the model for ~20 epochs
  - Write your findings after the model fit. You must check if there is any evidence of model overfit or underfit.
- **Chose an appropriate data augmentation strategy to resolve underfitting/overfitting** 
- **Model Building & training on the augmented data :**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~20 epochs
  - Write your findings after the model fit, see if the earlier issue is resolved or not?
- **Class distribution:** Examine the current class distribution in the training dataset
  - Which class has the least number of samples?
  - Which classes dominate the data in terms of the proportionate number of samples?
- **Handling class imbalances:** Rectify class imbalances present in the training dataset with [Augmentor library](https://augmentor.readthedocs.io/en/master/).
- **Model Building & training on the rectified class imbalance data :**
  - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
  - Choose an appropriate optimiser and loss function for model training
  - Train the model for ~30 epochs
  - Write your findings after the model fit, see if the issues are resolved or not?

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Technologies Used
- Python 3.7.15
- Google Colab
- Tensorflow
- keras
- Matplotlib
- numpy
- pandas

## Conclusions
- The class rebalance helped in reducing overfititng of the data and thus the loss is being reduced. But it reduced the Acurracy very low.
- Initially we tried without the ImageDataGenerator which created data to over fit at high ratio.
- Then we introduced dropout and ImageDataGenerator which reduced the over fit.
- At last we tried Batch Normalization and Augumentation which really helped in carry forward

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- We implemented this project as part of the Machine Learning - Linear Regression Module required for Post Graduate Diploma in Machine Learning and AI - IIIT,Bangalore (April -2022 batch).
- This project was based on [this tutorial](https://learn.upgrad.com/course/2880).


## Contact
Created by [@akashpd] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
