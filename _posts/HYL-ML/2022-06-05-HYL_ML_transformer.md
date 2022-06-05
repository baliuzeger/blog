---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Transformer"
---

## Overview

For sequence-to-sequence (seq2seq) tasks, the machine has to take a variable length sequence as input and generate an output sequence whose length is determined by the machine. *Transformer* performs such task.

A transformer is composed of an *encoder* and a *decoder*. The encoder produces a sequence of vectors whose  length is the same as the input sequence. The decoder produces the output sequence from the encoded sdquence.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/transformer-structure.png" alt="transformer-structure" style="width:45a0px;"/>
</p>

## Encoder

The procedure of an encoder layer:
1. Perform multi-head self-attention on the input sequence.
2. Residual connection: add the input sequence to the sequence generated in (1).
3. Perform *layer normalization*.
4. Feed to a feedforward network.
5. Residual connection: add the sequence from (3) to the sequence from (4).

The overall encoder is the composition of multiple encoder layers.

The *layer normalization* is to normalize all the features over an example.

![encoder-procedure](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/encoder-procedure.png)

### On Normalization

There are more approaches for the normalization: [On Layer Normalization in the Transformer Architecture](https://arxiv.org/abs/2002.047 45); [PowerNorm: Rethinking Batch Normalization in Transformers](https://arxiv.org/abs/2003.078 45).

## Decoder

![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/.png)
![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/.png)
![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/.png)

### Auto-Regressive (AT)

### Non-Auto-Regressive (NAT)

## Training

### Teacher Forcing

### Scheduled Sampling

## Further Discussions

### Copy Mechanism

### Guided Attention

### Beam Search


## References

[Youtube【機器學習2021】Transformer (上)](https://youtu.be/n9TlOhRjYoc)

[Youtube【機器學習2021】Transformer (下)](https://youtu.be/N6aRv06iv2g)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
