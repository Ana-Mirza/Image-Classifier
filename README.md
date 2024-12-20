# Image Classifier

This repo contains the machine learning homework of image classification using two datasets with several models.
It includes the jupyter notebook with the source code of the implementation and a report of the results obtained in a pdf file.

- data extraction, transformation and attribute extraction
- model training and evaluation
- visualizations of the data sets and model performace

## Data Sets
### 1. Fruits-360

### 2. Fashion-MNIST

#### Project File Structure
```console
$ ls -l
-rw-r--r-- 1 user user  3572476 Dec 20 10:46 ImageClassifier.ipynb
-rw-r--r-- 1 user user     1159 Dec 20 11:33 README.md
drwxr-xr-x 6 user user     4096 Nov 25 23:27 data
drwxr-xr-x 4 user user     4096 Nov 21 14:35 input
-rw-r--r-- 1 user user      744 Nov 21 14:31 mnist_reader.py
```

## Results Summary
This is a summary of the models/ accuracy after being trained with the datasets after applying different extraction methodologies and tuning the hyperparameters.

TODO: insert table

## Conclusions
Based on the analysis perfomed on the data sets and the training of the models using different methods, several conclusions were extracted on the following topics:

1. **40% lower** results obtained with an imbalanced data set
2. **30% better** accuracy with **data normalization** applied before PCA
3. **1%-5%** better results after **Hyperparameter tuning**
4. **Attribute extraction algorithm**  
