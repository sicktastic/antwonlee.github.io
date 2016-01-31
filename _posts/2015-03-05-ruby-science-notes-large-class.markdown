---
layout: post
title:  "Ruby Science Notes: Large Class"
date:   2015-03-05 15:23:00
categories: Ruby
banner_image: ""
featured: false
comments: true
---

I started reading [Ruby Science](https://gumroad.com/l/ruby-science) by [Thoughtbot](http://thoughtbot.com).  I really love this agency, and I learn most of my rails knowledge from [Upcase](https://upcase.com).
<!--more-->

According to the book, here are some indications where your class might be little too large than it ought to be:

+ You can't easily describe what the class does in one sentence.
+ You can't tell what the class does without scrolling.
+ The class needs to change for more than one reason.
+ The class has more than seven methods.

You should look at one of your large class, and see if any of these attributes are true.
