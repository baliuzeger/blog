---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Transformer"
---

## Overview

For sequence-to-sequence (seq2seq) tasks, the machine has to take a variable length sequence as input and generate an output sequence whose length is determined by the machine. *Transformer* performs such task.

A transformer is composed of an *encoder* and a *decoder*. The encoder produces a sequence of vectors whose  length is the same as the input sequence. The decoder produces the output sequence from the encoded sdquence.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/transformer-structure.png" alt="transformer-structure" style="width:450px;"/>
</p>

## Encoder

## Decoder

### Auto-Regressive (AT)

### Non-Auto-Regressive (NAT)

## Training

### Teacher Forcing

### Scheduled Sampling

### Copy Mechanism

### Guided Attention

### Beam Search


## References

[Youtube【機器學習2021】Transformer (上)](https://youtu.be/n9TlOhRjYoc)

[Youtube【機器學習2021】Transformer (下)](https://youtu.be/N6aRv06iv2g)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
