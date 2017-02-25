---
layout: post
title:  "Javascript: The Good Parts"
date:   2017-02-25 12:00:00
categories: Javascript
banner_image: ""
featured: false
comments: true
---

Most programmers love to hate Javascript, because some of the bad parts of the
language are really bad while some of the good parts of the language are really
good.

<!--more-->

One of my favorite programming book is <a href="http://shop.oreilly.com/product/9780596517748.do" target="_blank">Javascript: The Good Parts</a> written by <a href="https://en.wikipedia.org/wiki/Douglas_Crockford" target="_blank">Douglas Crokford</a>, who is known for his involvement with JSON, JSLint, and more.

For next few blog posts, I am hoping to concentrate on writting more about his point of views regarding Javascript.  If you are like me who writes code for the web, Javascript is an essential language for you to master.  Douglas will teach you some great parts of the language while warning you about the bad parts.  I highly encourage you to read his book.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hQVTIJBZook"
frameborder="0" allowfullscreen></iframe>

<br />

For this post, let's look at a simple example of <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness" target="_blank">double equal operator</a> in Javascript.  It is supposed to be a equality operator, but because it performs coercion prior to comparison in Javascript&mdash;it can lead to false positives.  If you are new to the language, a simple thing like that can make mathematical law of transitivity a nightmare.

Here are some examples:

```javascript
0 == ''           //true
0 == '0'          //true
'' == '0'         //false
fasle == 'false'  //false
false == '0'      //true
" \t\r\n " == 0   //true
```

When you are writting code, one of the things you want to make sure is that it is not confusing.  For this very reason, Douglas argues we should <u>always</u> use ===, and never == for comparison.

I agree.
