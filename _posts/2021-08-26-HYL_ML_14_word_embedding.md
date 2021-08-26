---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 14: Word Embedding"
---

## Approaches to Represent Words

### 1-of-N Embedding

The total number of dimensions is the total number of words. The only 1 dimension with value 1 represent the corresponding word. By such approach, every word is independent and we can't find the relationship between words.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_14/one-of-N.png" alt="1 of N" style="width:400px;"/>
</p>

### Word class

Clustering the words. Since the relationships between the words are complex, so such clustering still lose many information.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_14/word-class.png" alt="word class" style="width:400px;"/>
</p>

## Word Embedding

dimension reduction from 1-of-N to high dimensional word vectors



## References

[Youtube ML Lecture 14: Unsupervised Learning - Word Embedding](https://www.youtube.com/watch?v=X7PH3NuYW0Q&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=23)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
