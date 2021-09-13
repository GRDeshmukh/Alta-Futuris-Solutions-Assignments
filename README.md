## CNN on SVHN (Street View House Number) dataset

**Please check above svhn_model.ipynb and data_preprocess.ipynb files for building Convolutional Neural Network and data preprocessing.**

The dataset link is given below.

**Google Street View House Number(SVHN) Dataset**        **[Link](http://ufldl.stanford.edu/housenumbers/)**

 SVHN contains much more labeled data (over **600,000 images**) with real world problems of recognizing digits and numbers in **natural scene images.**


## Overview for SVHN dataset:

This is the overview in terms of classes, digits for training and testing as well as data formats
1. Total 10 Classes, 1 for each digits  *i.e Label '9' for digit 9 and '10' for digit 0.*
2. For training 73257 digits, For testing 26,032 digits
3. It is available in two different formats
   - Original images with bounding box available for each character (may contain multiple characters in same images).
   - **MNIST** like 32x32 cropped images having single character in each image.
 



Dataset is obtained from house numbers in Google Street View images. 


Here we are classifying 32 x 32 cropped images given in format 2 

Using CNN architecture.

[Train_32x32](http://ufldl.stanford.edu/housenumbers/train_32x32.mat)                     
[Test_32x32](http://ufldl.stanford.edu/housenumbers/test_32x32.mat)

### Model building and data preprocessing scripts 

   - **`data_preprocess.ipynb`**: preprocess the data
   
   - **`svhn_model.ipynb`**: run the model and report results
    
### New Addition
 ```
- Confusion metric 
- Visualization of misclassified and classfied images
```
    
**Findings:**
```
From logs we can make out that dropout rate should be higher to learn
good features as images have lots of others digits image pixels also in it.

So it gets confused more often
```

**Note:** 
```
I have performed above experiment under 4GB RAM and 1GB GPU Memory.
So it was difficult to train it for more steps, and adding more layers in architecture
```
