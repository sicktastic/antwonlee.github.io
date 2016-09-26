---
layout: post
title:  "kNN(k Nearest Neighbors) Algorithm"
date:   2016-09-09 02:00:00
categories: machine learning, python
banner_image: ""
featured: false
comments: true
---

kNN is one of the algorithm used for <a href="http://math.stackexchange.com/questions/141381/regression-vs-classification" target="_blank">classification and regression</a> in <a href="https://en.wikipedia.org/wiki/Supervised_learning" target="_blank">Supervised Learning</a>.  It is regarded as one of the simplest machine learning algorithm.

<!--more-->

Unlike other Supervised Learning algorithms, it does not have a training phase.  The training and testing is pretty much the same thing.  It is a <a href="https://en.wikipedia.org/wiki/Lazy_learning" target="_blank">lazy learner</a> where training dataset is already stored. Because of that very reason, kNN is not an ideal candidate for algorithm that needs to process large data set.

With kNN, you are basically looking for the closest points to the new point. The `k` represents the amount of nearest neighbors of the unknown point. We provide the `k` amount (Often an odd number) of the algorithm to predict the outcome.

+ kNN is a type of instance-based learning, or lazy learning, where the function
  is only approximated locally and all computation is deferred until
  classification.
+ The kNN algorithm is among the simplest of all Machine Learning Algorithms.
+ In kNN classification, the output is a class membership.  An Object is
  classified by a majority vote of its neighbors, with the object being assigned
  to the class most common among its `k` nearest neighbors (`k` is a positive
  integer, typically small).

<i style="font-size: 10px;">Reference: <a href="https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm" target="_blank">https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm</a></i>

<strong>What does it measure?</strong>
<br />
<a href="https://en.wikipedia.org/wiki/Euclidean_distance" target="_blank">Euclidean Distance</a>.
<div style="margin: 0 auto; width: 100%; text-align: center">
  <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/dc0281a964ec758cca02ab9ef91a7f54ac00d4b7" />
</div>
You can write this in Python like this: `math.sqrt((x2-x1)**2 + (y2-y1)**2)`
<br /><br />
<strong>Pros and Cons?</strong>
<br />
<u>Pros:</u> High accuracy, insensitive to outliers, no assumptions about data.
<br />
<u>Cons:</u> Computationally expensive, high memory requirement.
<br />
<u>Works with:</u> Numeric values, nominal values.
<br /><br />
<strong>Good tools?</strong>
<br />
<a href="http://scikit-learn.org/stable/index.html" target="_blank">Scikit-learn</a> is a great Machine Learning library to perform machine learning algorithm.
<br /><br />
Example of <a href="http://scikit-learn.org/stable/auto_examples/neighbors/plot_classification.html" target="_blank">kNN classification example</a> from scikit:
<img src="http://scikit-learn.org/stable/_images/plot_classification_001.png" />
<script src="https://gist.github.com/antwonlee/bd7859cb32db2884717cd912bb81ac3e.js"></script>
<br /><br />
Example of <a href="http://scikit-learn.org/stable/auto_examples/neighbors/plot_regression.html" target="_blank">kNN regression example</a> from scikit:
<img src="http://scikit-learn.org/stable/_images/plot_regression_001.png" />
<script src="https://gist.github.com/antwonlee/65b936bb167d66a4b3f3e0a257c54264.js"></script>
