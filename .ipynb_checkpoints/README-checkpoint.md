# MachineLearningA2
https://www.tensorflow.org/guide/data


# Introduction

## Research Question

Given the two datasets, this investigation sets out with two ultimate aims.
1. To build a model which, given an image of a cell, can predict whether or not the cell is cancerous or not (M1).
2. To build a model which, given an image of a cell, can predict the class of cell type (M2).

The similarities and differences of the two tasks must be aknowledged.

The components of a machine learning problem will be addressed as follows:

### Experience

The algorithm will be taking the images provided in the dataset as experience for the relevant problems. A main dataset has been provided, whose associated data/output set can be used to build both models. A second extra dataset has been provided, which will further improve model M1.

Regarding data cleansing, the outcome was fortunate. After initial analysis of the data, no whitespaces, impossible values, null values, or spelling errors were found. 

### Performance evaluation

The performance of model M1 will be evaluated through a confusion matrix of its ultimate predictions, resulting in Recall, Precision, and F1 scores. A sample of images from the testing dataset and their relevant predictions will be displayed as a demonstration. The test image names and their predictions will then be saved as a csv file.

Analysing the results of Sirinukunwattana et al., They arrived at a maximum precision of 0.783, recall of 0.827, and F1 of 0.802, albeit the results arose from different model tunings. For our Baseline model, we can hope for over 0.5 in these evaluations, based 


https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7399414&tag=1


https://datascience.stackexchange.com/questions/45165/how-to-get-accuracy-f1-precision-and-recall-for-a-keras-model

### Model selection

A short analysis of the aims of both M1 and M2 reveals that it is a supervised learning problem (given labelled datasets to train the algorithm). It is also clear both both models are trying to classify inputs in to their respective discrete categories, rather than predict some continuous value of 'cancerous' or 'cell type'. Therefore, the investigation will focus on classification ML paradigms.

As mentioned earlier, the only data provided as input is the raw image pixel data. One approach might be to try and derive features related to cancer detection manually (textures, edges, shapes, etc), and build a model based on these features. To do so, however, would be a long and arduous process. A much simpler model for our purposes will be a neural network. Using such a model would provide benefits that address the mentioned problems. The network will be able to detect and learn which features of an image are most important naturally, but will also be able to extract this information from the raw pixel data.

Our baseline model will be a simple shallow sequential neural network. The images themselves will be taken as input datas, with one hidden layer for flattening the pixels, and seperating RGB colour channels. The network will then output the probability of the image being cancerous. This baseline will establish the validity of a NN model, which can then be tuned by either changing the number of layers/parameters, or experimenting with different metrics/losses/optimizers.

https://www.educba.com/classification-of-neural-network/


|
|
|
V

CNN keras
> https://www.ibm.com/topics/supervised-learning#:~:text=the%20next%20step-,What%20is%20supervised%20learning%3F,data%20or%20predict%20outcomes%20accurately.
> https://datascience.stackexchange.com/questions/73093/what-does-from-logits-true-do-in-sparsecategoricalcrossentropy-loss-function

> https://developers.google.com/machine-learning/practica/image-classification#:~:text=Image%20classification%20is%20a%20supervised,the%20input%20to%20the%20model.

### Loss function

Referencing the works of Sirinukunwattana et al., Cross entropy is used as an appropriate loss function for cancer detection and classification. M1 therefore will evaluate loss as the binary crossentropy loss.

|
|
|
|
V

After testing the baseline model, we arrive at 