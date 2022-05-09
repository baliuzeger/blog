---
layout: post
title: "Chap 3: Capital Share Bikeshare Predictor"
---

### Import

![0_import](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/00_import.png)

### Data Preprocess
#### Load & View the data
![1_view-data-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/01_view-data-1.png)
![1_view-data-2](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/01_view-data-2.png)

#### make 1-hot & binary input features
check total number of classes to separate the binary and those has more than 2 classes.
![2_check-classes](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/02_check-classes.png)

make the 1-hot features
![3_dummy-fields-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/03_dummy-fields-1.png)
![3_dummy-fields-2](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/03_dummy-fields-2.png)

include the binary features into the dataframe of input.
![04_binary_features-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/04_binary_features-1.png)
![04_binary_features-2](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/04_binary_features-2.png)

#### process the quantitative data
normalize the quantitative data.
![05_quantitative](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/05_quantitative-1.png)

add then into the input & target dataframe.
![05_quantitative](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/05_quantitative-2.png)
![05_quantitative](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/05_quantitative-3.png)

#### make the input & target tensors
![06_tensor-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/06_tensor-1.png)
beware the `values.reshape(len(df_tgt),1)`. For the output is only 1 dimensional, such reshape help avoid the warning of dimensional mismatch.
![06_tensor-2](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/06_tensor-2.png)

#### make dataset objects
![07_dataset-obj](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/07_dataset-obj.png)

#### define & make model
![08_define-model](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/08_define-model.png)

#### make train & test function
![09_train-test-fn-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/09_train-test-fn-1.png)
![09_train-test-fn-1](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/09_train-test-fn-1.png)

![](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/.png)
![](https://baliuzeger.github.io/sjl/assets/images/kionge_ch3_bicycle/.png)
