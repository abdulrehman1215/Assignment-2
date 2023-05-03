# Assignment-2

Expression Classification, Valence & Arousal Estimation Using pre-trained models and Transfer Learning
# Abstract:
	
  AFFECT is a psychological term used to describe the outward expression of emotion and feelings. Face and facial expressions are undoubtedly one of the most important nonverbal channels used by the human being to convey internal emotion. This report presents image classification and params regression for a state-of-the-art dataset i.e. AffectNet. EfficientNetB3 and VGG16 with ImageNet weights have been used. The report aims to compare both baselines and demonstrate their experimental results.
Keywords: Classification, Regression, VGG16, EfficientNetB3, pre-trained model, transfer learning
# Introduction:
	
  AFFECT is a psychological term used to describe the outward expression of emotion and feelings. Affective computing seeks to develop systems and devices that can recognize, interpret, and simulate human affects through various channels such as face, voice, and biological signals. Face and facial expressions are undoubtedly one of the most important nonverbal channels used by the human being to convey internal emotion.
	Dimensional model of affect is related with Quantification of affect into continuous values of valence and arousal. Valence refers to how positive or negative an event is, and arousal reflects whether an event is exciting/agitating or calm/soothing” 

  Valence: Whether expression is positive or negative 
  Arousal: Whether event is exciting/agitating or calm/soothing
 
In this report, I will share the approach of emotion recognition using pre-trained models such as VGG16 and EfficientNetB3. Transfer Learning was used to get these pre-trained CNN architectures and then train custom Fully Connected layers on top of that CNN architecture to match our requirements.

# Optimal Architecture:
	
  Here are the favorable architectures for solving the problem at hand:
# VGG16 Baseline:
 
  VGG16 is a state-of-the-art CNN architecture used for image classification. It is trained on an imagenet dataset. It is a small model and provides a great starting point for deep-learning projects which use transfer learning. In this project, I have started with the VGG16 baseline as the first baseline.

# EfficientNetB3 Baselines
	
  As AffectNet is a great and well-known dataset in the field of emotion detection, many papers have used this dataset and implemented different pre-trained models. EfficientNet trained on the ImageNet dataset gives the highest accuracy for classification. The classification accuracy was reported to be around 63%. This motivated me to use EfficientNet trained on the ImageNet dataset to be my second baseline for my project.

 
# Data Loading & Data Handling:
  
  As this dataset was a big dataset, so data handling and loading the data is a main objective of this project. Following are the steps used for data handling and loading the data in this project:
Split data into directories:
	First of all, I have split the data into 8 different directories to ensure that it can be loaded properly using keras’ “keras.utils.image_dataset_from_directory” loader.
 
# Split into batches:
	
  There were around 287k images in the train set, to handle such an amount of data, I split the data into equal-sized batches having 200 images each.

# Normalization:
	
  The images were not noramalized, so I manually normalized the images to improve the efficiency of the neural network architecture.
 
# Transfer Learning:
	
  I have picked pretrained models of VGG16 and EfficientNetB3 with weights of ImageNet.
 
# Custom Model training:
	
  I was not satisfied by the performance of pre-trained models as they were mostly trained on the ImageNet dataset, so I trained my own custom CNN model:
 
# Results:
## VGG16 Results:
	
  Training Accuracy: 72.6%
	
  Validation Accuracy = Test Accuracy = 39.2%

# EfficientNet Results:
  I was only able to run 1 epoch of efficientNet and then my google colab ran out of GPU session limit. Here’s the results that I got: 
	Training Accuracy: 41%
	Validation Accuracy = Test Accuracy = 17%
# Custom Model Result:
	
  Training Accuracy: 77.8%
	Validation Accuracy = Test Accuracy = 43.7%
