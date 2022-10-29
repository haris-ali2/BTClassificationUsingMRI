# Brain Tumor Classification Using MRI

This Repo contains the classification model built on MR images for the classification of brain tumor.

## Data


1. The data contains 4 classes:
    - No Tumor
    - Pituitary
    - Glioma
    - Meningioma
2. The datset can be found [here](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri?select=Training).
3. The `no_tumor` class contains half the examples than the other 3 classes. To mitigate this problem, the data from [Br35H](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection?select=no) is used to increase the examples in the `no_tumor` class and its size is made equal to the other 3 classes.  

## Model


- The architecture used for the classification of is Pre-trained [EfficientNet-B0](https://arxiv.org/abs/1905.11946).
- Optimizer: `Adam`
- Loss: `Categorical CrossEntropy`

## Results

The model is evaluated on 394 test images, unseen by the trained model before. 
1. Version 1: 
    - The training and validation accuracy came out to be `~95%`.
    - The test accuracy proved to be `~71%` yet.
    - The worst learned class being `no_tumor`, probably because of class imbalance in the training data where `no_tumor` is almost half the amount of other classes in the original data.
2. Version 2
    - Added gaussian Noise in training data.
    - The training and validation accuracy came out to be `~97%`.
    - The test accuracy proved to be `~76%`.


