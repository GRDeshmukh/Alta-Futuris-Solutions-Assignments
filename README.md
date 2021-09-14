## ```CNN on SVHN (Street View House Number) dataset```

**Please check above svhn_model.ipynb and data_preprocess.ipynb files for building Convolutional Neural Network and data preprocessing.**

The **Street View House Number (SVHN)** is a digit classification benchmark dataset that contains 600000 32×32 RGB images of printed digits (from 0 to 9) cropped from pictures of house number plates. The cropped images are centered in the digit of interest, but nearby digits and other distractors are kept in the image. 

The dataset link is given below.

**```Street View House Number(SVHN) Dataset```**        **[Link](http://ufldl.stanford.edu/housenumbers/)**

 dataset can be seen as similar in flavor to MNIST (e.g., the images are of small cropped digits), but incorporates an order of magnitude more labeled data (over 600,000 digit images) and comes from a significantly real world problem (recognizing digits and numbers in natural scene images)


## ``Standard overview for SVHN dataset``:

The images lack any contrast normalisation, contain overlapping digits and distracting features which makes it to differ from MNIST.

![download (1)](https://user-images.githubusercontent.com/55298667/133098164-33388ca4-8f8a-4a40-a8c0-04f0bfe1316e.jpg)

It also comes with an additional 531,131 somewhat less difficult samples that can be used as extra training data.

This is the overview in terms of classes, digits for training and testing as well as data formats
1. Total 10 Classes, 1 for each digits  *i.e Label '9' for digit 9 and '10' for digit 0.*
2. For training 73257 digits, For testing 26,032 digits
3. It is important to note that the data are divided into two format. We are going to use Format 2:
   
   **Format 1**: The original, variable-resolution colored house-number images with character level bounding boxes.
   
   **Format 2**: The cropped digits (32x32 pixels) which follow the philosophy of the MNIST dataset more closely, but also contain some distracting digits to the sides of the   digit    of interest.
 



Dataset is obtained from house numbers in Google Street View images. 


Here we are classifying 32 x 32 cropped images given in format 2 

Using CNN architecture.

[Train_32x32](http://ufldl.stanford.edu/housenumbers/train_32x32.mat)                     
[Test_32x32](http://ufldl.stanford.edu/housenumbers/test_32x32.mat)

### Model building and data preprocessing scripts

  Preprocess the data:  **data_preprocess.ipynb**
   
  Run the model and report results: **svhn_model.ipynb**
    
### New scaled addition
Following is the new addition 
- Visualization of misclassified and classfied images
    
**Dropout rate finding from logs:**

Dropout rate should be higher to learn good features 
as images have lots of others digits image pixels in it.

That makes it confuse more often.


**Consideration and Note:** 

Above experiment has been performed under 4GB RAM and 1GB GPU Memory.
Due to these specifications, it was difficult to train it for more steps and add more layers in architecture.

