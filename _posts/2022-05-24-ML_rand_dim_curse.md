---
layout: post
title: "The Curse of Dimensionality"
---

The curse of dimensionality refers to various phenomena that arise when analyzing and organizing data in high-dimensional spaces that do not occur in low-dimensional settings. The common theme of these problems is that when the dimensionality increases, the volume of the space increases so fast that the available data become sparse. In order to obtain a reliable result, the amount of data needed often grows exponentially with the dimensionality. Also, organizing and searching data often relies on detecting areas where objects form groups with similar properties; in high dimensional data, however, all objects appear to be sparse and dissimilar in many ways, which prevents common data organization strategies from being efficient.

In machine learning, the curse of dimensionality is used interchangeably with the *peaking phenomenon* / *Hughes phenomenon*: with a fixed number of training samples, the average (expected) predictive power of a classifier or regressor first increases as the number of dimensions or features used is increased but beyond a certain dimensionality it starts deteriorating instead of improving steadily.

In data mining, the curse of dimensionality refers to a data set with too many features. When exploring the correlation between the features and the results, the total number of combinations grows factorially as the number of features in the data set grows.
