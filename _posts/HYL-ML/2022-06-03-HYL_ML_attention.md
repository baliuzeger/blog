---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Self-Attention"
---

## Overview

With a vector sequence as input, self-attention can produce a sequence of vectors (or scalars) of the same length. The produced vectors can then be fed into feedforward networks or further self-attention layers. Conceptually, the production of every vector takes into account the whole input sequence, evaluate some parts as more relevant and let the relevant ones contribute more.

![overview](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/overview.png)

## Operation

For a sequence of $n_i$ vectors of $n_a$ dimentions as input, for every vector $a_{i}$, we calculate the relevance $\alpha_{ij}$ to every vector $j$. We also produce a *value vector* $v_j$ for every vector $a_j$. Then we calculate a weighted sum over $v_j$'s by $\alpha_{ij}$'s as the output $b_i$ for vector $a_i$. After calculating $a_i$'s for all the input vectors, we operations of a self-attention layer is done.

### Calculating the Relevance $\alpha$



## References

[【機器學習2021】自注意力機制 (Self-attention) (上)](https://youtu.be/hYdO9CscNes)

[【機器學習2021】自注意力機制 (Self-attention) (下)](https://youtu.be/gmsMY5kc-zw)

[Course Website](https://speech.ee.ntu.edu.tw/~hylee/ml/2021-spring.php)
