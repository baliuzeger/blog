---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Transfer Learning"
---

**Transfer learning** is about the scenarios that we have data which are not directly directly related to the task considered. Besiedes, the usage of terminologies in the field of transfer learning are somewhat chaotic, so the meaning of some terms may vary between articles.

## Categories of Transfer Learning

![categories](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/overview.png)


## Model Fine-Tuning

We have a large amount of source data and very little target data, both are labbelled. We train the a model by the source data first and then re-train it by the target data. The challenge is that we have only limited target data, so be careful about overfitting. We have the following methods:

### Conservertive Learning

Make constraints, i.e. regulatizations, to let some parts of the re-trained model to be close to the pre-trained model.

![conservative training](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/conservative.png)

### Layer Transfer

When training by the target data, we copy some layers of the pre-trained network, while the others are randomly initialized. If we have very limited data, then we fix the transfered layers and train only the others; if we have sufficient data, then we fine-tune the whole network.

Which layers to be transfered dependes on the task. For example, for image recognition, usually we fine-tune the last layers because the former layers are for extracting pattenrs fram the images; for speech recognition, ususally we fine-tune the first layers because the parameters for extracting patterns varies to fit the unique vocal mechanisms of individuals.

![layer-transfer](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/layer-transfer.png)

## Multi-Task Learning

We let multiple networks share some layers.

![multi-task learning](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/multi-task.png)

To let the network learn which layers to be shared, there's Progressive Neural Networks.

![progressive NN](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_19/progressive.png)

## My discussions

transfer learning vs semi-supervised learning



## References

[Youtube ML Lecture 19: Transfer Learning](https://www.youtube.com/watch?v=YNUek8ioAJk&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=29)

[Course website](https://speech.ee.ntu.edu.tw/~hylee/ml/2020-spring.html)
