---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: More about Auto-Encoder"
---

## More than minimizing reconstruction error

### To Train the encoder by the discriminator

"An embedding should represent the object", this is the our motivation to make the embeddings. By such concept, we have the question "how to evaluate an encoder". By following the question, we have another approach to train the encoders.

We build an encoder that generate a code by an input object, while this time we build a discriminator that take an input object and a code as its input, and recognize whether the code comes from the object. The encoder has parameters $\theta$ and the discriminator has parameters $\phi$. Let the loss of the diecriminator be $L_D$, then for the discriminator, we train $\phi$ to find the minimum of $L_D^*$, i.e.

$$L_D^* = \min\limits_{\phi} L_D$$

and for the encoder, the lower the $ L_D^* $, the better the representations, so we train $ \theta $ to find the minimum of $ L_D^* $, then

$$ \theta^* = arg \min\limits_{\theta} L_D^* \\
=  arg \min\limits_{\theta} \min\limits_{\phi} L_D $$

we train the encoder and the discriminator simultaneously to minimize $L_D$. This is the **Deep InfoMax** (DIM).

Besides, we can see the typical auto-encoder as a special case of the encoder-discriminator approach. We can simply use the reconstruction error of the typical aotu-encoder as a score for the discriminator.

The encoder-discriminator approach also has some advantages. We don't train an decoder, that saves computing cost. On the other hand, we have more data for the discriminator, i.e. we have both positive (the code comes from the object) and negative (the code doesn't come from the object) examples. While for typical auto-encoder, we have only positive examples.


## More interpretable embedding

## References

[Youtube More about Auto-encoder (1/4)](https://www.youtube.com/watch?v=6ZWu4L7XOiQ&list=PLJV_el3uVTsOK_ZK5L0Iv_EQoL1JefRL4&index=48)

[Youtube More about Auto-encoder (2/4)](https://www.youtube.com/watch?v=hhsfEaVaeQU&list=PLJV_el3uVTsOK_ZK5L0Iv_EQoL1JefRL4&index=49)

[Youtube More about Auto-encoder (3/4)](https://www.youtube.com/watch?v=ZRyoCBCFMOs&list=PLJV_el3uVTsOK_ZK5L0Iv_EQoL1JefRL4&index=50)

[Youtube More about Auto-encoder (4/4)](https://www.youtube.com/watch?v=DRLsw4CshqU&list=PLJV_el3uVTsOK_ZK5L0Iv_EQoL1JefRL4&index=51)

[Course website](https://speech.ee.ntu.edu.tw/~hylee/ml/2020-spring.html)
