---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 12: Semi-Supervised Learning"
---

In supervised learning, all the training data are labelled, i.e. we have

$$\{(x^r, \hat{y}^r)\}^{R}_{r=1}$$

While in some scenarios, collecting data is easy but collecting *labelled* data is expensive, so we may have some labelled data and many unlabelled data, i.e. we have

$$\{(x^r, \hat{y}^r)\}^{R}_{r=1}, \{ x^u \}^{R+U}_{u=R+1}$$

Further more, **transductive learning** is the case that unlabeled data is the testing data, i.e. trying to be sepcific on the problem / task, and **inductive learning** unlabeled data is not the testing data, i.e. trying to be be general.

## Semi-Supervised Learning for Generative Models

### Steps

Consider a binary classifgication,

**Step 0**

Initialze the model by the labelled data as in supervised learning:

$$\theta = \{  P(C_1), P(C_2), \mu^1, \mu^2, \Sigma \} $$

**Step 1**

Compute the posterior probability of all the unlabeled data $P_{\theta}(C_1 \vert x^u)$ by the calculated $\theta$.

**Step 2**

Update the model $\theta$ by

$$P(C_1) = \frac{N_1 + \sum_{x^u} P(C_1 \vert x^u)}{N_{tot}}$$

$$\mu^1 = \frac{1}{N_1} \sum_{x^r \in C_1} x^r + \frac{1}{ \sum_{x^u}P(C_1 \vert x^u) } \sum_{x^u}P(C_1 \vert x^u) \dots$$

and then repeat from step 1 until $\theta$ converges. $N_{tot}$ is the total number of examples, $N_1$ is the number of examples belonging to $C1$.

### Explanation

We are finding the maximum likelihood with labelled data and unlabelled data

$$ lnL(\theta) = \sum_{x^r} ln P_{\theta}(x^r, \hat{y}^r) + \sum_{x^u} lnP_{\theta}(x^u) $$

while it's non-convex, so we perform a **EM algorithm** to solve it iteratively, where

$$ P_{\theta}(x^u) = P_{\theta}(x^u \vert C_1)P(C_1) + P_{\theta}(x^u \vert C_2)P(C_2) $$

here the labels we make on the originally unlabelled data are **soft labels**, i.e. an example belong to the classes by probability.


## Low Density Seperation Assumption

非黑即白。"It's either black or white."

We assume that at the boundary of classes, the density of examples are relatively low.

### Self-Training

self-training is useless on regression!!
NN self-training must use hard label!!


### Entropy-Based Regularization

### Semi-Supervised SVM

![semi-supervised SVM](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_12/semi-SVM.png)

## Smoothness Assumption

### Cluster and Label

### Graph-Based Approach

## Better Representation

去蕪存菁，化繁為簡。

Find the latent factors behind the observation, where the latent factors (usually simpler) are better representations.
