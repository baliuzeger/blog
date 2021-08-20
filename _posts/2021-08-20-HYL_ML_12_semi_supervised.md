---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 12: Semi-Supervised Learning"
---

In supervised learning, all the training data are labelled, i.e. we have

$$\{(x^r, \hat{y}^r)\}^{R}_{r=1}$$

While in some scenarios, collecting data is easy but collecting *labelled* data is expensive, so we may have some labelled data and many unlabelled data, i.e. we have

$$\{(x^r, \hat{y}^r)\}^{R}_{r=1}, \{ x^u \}^{R+U}_{u=R+1}$$

Further more, **transductive learning** is the case that unlabeled data is the testing data, i.e. trying to be sepcific on the problem / task, and **inductive learning** unlabeled data is not the testing data, i.e. trying to be be general.

## Semi-Supervised Generative Model

### Steps

Consider a binary classifgication,

**Step 0**

Initialze the model $\theta = \{  P(C_1), P(C_2), \mu^1, \mu^2, \Sigma \} $ by the labelled data as in supervised learning.

**Step 1**

Compute the posterior probability of all the unlabeled data $P_{\theta}(C_1 \vert x^u)$ by the calculated $\theta$.

****
