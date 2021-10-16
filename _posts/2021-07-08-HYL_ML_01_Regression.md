---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 1, Regression"
---

## Notations

$x^n$: vector of input # n. The superscript indicates the # of object.

$x^n_i$: feature # i of input # n. The subscript indicates the # of feature/component.

$\hat{y}^n$: the real output # n.

$(x^n,\hat{y^n})$: a data pair.

$f^* = arg \min\limits_{f}L(f)$: find best function f over loss function L (badness).

or $w^* = arg \min\limits_{w}L(w)$: find the best vector of parameters, where $w$ defines a function $f$.

## Gradient Descent

For a loss function $L(w)$:
 1. (Randomly) pick initial $w^0$.
 2. $w^1 = w^0 - \eta \nabla L \vert_{w=w^0}$, where $\eta$ is the learning rate.
 3. repeat step 2 to get $w^2$ ... $w^T$ after $T$ iterations.

Finally, we can get a local minimum (possibly the global minum).

### On evaluating functions

When evaluating functions. what we really care about is the loss over *testing set* but not the *training set*.

## Overfitting

If we can truely find the best function, a more complicated model / larger function set yields lower error on training data, but not always yields lower error on testing data. Such phenomenon is *overfitting*. Therefore, it's important to select the suitable model.

## Regularization

In the example of linear regression, we can add a term $\lambda \sum \vert w \vert ^2$. It let the functions with smaller $w$'s be better, i.e. it prefer smoother functions. It also let noises have less influence over the loss function.

Higher $\lambda$ let the loss function consider the error on training data less, so it increases training error. We prefer smoother functions, but don't make it be too smooth, i.e. becoming constants.

We don't have to perform regulatization on biases because it's not related to smoothness.

## On larger testing data set

Over more testing data, the average error should be higher. Such concepts are related to validation.

## Reference
[Youtube Link ML Lecture 1: Regression - Case Study](https://www.youtube.com/watch?v=fegAeph9UaA&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=3)

[Youtube Link ML Lecture 1: Regression - Demo](https://www.youtube.com/watch?v=1UqCjFQiiy0&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=4)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
