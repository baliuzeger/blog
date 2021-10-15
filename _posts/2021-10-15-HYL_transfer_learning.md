---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Transfer Learning"
---

**Transfer learning** is about the scenarios that we have data which are not directly directly related to the task considered. Besiedes, the usage of terminologies in the field of transfer learning are somewhat chaotic, so the meaning of some terms may vary between articles.

## Categories of Transfer Learning

![categories](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/overview.png)


## Model Fine-Tuning

We have a large amount of source data and very little target data, both are labbelled. We train the a model by the source data first and then re-train it by the target data. The challenge is that we have only limited target data, so be careful about overfitting.

### Conservertive Learning

Make constraints, i.e. regulatizations, to let some parts of the re-trained model to be close to the pre-trained model.

![conservative training](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/conservative.png)

## My discussions

transfer learning vs semi-supervised learning


## References

[Youtube ML Lecture 19: Transfer Learning](https://www.youtube.com/watch?v=YNUek8ioAJk&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=29)

[Course website](https://speech.ee.ntu.edu.tw/~hylee/ml/2020-spring.html)
