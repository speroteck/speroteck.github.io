---
layout: post
title:  "Don't let compiled css files conflict in a rebase"
date:   2013-12-26 14:10:18
author: Den Kezlya
tags: 
category: tutorial
---

We don’t want compiled css files to merge, we just want their source files to merge cleanly.

*Set up a merge driver in your **.git/config** file:
```php
[merge "ours"]
    name = "Keep ours merge"
    driver = true
```
Then tell your built files to use that merge driver in your **.gitattributes** file:
```php
src/skin/frontend/responsivetheme/default/css/app.css merge=ours
src/skin/frontend/responsivetheme/default/css/app.css.map merge=ours
```

When merging built CSS files, use **--ours**, as in **git checkout --ours file**, which will use their branch’s version of the file. That’s not a typo, Git is just weird. Instead of trying to merge the files, it just picks one version over the other. The next section tells us how to automatically rebuild the files so they aren’t out of sync after a rebase.
