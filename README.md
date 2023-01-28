# Digit-Recognizer-Keras
Digit Recognizer is a Multiclass Classification project involving image recognition. We have to classify handwritten digits as 0 to 9.
## 0. Introduction

Digit Recognizer is a Multiclass Classification project involving image recognition. We have to classify handwritten digits as 0 to 9.



MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.

In this competition, your goal is to correctly identify digits from a dataset of tens of thousands of handwritten images. We’ve curated a set of tutorial-style kernels which cover everything from regression to neural networks. We encourage you to experiment with different algorithms to learn first-hand what works well and how techniques compare.

### Intro to Convolutional Neural Networks

Convolutional neural networks (CNNs) are the current state-of-the-art model
architecture for image classification tasks. CNNs apply a series of filters to
the raw pixel data of an image to extract and learn higher-level features, which
the model can then use for classification. CNNs contains three components:

*   **Convolutional layers**, which apply a specified number of convolution
    filters to the image. For each subregion, the layer performs a set of
    mathematical operations to produce a single value in the output feature map.
    Convolutional layers then typically apply a
    [ReLU activation function](https://en.wikipedia.org/wiki/Rectifier_\(neural_networks\)) to
    the output to introduce nonlinearities into the model.

*   **Pooling layers**, which
    [downsample the image data](https://en.wikipedia.org/wiki/Convolutional_neural_network#Pooling_layer)
    extracted by the convolutional layers to reduce the dimensionality of the
    feature map in order to decrease processing time. A commonly used pooling
    algorithm is max pooling, which extracts subregions of the feature map
    (e.g., 2x2-pixel tiles), keeps their maximum value, and discards all other
    values.

*   **Dense (fully connected) layers**, which perform classification on the
    features extracted by the convolutional layers and downsampled by the
    pooling layers. In a dense layer, every node in the layer is connected to
    every node in the preceding layer.

Typically, a CNN is composed of a stack of convolutional modules that perform
feature extraction. Each module consists of a convolutional layer followed by a
pooling layer. The last convolutional module is followed by one or more dense
layers that perform classification. The final dense layer in a CNN contains a
single node for each target class in the model (all the possible classes the
model may predict), with a
[softmax](https://en.wikipedia.org/wiki/Softmax_function) activation function to
generate a value between 0–1 for each node (the sum of all these softmax values
is equal to 1). We can interpret the softmax values for a given image as
relative measurements of how likely it is that the image falls into each target
class.
