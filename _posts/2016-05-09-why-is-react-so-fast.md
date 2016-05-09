---
layout: post
title:  "Why is React So Fast?"
date:   2016-05-09 07:00:00
categories: React, Javascript
banner_image: ""
featured: false
comments: true
---

Because...

<!--more-->

+ Javascript objects are faster than DOM objects.
+ Te React <a href="https://facebook.github.io/react/docs/glossary.html" target="_blank">virtual DOM</a> is a Javascript object.
+ React never reads from the "real" DOM.
+ React only writes to the real DOM if needed.
+ React efficiently handles DOM updates.

Notes from Eve Porcello

Recommended books on Javascript: <a
href="http://shop.oreilly.com/product/9780596517748.do" target="_blank">Javascript: The Good Parts</a>
