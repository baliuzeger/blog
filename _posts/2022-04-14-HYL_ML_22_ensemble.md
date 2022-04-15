---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Ensemble"
---

## Ensemble: Bagging

By Bagging, we create multiple training data sets from the original training data set, train multiple models, and combine all the trained models for inference. For classification, we can use voting as the methodology of the combination; for regression, we can use averaging as the methodology.

Bagging may be helpful when our model is complex and easy to overfit. In other words, bagging is for reducing the error from **variance** of the model. Bagging is for the **strong** models.

![bagging training](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_22_ensemble/bagging-train.png)

![bagging inference](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_22_ensemble/bagging-inference.png)

*Random forest* is the decision tree with bagging.

## Ensemble: Boosting

Boosting is for the **weak** models.

Guarantee: If your ML algorithm can produce classifier with error rate smaller than 50% **on training data**, then You can obtain 0% error rate classifier after boosting.

Framework of boosting:
- Obtain the first classifier $f_1(x)$.
- Find another function $f_2(x)$, which is complementary with $f_1(x)$.
- ...... Find another classifier  $f_n(x)$
- Combine all the classifiers.

To obtain different classifiers, we can create new training sets by re-sampling or re-weighting the training. In real implementation, you only have to change the cost/objective function. For example, we multiply weights for each data points

$$ L(f) = \sum_n l(f(x^n), \hat{y}^n) \to L(f) = \sum_n \mu_n l(f(x^n), \hat{y}^n) $$

By boosting, the classifiers are learned **sequentially**. Not like bagging, where the classifiers can be learned independently.

## References

[Youtube ML Lecture 22: Ensemble](https://youtu.be/tH9FH1DH5n0)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
