---
layout: blog
topic: Azure
title: AI-900 AI Fundamentals
tags:  datascience azure ai
comments: true
date: 2022-11-02
---

# AI-900: AI Fundamentals

- [AI, ML, DL](#ai-ml-dl)
- [Types of Learning](#types-of-learning)
  - [Supervised Learning](#supervised-learning)
  - [Unsupervised Learning](#unsupervised-learning)
  - [Reinforcement Learning](#reinforcement-learning)
- [Neural Network](#neural-network)
- [GPU vs. CPU](#gpu-vs-cpu)
  - [General Processing Unit](#general-processing-unit)
  - [Central Processing Unit](#central-processing-unit)
- [Computer Vision](#computer-vision)
## AI, ML, DL
![](/assets/2022-10-27-17-29-19.png)

## Types of Learning

### Supervised Learning 
- Labelded data is used for training
- Task-driven - make a prediction
- eg. classification, regresssion

### Unsupervised Learning
- Unlabelled data is used for training
- Data-driven - recognize a pattern
- e.g. clustering, association

### Reinforcement Learning 
- No data; an environment and an ML model that generates data to reach a goal
- Decision-driven
- e.g. Game AI, Robot Navigation

## Neural Network
- Algorithms trying to mimick the brain
- Data is input into a neuron - which represents an algorithm and the output is passed to one of many other connected neurons
- The connection between neurons is weighted and the network is organized in layers - 1 input layer, 1 to many hidden layers, 1 output layer
- A neural network that has 3 or more hidden layers is considered **deep learning**

![](/assets/2022-11-02-22-36-16.png)

## GPU vs. CPU

### General Processing Unit
- Designed to quickly render high-resolution images and videos concurrently
- Have thousands of processor cores
- Optimized for parallel operations on multiple sets of data 

### Central Processing Unit
- Designed to handle a wide range of tasks quickly
- Have on average 4-16 processor cores
- Optimized for serial operations

## Computer Vision
- Use neural networks to gain high-level understanding of digital images or videos
  - Convolutional neutral network (CNN)
  - Recurrent neural network (RNN)