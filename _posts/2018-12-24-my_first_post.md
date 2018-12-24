---
layout: post
title: How to use Latex in Jekyll 
date: 2018-12-24
tags: [Jekyll]
---

The simplest way I found on the Internet to enable Latex in Jekyll.

## Enable MathJax ##

Add the follwing code to `_includes/head.html`
```javascript
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> 
```

## Using LaTeX ##

Just input equations with `\\[` instead of `$$` in LaTeX

```
\\[
e^{ix} = \cos x + i \sin x 
\\]
```
which shows
\\[
e^{ix} = \cos x + i \sin x 
\\]

## Reference ##
[1. http://blog.lostinmyterminal.com/webpages/2015/01/09/math-support-in-jekyll.html](http://blog.lostinmyterminal.com/webpages/2015/01/09/math-support-in-jekyll.html)

[2. https://stackoverflow.com/questions/26275645/how-to-support-latex-in-github-pages](https://stackoverflow.com/questions/26275645/how-to-support-latex-in-github-pages)