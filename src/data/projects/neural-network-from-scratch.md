---
title: Neural network from scratch
description: A zero-library neural network that I made as a bet
tags:
  - Machine learning
  - Image Recognition
  - Python
featured: true
repo: https://github.com/Deneb999/neural-network-from-scratch
image: /mnist.webp
---

During my first year of college, I was working on a minesweeper speedrunner. The program would play minesweeper in
an optimal way, in order to solve it as fast as possible. To that purpose, I recognized that I would need to make or
obtain some kind of tool that would recognize the numbers on the screen. I was talking to a friend about my intention
to write a neural network to recognize these numbers, when he told me that it was something way too hard to implement.
This then derived into a friendly discussion about implementation of machine learning models, and this into a
**bet** made to me: that I couldn't write a model to recognize numbers from scratch.

I was given a week to complete this project, but I set out to do it in a weekend instead. I reasearched neural network
models and soaked in all the information possible about backpropagation and activation functions. I made some experiments
and decided on creating a [784,512,10] neural network to learn the numbers from 1 to 10, as a compromise between
performance and training speed (I was running the training on my laptop).

The implementation wasn't as hard as one would have thought, once I understood the materials. I wrote a class
Neural_network (yes, I was young and didn't know better than to snake-case a Python class) with an activation
function, error metric, training, forward propagation and stochastic gradient descent. I didn't know anything about 
adaptative learning rates, optimization in Python or even **matrix multiplication**. In fact, there are way too many
nested for loops in my code. As I said, I was young and in my first year of university.

For the training, I downloaded the mnist dataset and split it between training and testing. After two days of the 
computer running my very poorly optimized code, I managed to achieve an accuracy of 90%, winning the bet.