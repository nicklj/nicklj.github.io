---
layout: post
title: How to use Latex in Jekyll 
date: 2018-12-24
tags: [Jekyll]
---

The simplest way I found on the Internet to enable Latex in Jekyll.

### Enable MathJax ###

Add the follwing code to '_includes/head.html'
~~~
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    jax: ["input/TeX", "output/HTML-CSS"],
    tex2jax: {
      inlineMath: [ ['$', '$'], ["\\(", "\\)"] ],
      displayMath: [ ['$$', '$$'], ["\\[", "\\]"] ],
      processEscapes: true,
      skipTags: ['script', 'noscript', 'style', 'textarea', 'pre', 'code']
    }
    //,
    //displayAlign: "left",
    //displayIndent: "2em"
  });
</script>
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML" type="text/javascript"></script>
~~~

### Using Latex ###

\\[
e^{ix} = \cos x + i \sin x $$
\\]

### Reference ###
http://blog.lostinmyterminal.com/webpages/2015/01/09/math-support-in-jekyll.html