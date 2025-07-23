---
layout: post
title: "数学latex测试文档"
date: 2025-7-20 10:00:00
blurb: "在GitHub pages引入latex公式以实现数学公式的渲染"
---

<br />
<br />


1.在_includes下添加mathjax_support.html文件

mathjax_support.html详细代码:


{% raw %}
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    TeX: {
      equationNumbers: {
        autoNumber: "AMS"
      }
    },
    tex2jax: {
      inlineMath: [ ['$', '$'] ],
      displayMath: [ ['$$', '$$'], ['\

\[', '\\]

'] ],
      processEscapes: true,
    }
  });
</script>
<script
  type="text/javascript"
  async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML"
></script>
{% endraw %}


<br />
<br />

2.在_includes/head.html添加引入代码

{% raw %}
{% include mathjax_support.html %}
{% endraw %}

下面是一个公式的例子:
$ e = m c^2 $