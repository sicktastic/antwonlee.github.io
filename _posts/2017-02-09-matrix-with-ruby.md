---
layout: post
title:  "Matrix with Ruby"
date:   2017-02-09 12:00:00
categories: Machine Learning, Linear Algebra
banner_image: ""
featured: false
comments: true
---

While doing math in Ruby is little more challenging than Python or R, it is
still my favorite language!  Here is how we create simple matrix with Ruby with
<a href="http://ruby-doc.org/stdlib-2.0.0/libdoc/matrix/rdoc/Matrix.html" target="_blank">matrix class</a> and do a simple multiplication.

<!--more-->

```ruby
require 'matrix'

matrix_a = Matrix[[1, 2], [3, 4]]
matrix_b = Matrix[[-3, -8, 3], [-2, 1, 4]]

result = matrix_a * matrix_b
# => Matrix[[-7, -6, 11], [-17, -20, 25]]
```
