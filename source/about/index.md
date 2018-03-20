---
title: 关于
date: 2018-02-15 23:36:30
type: "about"
---

# 关于about
1. 说是about, 其实就是个说明. 
1. 分类[隔三差五](../categories/隔三差五/)对应于**每日一题**. 由于每日一题之不可得, 那么就不得已而求其次, 故隔三差五.
2. [memo](../maxim)与[絮语](https://logithm.github.io/wiki/mist/murmur.html).
3. [个人wiki](http://logithm.github.io/wiki)是用simiki搭建的, 主要是因为在办公过程中, 总是遇到同样的问题, 做的备忘录.




# Todo
+ [x] 把插图搞清楚. 关于图床部分因为注册需要手机.  
+ [x] todo list.
+ [ ] post的front-matter部分的description不能用冒号, 其实是冒号有重要作用.
+ [ ] latex2html
+ [ ] 




# Done
1. [博客内部链接: pages之间的互相链接](https://qiwulun.github.io/posts/用Hexo和Org写博客──站内链接.html).   
	* 首先, `_config.yml`中, 将	
	```permalink: :year/:month/:day/:title/```	
	修改为	
	```permalink: _post/:title.html```. 	
	* 其次, 比如要在`about`页面上链接`maxim`页面, 只要 `[maxim](../maxim)`即可. 注意是两个`..`, 也不需要加`.html`后缀. 
	另外, `[隔三差五](../categories/隔三差五/)`也是正确的.  
	* 再次, 博客内部某博文链接到另一博文: `{% post_link blog.md %}`, 其中`blog.md`就是那个目标博文的md文件.
2. 插图问题, 解决为 `![](../../../../images/001.png)` . 2018-02-16
3. 换行问题参见: {% post_link hexo %}
