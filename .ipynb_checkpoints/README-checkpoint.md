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

The performance of model M1 will be evaluated through a confusion matrix of its ultimate predictions, resulting in Recall, '____', and F1 scores. A sample of images from the testing dataset and their relevant predictions will be displayed as a demonstration. The test image names and their predictions will then be saved as a csv file.

### Model selection

A short analysis of the aims of both M1 and M2 reveals that it is a supervised learning problem (given labelled datasets to train the algorithm). It is also clear both both models are trying to classify inputs in to their respective discrete categories, rather than predict some continuous value of 'cancerous' or 'cell type'. Therefore, the investigation will focus on classification ML paradigms.
|
|
|
V

Binary classification

|
|
|
V

CNN keras
> https://www.ibm.com/topics/supervised-learning#:~:text=the%20next%20step-,What%20is%20supervised%20learning%3F,data%20or%20predict%20outcomes%20accurately.
> https://datascience.stackexchange.com/questions/73093/what-does-from-logits-true-do-in-sparsecategoricalcrossentropy-loss-function
### Loss function

