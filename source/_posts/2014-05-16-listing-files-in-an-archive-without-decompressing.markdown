---
layout: post
title: "Listing files in an archive without decompressing"
date: 2014-05-16 18:05:11 -0700
comments: true
categories: [How to, Unix]
---

## The problem

My Macbook Pro has a fairly small hardrive, so I try to compress files that I do not need on an everyday basis. Mac OS X tends to decompress any archive file that you click on and I needed to check the content of an archive that resided on Dropbox.

## The solution

The archive I was looking at was a tar.gz archive. It turns out tar does this very well, which I found out through [this blog](http://www.tannerwilliamson.com/2009/10/16/view-gzip-tar-gz-archive-file-contents-without-extracing-files/) :

``` console
tar -tf nameofthearchive.tar.gz
```

or without the dash (BSD-style options) :

``` console
tar tf nameofthearchive.tar.gz
```

If the archive is a zipfile, one can use the **zipinfo** command :

``` console
zipinfo nameofthearchive.zip
```

or **unzip -l** :
``` console
unzip -l nameofthearchive.zip
```


