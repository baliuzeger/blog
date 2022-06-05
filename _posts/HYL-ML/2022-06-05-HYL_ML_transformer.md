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

### Autoregressive (AT) & Non-Autoregressive (NAT)

The original transformer is *autoregressive*. The autoregressive decoder works by the following procedures:

1. Feed the "start" token into the decoder, and the decoder produce the 1st output token.
2. Feed the token produced by the previous step into the decoder, and the decoder produce the next token.
3. Repeat (2) until the decoder produce the "stop" token.

![auto-regressive](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/auto-regressive.png)

For a *non-autoregressive* decoder, all the tokens of the output sequence are produced simultaneously. To decide the output length, we can either train another predictor to predict the output length or let the decoder output a very long sequence and ignore tokens after "end". The NAT decoders have some advantages. By the NAT decoders, all the outputs tokens are computed parallelly. The generation by NAT decoders is more stable in some tasks, e.g. text-to-speech (TTS). However, usually the performance of AT decoders are better than the NAT decoders. *Multi-modality* may be a cause. ([To learn more.](https://youtu.be/jvyKmU4OM3c))

![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/.png)
![](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_transformer/.png)


### Masked Attention

### Cross Attention

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
