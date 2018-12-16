---
title: NeuralNetworksPart1
name: Step By Step Guide To Run Your Trained Neural Network Model On Android (Part I) 
---
![Neural Network](img/neural_cover.png)
> In this post I am trying to explain how to run a trained neural network model on android. For this guide I’m going to use Keras deep learning library to implement the neural network. The proof of concept code is available on my GitHub repository. I’ve wrote this post in two parts. Part I will provide all the background information of deep learning libraries that will be useful to understand this guide. In part II , I will guide you through the real coding stuff.

## Why you should read this Article ?
Training the model in Android phone itself might not be a good idea. Training phase requires lot of resources and may take several hours depending on the training data set you have. One option is that you could train the model on a server or in your laptop and import it to your android project. If the model is evolving then you can retrain it and just update the app with new model.

This might be a really useful article if you are an android app developer. There is a plethora of articles written on this subject which I have listed in references which are little bit complicated to begin with. After reading this post I encourage you to read those articles as well. So Let’s get started.
## Prerequisites
This post doesn’t intend to give you a deep explanation about internals of neural networks. So you must at least have some idea about machine learning , what neural networks are and how they work. you should also have some knowledge about python basics. If so you are good to go.

## What you’ll learn from this guide….

1. _Introduction to TensorFlow and Keras deep learning libraries._

2. _Creating a Neural Network using Keras Deep learning library._

3. _How to save your trained Model as protobuf(.pb) file._

4. _Importing trained model to your android project and make predictions._

## 1.Introduction to TensorFlow and Keras deep learning libraries

> What is TensorFlow?

The main reason why I have include TensorFlow in this guide is because you need to have a little understanding about what a node is. It will help you to understand the code of converting your Keras model to protobuf file. If you are confused right now, don’t be, It will all make sense while you go through the post. ;)

Ok back to TensorFlow. Its an open source library developed by google engineers for machine learning tasks. The important fact about TensorFlow is that it provides multiple API’s. Unlike very high level libraries like Skit-learn, TensorFlow allows fine control over the models.

A **tensor** is nothing but a set of primitive values shaped into an array of any number of dimensions. tensor’s **rank** is its number of dimensions.

![tensor rank example](img/tensor_rank.png)

**Node** takes zero or more tensors as inputs and produces a tensor as an output. For example you can have store constant values in two nodes and get the addition of the values of these two nodes to another node. These nodes have unique names. If you want more details there’s a nice tutorial [here](https://www.tensorflow.org/tutorials/).