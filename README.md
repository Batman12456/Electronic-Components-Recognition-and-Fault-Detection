This repo contains the files and folders necessary for Electronic components recognition and Fault Detection.

# Python
Python codes contain two parts:
- Codes related to create and train the image classification Tensorflow model based on MobileNet.
- Codes related to crawl [Digi-Key], the world's largest seller of electronic components, to create the image datasets

The model which is used for image classification is MobileNet version 2. The model has 154 layers, and in the beginning, the model is not trained and only the last layer of the model among the classification layer are trained with 10 epochs. Then, for fine tuning the model, the last 54 layers of the model is also trained with another 10 epochs.
## Evaluation
For evaluation, the dataset is divided into train set (70%) and validation set (30%). The following table is the results after training the model.
| Metric |Train Set | Validation Set |
|--------|--------- | ---------------|
|  Loss  | 0.5579   |  0.6060        |
|Accuracy| 81.49%   |  78.58%        |

The loss used for evaluation is Cross-entropy. 

# Dataset
The dataset contains 4038 photos of electronic components in 6 different categories: Capacitor, Diode, Resistor, Transformer, Inductor, and IC.
Two resources were used to create the dataset. The [Digi-Key] website, which is the biggest seller of electronic components in the world, was crawled in order to extract photos of the mentioned categories. Also, a public dataset of electronic components hosted in [Kaggle] was used.

# Dataset for PCB

https://public.roboflow.ai/object-detection/undefined

Provided by undefined
License: Public Domain

undefined


pcb components - v2 
==============================

This dataset was exported via roboflow.ai.

It includes 1416 images.
Electronics-componets are annotated in YOLO v5 PyTorch format.

The following pre-processing was applied to each image:
* Auto-orientation of pixel data (with EXIF-orientation stripping)
* Resize to 416x416 (Stretch)

No image augmentation techniques were applied.

# yolov8 fault detection 
https://universe.roboflow.com/annotation-2dedh/yolov8-fault-detection

Provided by a Roboflow user
License: CC BY 4.0

yolov8 fault detection - v1 
==============================

This dataset was exported via roboflow.com.

Roboflow is an end-to-end computer vision platform that helps you
* collaborate with your team on computer vision projects
* collect & organize images
* understand and search unstructured image data
* annotate, and create datasets
* export, train, and deploy computer vision models
* use active learning to improve your dataset over time

For state of the art Computer Vision training notebooks you can use with this dataset,
visit https://github.com/roboflow/notebooks

To find over 100k other datasets and pre-trained models, visit https://universe.roboflow.com

The dataset includes 435 images.
Fault-detected-no-fault-detected are annotated in YOLO v5 PyTorch format.

The following pre-processing was applied to each image:
* Auto-orientation of pixel data (with EXIF-orientation stripping)
* Resize to 640x640 (Stretch)

The following augmentation was applied to create 3 versions of each source image:
* 50% probability of horizontal flip
* Equal probability of one of the following 90-degree rotations: none, clockwise, counter-clockwise, upside-down
* Randomly crop between 0 and 20 percent of the image
* Random rotation of between -15 and +15 degrees
* Random shear of between -10° to +10° horizontally and -10° to +10° vertically
* Random brigthness adjustment of between -15 and +15 percent
* Random exposure adjustment of between -10 and +10 percent



