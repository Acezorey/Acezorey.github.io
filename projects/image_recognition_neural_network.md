---
layout: project
type: project
image: img/deeplearning.jpg
title: "Image Recognition Neural Network"
date: 2025-01
published: true
labels:
  - Artificial Intelligence
  - Python
  - NumPy
  - Educational
  - Jupyter Notebook
summary: "Neural network developed and trained to recognize 2D images"
---

<img width="100%" src="../img/dataset-cover.png">

## Overview
This program is a deep learning neural network developed entirely without using any machine learning libraries, such as PyTorch or Tensorflow, using only pure Python and NumPy. Designed with guidance from the book <a href="https://nnfs.io/">Neural Networks from Scratch</a>, this was made for educational purposes to learn of the mathematics and mechanics behind deep learning models.

## Technical Details
This model was trained on the Fashion MNIST dataset (accessable on <a href="https://www.kaggle.com/datasets/zalando-research/fashionmnist">Kaggle</a>, examples of training data shown on top), a dataset containing tens of thousands of labeled 28x28 pixel images of articles of clothing.

<img width="500px" src="../img/modeltraining.png">

It is also indeed capable of recognizing pieces of clothing from test images, including hand drawn ones.

<img width="500px" src="../img/modelprediction.png">

This model uses 3 layers: an input layer of 128 neurons, a deep layer of 128 neurons, and an output layer of 10 neurons. During the forward pass, each neuron takes in an input value, multiplies said value to a weight, and adds a bias value, creating the resulting output. Note that the "neurons" themselves are not actually "real", as in there is no "neuron" class or object, it is just a way to represent the data being processed. In reality each layer takes in an input matrix, multiplies it to a weight value matrix, and adds a bias matrix. 

This output is then sent through an activation function, in this instance the Reticulated Linear Activation (<a href="https://www.geeksforgeeks.org/relu-activation-function-in-deep-learning/">ReLU</a>) function. The ReLU function essentially multiplies the output by 1 (keeps the output) if the output of the neuron > 0, and equates it to 0 otherwise.

During training, the final output then has its loss and accuracy calculated via <a href="https://www.geeksforgeeks.org/categorical-cross-entropy-in-multi-class-classification/">categorical crossentropy</a>. 

Using the calculated loss, the model then initiates the backward pass, utilizing the Adaptive Moment Estimation (<a href="https://www.geeksforgeeks.org/adam-optimizer/">Adam</a>) Optimizer function to update the various weights and biases used in the neural layers in order to reduce loss and increase accuracy through <a href="https://www.geeksforgeeks.org/gradient-descent-algorithm-and-its-variants/">gradient descent</a>.

This forward pass - backward pass process continues until the entirety of the training data has been processed by the model. The data itself is randomized during training to prevent the model from just memorizing a single kind of data (ex: memorizing what a shoe looks like and nothing else), and is also divided into smaller sets to allow for more efficient training.

This model utilizes a lot of math: most notably linear algebra, calculus, and partial differential equations.

## Links
Github: <a href="https://github.com/Acezorey/neural-network-learning">Link</a>
