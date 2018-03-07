---
title: 微信公众号文章排版之mathjax
date: 2018-02-25 22:10:19
tags: [mathjax,css,wechat]
categories: [工具]
keywords:
description: 微信是个封闭系统, 大局域网, 很有想象力. 数学公式的排版是个问题, mathjax 可以将TEX格式的公式输出为 SVG, 而 SVG 是可以直接拷贝到公众号编辑器中的.
mathjax: true
---

html文件中的代码换成以下即可

```javascript
  <script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    extensions: ["tex2jax.js"],
    jax: ["input/TeX","output/SVG"],
    TeX: {
      extensions: ["AMSmath.js","AMSsymbols.js","noErrors.js","noUndefined.js"]
    },
    tex2jax: {
      inlineMath: [["$","$"],["\\(","\\)"]]
    }
  });
  </script>
  <script type="text/javascript" src="https://cdn.bootcss.com/mathjax/2.7.2/MathJax.js"></script>
  ```

  src也可以是:
  ```html
  <script type="text/javascript" src="../mathjax/MathJax.js"></script>
  ```

  如此一来, 就是本地写个md文件, 把 mathjax 放到适当的地方, 借助于工具, 将 md 转为 html , 然后在手工修改一下. 
  等等, pandoc 应该可以自动实现, 通过模板.

  ```javascript
  MathJax.Hub.Config({
    showProcessingMessages: false, //关闭js加载过程信息
    messageStyle: "none", //不显示信息
    extensions: ["tex2jax.js"],
    jax: ["input/TeX", "output/HTML-CSS"],
    tex2jax: {
        inlineMath: [ ['$','$'], ["\\(","\\)"] ], //行内公式选择符
        displayMath: [ ['$$','$$'], ["\\[","\\]"] ], //段内公式选择符
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre','code','a'], //避开某些标签
        ignoreClass:"comment-content" //避开含该Class的标签
    },
    "HTML-CSS": {
        availableFonts: ["STIX","TeX"], //可选字体
        showMathMenu: false //关闭右击菜单显示
    }
});
```


-----------------

在input.txt文件所在目录下, 新建header.swig文件(猜测也可以是js等后缀), 代码如下: 

```html
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  extensions: ["tex2jax.js"],
  jax: ["input/TeX","output/SVG"],
  TeX: {
    extensions: ["AMSmath.js","AMSsymbols.js","noErrors.js","noUndefined.js"],
    equationNumbers: {autoNumber: "all"}
  },
  tex2jax: {
    inlineMath: [["$","$"],["\\(","\\)"]]
  }
});
</script>
<script type="text/javascript" src="https://cdn.bootcss.com/mathjax/2.7.2/MathJax.js"></script>
```

然后, dos切换到当前目录: `pandoc input.txt -t html -s -o output.html --mathjax -H header.swig`. 

参考: [TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/111868/pandoc-how-can-i-get-numbered-latex-equations-to-show-up-in-both-pdf-and-html-o),
[pandoc issues 1938](https://github.com/jgm/pandoc/issues/1938#issuecomment-74011358),



--------
mathjax值得好好喝一壶
1. [hexo中的latex](https://jdhao.github.io/2017/10/06/hexo-markdown-latex-equation/): 基本上解决了问题. 好.
