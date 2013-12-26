---
layout: post
title:  "Support Sass in Chrome Dev Tools"
date:   2013-12-26 14:10:18
author: Den Kezlya
tags: 
category: news
---

While working with Compass (sass), we have to have opportunity of debugging scss files.
![Dev Tools](https://developers.google.com/chrome-developer-tools/docs/css-preprocessors-files/sass-debugging.png)

First of all we need correct compass and sass versions with source-map compatibility.
sass - 3.3.0.alpha.149
compass-sourcemaps - 0.12.2.sourcemaps.57a186c

Installtions:
```php
gem install sass -v 3.3.0.alpha.149 --pre
gem install compass-sourcemaps -v 0.12.2.sourcemaps.57a186c --pre
```

If you have different version, you can uninstall them by commands bellow:
```php
gem uninstall sass
gem uninstall compass
```

Now we need to update compass config by adding line:
```php
sass_options = {:sourcemap => true}
```

Ok. Let's make changes in chrome setting.
To enable CSS source maps and CSS reload:
1. Open new tab with link chrome://flags/#enable-devtools-experiments and enable "Developer Tools experiments" support. Reload your browser.
2. 2. Open DevTools Settings and click General.
3. 3. Turn on Enable CSS source maps and Auto-reload generated CSS.
4. ![Dev Tools](http://habrastorage.org/storage2/d9f/fe9/875/d9ffe98756c7fa0d28614e90663785aa.jpg)
