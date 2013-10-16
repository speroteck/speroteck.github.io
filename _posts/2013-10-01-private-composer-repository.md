---
layout: post
title:  "Speroteck private package manager based on Composer"
date:   2013-10-01 19:15:18
author: Volodymyr Dubyna
tags: php composer
category: news
---

After some months of investigations, tries and failures we at last present
our own package manager for `PHP` libraries.
It is based on `composer` which contains a lot of features and the knowledge of it is a `must have` feature
of the modern developer.

It is located on [composer.speroteck.com](http://composer.speroteck.com).

Honestly I don't like their `strange` logo. But anyway it is hard to forget that `maestro` with "square" face.

![Composer Image](http://getcomposer.org/img/logo-composer-transparent.png)

### How to use it is extremely simple. Some examples to impress.

See full documentation on [composer](http://getcomposer.org) site and some examples in our repository [](https://gitlab.speroteck.com/speroteck/composer-repository/tree/master)
Don't forget to ask access to see content.

{% highlight bash linenos %}
# Add Speroteck repository to global configuration of composer
composer config --global repositories.speroteck composer http://composer.speroteck.com/

# Look for speroteck repositories
composer search speroteck

# Get information about package
composer show speroteck/quickview

# Create magento project
composer create-project -s dev speroteck/magento-ee mage1.13 1.13.0.2-dev
{% endhighlight %}



