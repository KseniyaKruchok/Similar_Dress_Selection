# Similar_Dress_Selection

## Overview

This project intends to develop a tool to select **similar looking dresses**. 
There are two approaches coded in this project:

1. build and train **custom CNN** (convolutional neural network) model for feature extraction. 
2. use pre-trained computer vision model (I used **Inception V3** trained on ImageNet dataset) for feature extractions

In either case extracted features are used as input in **unsupervised k Neareast Neighbors** model to identify similar looking items.

I am working with [Deep Fashion](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion.html) dataset to train custom convolutional neural network model and use its output in unsupervised Nearest Neighbor model. I am also using two other unlabeled dataset for testing. The image data is too heavy to be upladed here. It can be either found at above link or I can provide it upon request. Please feel free to reach me at Kseniya.Kruchok@gmail.com

## Repository Structure

The contect is conveniently divided into following folders:

***Data*** contains dataframes for train, test and validation sets related to items marked as dress in Deep Fashion dataset. This folder also has saved CNN model trained on low res images (the one trained on high res images is too heavy for github, but is available upon request)

***Data preprocessing*** consists of below three notebooks addressing data selection for training custom CNN model as well as exploration of image sizing and reshaping images from all datasets into sizes appropriate for modeling:

 - *Data_selection*: data exploration and wrangling to select dress samples from Deep Fashion dataset and select appropriate attributes
 - *Image_sizing*: exploration and analysis of image sizes for low and high resolution images
 - *Data_split_and_preprocessing*: cropping and resizing images to the same ratio, splitting data into train, validation and test sets
 
***Feature extraction*** has code for building and training CNN models as well as feture extraction from them and from Inception V3. It contains below notebooks

 - *CNN_architecture_exploration_on_low_res_images.ipynb*: exploration and training different CNN models (experimenting with number of layers, kernel size, number of neurons, activation functions, etc.) using low resolution images, calculating predictions using the optimal one for test sets
 - *CNN_trained_on_high_res_images*: building and training CNN (same as final structure of CNN trained on low res images) on high resolution images, calculating predictions for test sets
 - *Inception_V3_for_feature_extraction*: feature extraction using pre-trained computer vision model
 
 ***ML Unsupervised kNN*** contains code on building and exploring model to select similar looking items
 
 - *Unsupervised_kNN*: building and evaluating unsupervised kNN for similar dress selection using predictions from CNN and extracted features as input.


***Reports*** contains project proposal, final report and presentation slides
