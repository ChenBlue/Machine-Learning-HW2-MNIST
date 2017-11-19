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
- Dropout rate: 0.1 (Optional, if I let it zero, the model will be better)
- 5 fold cross-validation

## Precision & Recall
- True Negative(TN): case was negative and predicted negative
- True Positive(TP): case was positive and predicted positive
- False Negative(FN): case was positive but predicted negative
- False Positive(FP): case was negative but predicted positive
$$ Precision = \frac{TP}{TP+FP} $$
$$ Recall = \frac{TP}{TP+FN} $$

## Result
For validation dataset, average accuracy rate: 0.952 </br>
For testing dataset, accuracy rate: 0.953 </br>
| label | Precision | Recall |
| ----- |-----------| ------ |
|0 | 0.9407 | 0.9765 |
|1 | 0.9563 | 0.985 |
|2 | 0.9628 | 0.9312 |
|3 | 0.9332 | 0.9703 |
|4 | 0.9687 | 0.9318 |
