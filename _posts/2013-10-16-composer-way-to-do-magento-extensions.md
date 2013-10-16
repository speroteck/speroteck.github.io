---
layout: post
title:  "Composer way to build magento extensions"
date:   2013-10-16 19:15:18
tags: php magento composer
author: Volodymyr Dubyna
draft: true
category: tutorial
---

[Composer](http://getcomposer.org) is a grate tool to manage extensions and modules inside the project
Unfortunately Magento 1.* does not support it by default but we can easily implement it. Also we expect full composer 
support in Magento 2.*

On [Company Gitlab](http://gitlab.speroteck.com) we created new namespace called **Magento** where we registerd:

1. Magento different versions (community and enterprise)
2. Magento sample data (community and enterprise) 
3. Most used magento modules that could be installed into our base magento

If you don't have access, make a request to me.

How to use all those things together I'll describe in the next post
