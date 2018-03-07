---
title: NeXT主题的设置
date: 2018-03-06 15:29:57
tags: [next, hexo, config]
categories: 工具
keywords:
mathjax: true
description: 一定要搞清楚next主题的版本.
---

# 基本情况
1. NeXT的版本: v6.0.5 (2018-03-06)



# NeXT主题的设置(看[官网](http://theme-next.iissnan.com/)最好)
1. [基本设置](https://www.jianshu.com/p/efbeddc5eb19) 的[作者](http://www.dragonstyle.win/2017/11/07/Hexo-Next主题优化/), 
[这里是出处](http://blog.csdn.net/qq_33699981/article/details/72716951)   
2. [进一步修改](https://maoyanting.github.io/2018/02/07/hexo-NexT%E7%9A%84%E4%BC%98%E5%8C%96/), 
[这个很详细](https://reuixiy.github.io/technology/computer/computer-aided-art/2017/06/09/hexo-next-optimization.html),
[这个也很好](https://qianling.pw/hexo-optimization/)  ,
[高级设置](https://zhuzhuyule.com/archives/), 
[也不错](http://cxjiang.top/2017/04/07/Hexo-NexT/),
[一些颜色设置](http://www.lazyboy.site/2017/Next%E8%87%AA%E5%AE%9A%E4%B9%89%E6%A0%B7%E5%BC%8F/),

3. 关于换行: [文本编辑器中换行, html中不换行](https://github.com/iissnan/hexo-theme-next/issues/1672)
```
marked:
  gfm: true
  pedantic: false
  sanitize: false
  tables: true
  breaks: false # 此为关键
  smartLists: true
  smartypants: true
  modifyAnchors: ''
  autolink: true
```
update: 已经替换掉markdown的渲染(换成hexo-renderer-pandoc), 所以以上设置已删除. 2018-03-06

4. [修改文章之间的间距](https://github.com/iissnan/hexo-theme-next/issues/1250)
5. [修改字体与颜色](https://www.zhihu.com/question/49405680): `next\source\css\_variable\base.styl`




# mathjax
1. 貌似已经直接支持mathjax了, 并且在每个post的头部, 通过 mathjax:true 来决定是否加载. 
因为想通过修改`\next\layout\_third-party\mathjax.swig`
而达到[方程编号](https://jdhao.github.io/2018/01/25/hexo-mathjax-equation-number/)的目的时, 没有成功. 




# 中英文混排

中英文混排时, 习惯在汉字与英文字母及数字之间留一空白, 此空白被成为"[盘古之白](https://github.com/vinta/pangu.js)". 
写md文件时, 并不需要故意加上这个空白, 跟写tex文件一样. 

[谢朝辉](https://yihui.name/cn/2017/05/pangu/)修改了[pangu.js](https://github.com/vinta/pangu.js)的代码, 我将谢的代码写入了
一个新的文件: zmyjs.js. z的目的是文件排序用的. 
```
(function(u, c) {
  var d = document, t = 'script', o = d.createElement(t),
      s = d.getElementsByTagName(t)[0];
  o.src = u;
  if (c) { o.addEventListener('load', function(e) { c(e); }); }
  s.parentNode.insertBefore(o, s);
})('//cdn.bootcss.com/pangu/3.3.0/pangu.min.js', function() {
  pangu.spacingPage();
});
```

然后, 将zmyjs.js放到`\themes\next\source\js\src`目录下, 修改`\themes\next\layout\_layout.swig`文件,   
将 `<script type="text/javascript" src="/js/src/zmyjs.js"></script>` 放到 `</body>` 之前.
参考[hexo引用自定义js文件和css样式](http://longhaoteng.com/2016/08/01/hexo引用自定义js文件和css样式/).  

如此一来, HTML和LaTeX里都有了自动加空格的方案. 

另有其他[中英文混排](https://www.liaoyuqin.com/post/tools/zhong-ying-wen-hun-pai)的方案.



## update

next的v6.0.5版本中, 已经提到`pangu.js', 参见作者的[安装说明](https://github.com/theme-next/theme-next-pangu).   
需要 `git clone https://github.com/theme-next/theme-next-pangu.git themes/next/source/lib/pangu`





## 已安装的插件
1. [hexo-douban](https://github.com/mythsman/hexo-douban): 生成book/movie/game这几项, 没有music. 另外加载该插件时, `hexo g`速度慢.(已卸载)
2. hexo-math: 
	* `_config.yml`的修改:

	* 需要[把转义符修改](http://kubicode.me/2016/03/16/Hexo/Fix-Hexo-Bug-In-Mathjax/)
	[另一佐证](http://masikkk.com/article/hexo-13-MathJax/), 
	问题出在下划线`_`的多义: 文本的强调与公式的下标.  
	注: 是 `node_modules/marked/lib/marked.js`, 不是 `hexo-renderer-marked` .
3. hexo-heading-index: 标题编号.
4. hexo-browsersync: 本地修改自动刷新.(可能会导致markdown的渲染出问题, 估计是引号个数的事情. 与代码引用格式有关.)(已卸载)

