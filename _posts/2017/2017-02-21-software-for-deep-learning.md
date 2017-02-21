---
layout: post
title: Software for deep learning
date: '2017-02-21 12:40'
---

The [Montreal Institute for Learning Algorithms (MILA)](https://mila.umontreal.ca/) maintains a long [list of deep learning software](http://deeplearning.net/software_links/). I've only ever used Theano and Pylearn2 and need to familiarize myself with the current state of deep learning tools as I re-boot an existing project. This post is my attempt to organize basic information about a limited set of tools to help me decide exactly what to use for my current project.

## Computation Engines (Back ends)
Name | Language | Description
--|---|--
[Theano](http://deeplearning.net/software/theano) | Python | Define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently to run on CPU or GPU
[Tensor Flow](https://www.tensorflow.org/) | Python | Numerical computation using data flow graphs, similar to Theano
[Torch](http://torch.ch/) | Lua | Scientific computing framework, Tensor computation with strong GPU acceleration
[Caffe](http://caffe.berkeleyvision.org/) | Python | Machine vision library that ported Matlab fast CNNs to C and C++, not intended for other data types
[ND4J](http://nd4j.org/) | Java | Scientific computing libraries for the JVM



## Interface Libraries
Name | Language  |  Description | Back ends  
--|---|--
[Pylearn2](https://github.com/lisa-lab/pylearn2) | Python | Provides reusable common components, no longer actively developped | Theano
[GroundHog](https://github.com/lisa-groundhog/GroundHog)  | Python  | Complex recurrent neural network models, development discontinued, moved to Blocks   |   Theano
[Lasagne](http://lasagne.readthedocs.io/en/latest/index.html)  | Python  | Lightweight library to build and train neural networks in Theano. | Theano
[Keras](https://keras.io/)  | Python  | High-level library for fast experimentation | Theano, TensorFlow
[Blocks](http://blocks.readthedocs.io/en/latest/)  | Python | Quick prototyping of complex neural network models, annotates the Theano computational graph instead of adding abstractions, consists of Bricks (reusable common components), large graph management, training algorithms and training abilities.  | Theano
[Fuel](https://github.com/mila-udem/fuel) | Python |  Download/iterate/preprocess datasets to pipe into Blocks  | Theano
[PyTorch](http://pytorch.org/)  | Python  | Not a Python binding into a C++ framework, can use it naturally like you would use numpy / scipy / scikit-learn | Torch
[Deeplearning4j](http://deeplearning4j.org) | Java | Distributed deep-learning in Java and Scala | ND4J

## References
* http://deeplearning.net/software_links/
* https://deeplearning4j.org/compare-dl4j-torch7-pylearn
