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

### Training Model

![alt text](https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/model_CNN.png)

### Results

**Test Accuracy : 99.39%**
 
![alt text](https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/training_accuracy.png)

![alt text](https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/validation_accuracy.png)

![alt text](https://raw.githubusercontent.com/shreyagu/Handwritten-digit-recognition-MNIST/master/results/epoch_loss.png)


