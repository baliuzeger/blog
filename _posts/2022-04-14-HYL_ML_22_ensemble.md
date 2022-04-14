---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Ensemble"
---

## Ensemble: Bagging

By Bagging, we create multiple training data sets from the original training data set, train multiple models, and combine all the trained models for inference. For classification, we can use voting as the methodology of the combination; for regression, we can use averaging as the methodology.

Bagging may be helpful when our model is complex and easy to overfit. In other words, bagging is for reducing the error from **variance** of the model.

![bagging training](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_22_ensemble/bagging-train.png)

![bagging inference](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_22_ensemble/bagging-inference.png)

*Random forest* is the decision tree with bagging.

## References

[Youtube ML Lecture 22: Ensemble](https://youtu.be/tH9FH1DH5n0)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
