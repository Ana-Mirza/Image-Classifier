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
$ tree -L 1
.
├── Image-Classifier-Report.pdf
├── ImageClassifier.ipynb
├── README.md
├── data
├── input
└── mnist_reader.py
```

The data sets should be plased in the "input/" folder as demonstrated below:
```console
$ tree -L 2 input/
input/
├── fashion
│   ├── t10k-images-idx3-ubyte.gz
│   ├── t10k-labels-idx1-ubyte.gz
│   ├── train-images-idx3-ubyte.gz
│   └── train-labels-idx1-ubyte.gz
└── fruits-360
    ├── Test
    └── Training
```

Since the data sets are too big to be loaded into memory, intermediate results are calculated and stored on persistent memory to be later processed and used for training. For this, another folder named "data/" is needed, with the following folders inside:
```console
$ tree -L 1 /data
data/
├── fashion
├── final
└── fruits-360
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
