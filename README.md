# Similar_Dress_Selection

This project intends to develop a tool to select similar looking dresses. I am working with [Deep Fashion](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion.html) dataset to train custom convolutional neural network model and use its output in unsupervised Nearest Neighbor model. I am also using two other unlabeled dataset for testing. The image data is too heavy to be upladed here. It can be either found at above link or I can provide it upon request. Please feel free to reach me at Kseniya.Kruchok@gmail.com

STRUCTURE:

DATA: contains dataframes for train, test and validation sets related to items marked as dress in Deep Fashion dataset. This folder also has saved CNN model trained on low res images (the one trained on high res images is too heavy for github, but is available upon request)

REPORTS: contains project proposal milestone and final report

NOTEBOOKS:
 - Data_selection: data exploration and wrangling to select dress samples from Deep Fashion dataset and select appropriate attributes
 - Image_sizing: exploration and analysis of image sizes for low and high resolution images
 - Data_split_and_preprocessing: cropping and resizing images to the same ratio, splitting data into train, validation and test sets
 - CNN_trained_on_low_res_images: exploration and training different CNN models using low resolution images, calculating predictions for test sets
 - CNN_trained_on_high_res_images: building and training CNN (same as final structure of CNN trained on low res images) on high resolution images, calculating predictions for test sets
 - Inception_V3_for_feature_extraction: feature extraction using pre-trained computer vision model
 - Unsupervised_kNN: building and evaluating unsupervised kNN for similar dress selection using predictions from CNN and extracted features as input.
