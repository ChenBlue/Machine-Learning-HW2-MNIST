# Machine-Learning-HW2-MNIST
This is the homework from CS5651 Machine Learning in National Tsing Hua University.

## Introduction
MNIST is a simple computer vision dataset. It consists of images of handwritten digits like these:
![handwriting](https://github.com/ChenBlue/Machine-Learning-HW2-MNIST/blob/master/handwriting.JPG) </br>
All datas includes label on it. For example, the label of above image are 5,0,4,1. Each image is 28 pixels by 28 pixels. Moreover, The MNIST data is split into three parts: 55,000 data points of training data (mnist.train), 10,000 points of test data (mnist.test), and 5,000 points of validation data (mnist.validation). </br>
In this homework, we trained the data only on digits 0~4 and derive accuracy rate & precision rate & recall rate.

## Neural Network Structure
- Five hidden layers with 128 neurons each
- Softmax output layer with 5 neurons
- **He initialization**: tf.contrib.layers.variance_scaling_initializer()
- **ELU activation function**: tf.nn.elu
- **Adam Optimizer**: tf.train.AdamOptimizer()
- **Cross Entropy**:tf.nn.sparse_softmax_cross_entropy_with_logits
- Mini-batch size: 256
- Dropout rate: 0.1 (Optional, because it doesn't help)
