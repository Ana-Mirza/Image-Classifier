# Image Classifier

This repo contains the machine learning homework of image classification using two datasets and several models from python *sklearn* library.
It includes the jupyter notebook with the source code of the implementation and a pdf file report containing:

- data extraction, transformation and attribute extraction
- model training and evaluation
- visualizations of the data sets and model performace

## Data Sets
### 1. Fruits-360
The Fruits-360 dataset was one of the data sets used for analysing different strategies of attribute extraction and hyperparameter tuning on several models.
Since the data set was inbalanced, we were able to observe the effect of class distribution on the model performance.
Visualizations included in the report are limited to the 10 biggest classes in the data set because there are 70 total classes of fruits and vegetables.

**Link:** https://www.kaggle.com/datasets/moltean/fruits

### 2. Fashion-MNIST
The Fashion-MNIST data set is a balanced dataset of 10 classes of clothing items. The link of the data set is included below.

**Link:** https://github.com/zalandoresearch/fashion-mnist

### Project File Structure
Two additional folders named "input/" and "data/" need to be created to run the source code.
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

Since the data sets are too big to be loaded into memory, intermediate results are calculated and stored in the "data/" folder to be later processed and used for training. For this, additional folders are needed.
```console
$ tree -L 1 /data
data/
├── fashion
├── final
└── fruits-360
```

## Results Summary
This is a summary of the models' accuracy after being trained with the datasets, applying different extraction methodologies and tuning the hyperparameters.

| Model | Attribute Selection Algorithm | Fruits-360 | Fashion |
| --- | --- | --- | --- |
| Logistic Regression | HIST | 61.78% | - |
| | PCA (70 PC) | 71.78% | - |
| | HOG - PCA (20 PC) | - | 80.98% |
| SVM | HIST | 70.89% | - |
| | PCA (70 PC) | 92.35% | - |
| | HOG - PCA | - | 87.54% |
| Random Forest | HIST | 59.46% | - |
| | PCA (70 PC) | 87.31% | - |
| | HOG - PCA (20 PC) | - | 85.29% |
| Gradient Boosted Trees | HIST | 59.38% | - |
| | PCA (70 PC) | 81.16% | - |
| | HOG - PCA (20 PC) | - | 85.83% |

## Conclusions
Based on the analysis perfomed on the data sets and the training of the models using different methods, several conclusions were extracted:

1. **40% lower** results obtained with an **imbalanced data set**
2. **30% better** accuracy with **data normalization** applied before PCA
3. **30% better** results with best **attribute extraction algorithm** on best model (SVM - HIST vs PCA for Fruits-360)
4. **1%-5%** better results after **Hyperparameter tuning**
