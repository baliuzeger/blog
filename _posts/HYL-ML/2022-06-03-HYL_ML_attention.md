---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Self-Attention"
---

## Overview

With a vector sequence as input, self-attention can produce a sequence of vectors (or scalars) of the same length. The produced vectors can then be fed into feedforward networks or further self-attention layers. Conceptually, the production of every vector takes into account the whole input sequence, evaluate some parts as more relevant and let the relevant ones contribute more.

![overview](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/overview.png)

## Operations

For a sequence of $n_i$ vectors of $n_a$ dimentions as input, for every vector $a_{i}$, we calculate the relevance $\alpha_{j}$ to every vector $a_j$. We also produce a *value* vector $v_j$ for every vector $a_j$. Then we calculate a weighted sum over $v_j$'s by $\alpha_{j}$'s as the output $b_i$ for vector $a_i$. After calculating $b_i$'s for all the input vectors, we operations of a self-attention layer is done.

The detailed operations:

For every input vector $a_i$, we multiply it by matrix $W^q$ to produce a *query* vector $q_i$. Then for every input vector $a_i$, we multiply it by matrix $W^k$ to produce a *key* vector $k_i$.

Then we calculate the *relevance* $\alpha_{j}$ for every vector $a_j$ to vector $a_i$ by dot product or other computation:

![relevance](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/relevance.png)

Then we use softmax to normalize the $\alpha_{j}$'s to get the $\alpha'_{j}'s$. We can also use other non-linear functions instead of softmax.

![query-key](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/query-key.png)

Then we produce a *value* vector $v_j$ of dimension $n_b$ for every vector $a_j$ by matrix $W^v$. Then we use the $\alpha_{j}$'s as weights to sum the $v_j$'s to get the output vector $b_i$ for $a_i$. By repeating these procedures for all the $a_i$'s, we get the output vectors $b_i$'s for the input sequence $a_i$'s.

![sum-values](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/sum-values.png)

![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/.png)
![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/.png)
![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_attention/.png)

## References

[【機器學習2021】自注意力機制 (Self-attention) (上)](https://youtu.be/hYdO9CscNes)

[【機器學習2021】自注意力機制 (Self-attention) (下)](https://youtu.be/gmsMY5kc-zw)

[Course Website](https://speech.ee.ntu.edu.tw/~hylee/ml/2021-spring.php)
