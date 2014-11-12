---
layout: post
title: "Mouse events and images"
date: 2014-09-15 22:30:16 +0100
comments: true
published: false
categories: [Snippet, javascript, images]
---

This snippet provides the `x` and `y` coordinates of the mouse position when clicked.

``` javascript
function coords(event){
  posx = event.offsetX?(event.offsetX):event.pageX-document.getElementById("pointer_div").offsetLeft;
  posy = event.offsetY?(event.offsetY):event.pageY-document.getElementById("pointer_div").offsetTop;
  console.log(posx,posy)
  return [posx, posy]
}
```
