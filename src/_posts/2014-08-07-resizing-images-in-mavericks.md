---
layout: post
title: "Resizing images in Mavericks"
date: 2014-09-15 21:38:33 +0100
comments: true
published: true
categories: blog
---

After a search for batch resizing tools, which most require a bit of fiddling around with.
I found a handy command line tool which comes with maverick, [sips](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/sips.1.html).

``` bash
sips -Z 1024 *.jpg
```

If you run the above in a directory of pictures, it will resize all pictures in the current directory.
For my needs, I passed `-Z` to keep the ratio, and a maximum height of 1024 pixels.

As always, make sure to keep the original in case you don't like the results!