---
layout: post
title:  "Sass Control Directives"
date:   2016-12-31 00:36:00
categories: sass
banner_image: ""
featured: false
comments: true
---

I did not know until today that Sass had a control expressions.  Very cool.

<!--more-->

Notes from Upcase:

Control directives and expressions are useful in a scenario where the same styles are needed several times with variations. The functions available are: @if, @for, @each and @while. Using Sass maps with the @each function is a powerful combination.

```scss
$flashes: (
  "error": #fbe3e4,
  "notice": #e5edf8,
  "success": #e6efc2,
);

@each $type, $color in $flashes {
  .flash-#{$type} {
    background: $color;
    color: darken($color, 10%);
    padding: 10px 20px;
    width: 100%;
  }
}
```
