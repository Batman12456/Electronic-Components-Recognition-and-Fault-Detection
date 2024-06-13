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

