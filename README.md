## Overview
Using the dataset ["A dataset of skin lesion images collected in Argentina for the evaluation of AI tools in this population"](https://pubmed.ncbi.nlm.nih.gov/37853053/), I'm making several versions of the same or similar CNN models with the primary difference being the handling of the missing data within the dataset. While this dataset says it's for evaluation, it will be used for training as well in this project. However, this isn't meant to try and obtain a perfect classification model, but rather just evaluate the different methods of handling missingness.

## Dataset Information
This dataset contains 623 patients, with a total of 1,616 skin lesion images associated with those patients. The entirety of the dataset was collected from an Argentinian population, making it unique and important for evaluation.
- That uniqueness was part of what motivated me to chose this dataset over others.

## Information of Chosen Model
I've decided to use VGG-19 as a pretrained base, which has been good for classifications of other types of models. Even though VGG-16 and VGG-19 are similar, with VGG-19 requiring more computing power, this shouldn't be a problem since my dataset isn't very large.


## Chosen Methods of Data Handling
After preprocessing of the data in a general manner, the specific methods for handling the missing data will be applied:
1. CCA
	- This is just as a baseline to get me started and see what would happen. In reality, CCA is impractical for this dataset.
2. Single Imputation
	- With the use of KNN, we'll fill in each blank spot with what is most likely to be there based on it's neighbors with similar datapoints.
3. Multiple Imputation
4. Inverse Probability Weighing
