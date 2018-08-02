# Handwritten Digit Recognition on MNIST dataset

## Getting Started 
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites

[sklearn](http://scikit-learn.org/stable/documentation.html)
[keras](https://keras.io/)
[matplotlib](https://matplotlib.org/contents.html)

## Dataset
Publicly available [MNIST dataset](http://yann.lecun.com/exdb/mnist/) can be found [here](http://yann.lecun.com/exdb/mnist/).

## Conclusion

The five parameters which have been varied to plot the performance curves:
    1. EPOCHS: can be increased to increase accuracy, smoother training and testing convergence but increases computation time. 
    2. ACTIVATION FUNCTION: It plays an important role in deciding the rate of convergence, as observed, RELU converges faster than the sigmoid activation. Performance wise also RELU performs better than SIGMOID in terms of step speed and accuracy. Nowadays we should use ReLU which should only be applied to the hidden layers. And if your model suffers from dead neurons during training we should use leaky ReLu or Maxout function. 
    3. DROPOUT RATE: increasing dropout rate increases accuracy.  Accuracy is also improved if the dropout rate is added between the CONV layers and FC layers. This happens because of dimensionality reduction due to dropout and only important points are retained. This helps in prevention of over-fitting and results in better testing accuracy.
    4. BATCH SIZE: decreasing the batch size results in drastically increasing of computation time. This is explained by the fact that the training data is divided into smaller batch sizes and needs more batches to be processed hence increasing computation time . Batch size must be kept optimal, not too small and not too large, for best results. 

Many experiments were performed with the above parameters to obtain the best training model mentioned below.
    5. TRAINING MODEL :

Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 26, 26, 64)        640       
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 13, 13, 64)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 11, 11, 128)       73856     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 5, 5, 128)         0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 3, 3, 128)         147584    
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 1, 1, 64)          73792     
_________________________________________________________________
dropout_1 (Dropout)          (None, 1, 1, 64)          0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 64)                0         
_________________________________________________________________
dense_1 (Dense)              (None, 128)               8320      
_________________________________________________________________
dropout_2 (Dropout)          (None, 128)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 84)                10836     
_________________________________________________________________
dropout_3 (Dropout)          (None, 84)                0         
_________________________________________________________________
dense_3 (Dense)              (None, 10)                850       
=================================================================
Total params: 315,878
Trainable params: 315,878
Non-trainable params: 0
_________________________________________________________________


### Results

**Test Accuracy : 99.39%**
 
 ![alt text]((https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/training_accuracy.png)

 ![alt text]((https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/validation_accuracy.png)

 ![alt text]((https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/epoch_loss.png)


