# Mask-Detection

### Introduction
This is an image classification model that classifies different ways of people wearing masks. The data is retrieved from kaggle, created by [KUCEV ROMAN](https://www.kaggle.com/tapakah68/medical-masks-part1). The dataset used has 40000 images with each 10000 images for each labels. 

The labels are: 
* TYPE 1 - There is no mask on the face.
* TYPE 2 - The mask is on, but does not cover the nose or mouth.
* TYPE 3 - The mask covers the mouth, but does not cover the nose.
* TYPE 4 - The mask is worn correctly, covers the nose and mouth. 

### Model Architecture
This is a ViT based model which is pretrained on Imagenet dataset, with a specification of image size 224 and 16 patches. The model is transfer learn to match the dataset given by [KUCEV ROMAN](https://www.kaggle.com/tapakah68/medical-masks-part1). The overall test accuracy is 92.8%. Due to the massive amount of data with limited resources, the model was trained for only one epoch, however, one epoch has been proven to be sufficient enough for the model to distinguish different labels.

### Key things to note when using the dataset
After preprocessing the dataset, I realise the files listed below are corrupted for some reason and was not able to be read by [pillow](https://pillow.readthedocs.io/en/stable/installation.html). I decided to remove the files that can't be read manually after testing the files one by one.

These are the corrupted images that I found.//
![Capture](https://user-images.githubusercontent.com/67994195/133401930-85874880-1fdf-4b3f-b288-707a39ad5c1f.PNG)
