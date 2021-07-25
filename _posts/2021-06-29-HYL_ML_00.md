---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 0, Introduction"
---

## Definitions & Relationships of Terminologies
**Artificial intelligence**: The overall goal of the research, i.e. to let machines be as intelligent as human.
**Machine Learning**: An approach to AI, i.e. to let machines learn. For many problems, we can not hand-craft the rules to build a machine, so we collect data for the problem and let the machine learn from the data.

**Deep Learning**: Another approach to AI by ANN of more then 3 layers.

![terms](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_00/terms.png)

My comments: The definitions actually varies by context.

## The 3 Steps of Machine Learning, Simplified
 1. Define a set of functions.
 2. Define goodness of functions.
 3. Pick the best function.

#1 is "choose a ML model", which specifies the set of functions; #2 can be "define a loss function"; #3 is "training".

## Types of Tasks

**Regression**: input -> scalar, e.g. predicting the PM 2.5 value.

**Classification**: input -> Y/N (binary, e.g. spam identification, mail -> is a spam.) or classes (e.g. Go, current board -> the best location of the next step).

**Strutured Learning**: generate outputs with further structured informations, e.g. sentences (which has grammar) or to recognize objects in an image and also frame the location of the object.

![structured](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_00/structured.png)

## Types of Scenarios
In other words, "what kinds of data we can get". Usually we cannot control the scenarios.

**Supervised learning**: All the data are labelled, i.e. every sample of the data is a pair of input & output. Also, like "learn from teacher".

Labeling enough data may be labor-consuming or difficult, sometimes we want to avoid it, so there're also semi-supervised learning, transfer learning, unsupervised learning and reinforcement learning.

**Semi-Supervised Learning**: Some data are labelled & some data are not labelled. There may be only a few labelled data.

**Transfer Learning**: There're some (fewer) labelled data of the task, and there're some labelled or unlabelled data of other unrelated tasks.

**Unsupervised Learning**: The data are al unlabelled, i.e. only inputs or outputs are known.

**Reinforcement Learning**: to train by scores of outputs from inputs; learn from critics.


## Relationships between Scenarios, Tasks & Methods
![learning_map](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_00/learning_map.png)

## Reference
[Youtube Link](https://youtube.com/playlist?list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
