---
title: 乱七八糟
date: 2018-02-27 20:56:13
type: "backup"
---

1. [实时监测文件的变化(livereload)](http://www.hahack.com/codes/livereload-for-hexo/)
* `$ npm install hexo-livereload --save`
* 安装livereload的[浏览器插件](http://livereload.com/extensions/)

	ps: 没成功.

1. [hexo-toc](https://github.com/bubkoo/hexo-toc)可行

1. freemind主题修改post的标题大小在 `themes\freemind\source\css\style.ss`中

1. 今天比较兴奋的是通过wixo/freemind这两个主题, 发现几个好玩的博客. 2018-02-27

1. 人生能有几回搏啊, 自己喜欢的事情是做些文字工作, 比如coding, 要是早点能发现自己的喜好并且能为之一直投入的话, 是多么幸福的事情. 2018-02-27

1. 


# 备忘录 
from github(mymd/memo)


3. [反复引用同一个脚注](http://bbs.ctex.org/forum.php?mod=viewthread&tid=65541)

4. [通过css弄一个按钮](https://segmentfault.com/q/1010000003846721)

5. [markdown的一种实现形式](http://mixu.net/markdown-styles/) (便于切换css主题,可以生成目录,ubuntu下已实现,看首页说明即可.)
猜windows下也是可以的, 因为npm安装啊.(ps:的确可以.2017-10-12) windows下: C:\Users\user\AppData\Roaming\npm

6. [可以把一整个font-family都下载下来](https://zh.fonts2u.com/)

7. [font-family](http://www.larrycaiyu.com/): master.css
``` css
body {
  font-family: Rockwell, Verdana, sans-serif;
  letter-spacing: 0em;
  background: #fff url(/images/header_bg.gif) repeat-x top;
  color: #353B40;
  margin: 0;
  padding: 0;
  font-size: 1.1em;
}
```
8. markdown, wiki, 可以在latex中直接使用, 已经有相应的宏包了. 可能需要pdflatex. (latexstudio中的莲枝)

9. [wrapfig宏包可以实现左右排版](1-1.tex): 但是不能与列表环境互相嵌入.
``` latex
\begin{wrapfigure}[12]{r}[34pt]{5cm}
\begin{tikzpicture}
....
\end{tikzpicture}
\end{wrapfigure}
``` 

10. [zhlipsum 随机填充汉字](https://github.com/Stone-Zeng/zhlipsum)

11. tikzlog-1405.pdf: xyz轴指向的自定义(P18)
```latex
\begin{tikzpicture}[x={(-.1cm,-.15cm)},y={(1cm,0cm)},z={(0cm,1cm)}]
\draw[->] (-5,0,0) -- (5,0,0) node[below] {$x$};
\draw[->] (0,-2,0) -- (0,2,0) node[right] {$y$};
\draw[->] (0,0,-1) -- (0,0,3) node[above] {$z$};
\draw[color=red] plot[domain=0:2*pi] ({sin(\x r)},{cos(\x r)},2);
\draw[color=red] (0,0,0) -- (0,1,2) (0,0,0) -- (0,-1,2);
\end{tikzpicture}
```
12. [跨页表格/代码框](http://www.latexstudio.net/archives/10645) 还不错的book类

13. [开源微积分巨著《APEX Calculus》](http://www.latexstudio.net/archives/10627) [latex排版](https://github.com/APEXCalculus/APEXCalculus_Source)

14. ---[st3](https://9iphp.com/web/html/sublime-text-3-license-key.html)---
```
—– BEGIN LICENSE —–
Morin
2 User License
EA7E-924018
184B9FDB 02612F57 33B15E69 BBC567F1
E20FA231 C077EA95 CC14B48B 71DD2536
E209843A 94D13692 03AC2FAA 895B688D
B8F4A0E6 FDC15964 A5573FD7 6405ED1E
6F205469 7F34C69D 3D36E475 52AF6A5B
DFD15C31 85BA64EF F95DD592 4B42C314
AC655762 C0F0F5A1 018824E4 17C56E16
AC5AA84C 034F7A53 2C9A801B 8AED239F
—— END LICENSE ——
```
1. st3 code
```
—– BEGIN LICENSE —–
TwitterInc
200 User License
EA7E-890007
1D77F72E 390CDD93 4DCBA022 FAF60790
61AA12C0 A37081C5 D0316412 4584D136
94D7F7D4 95BC8C1C 527DA828 560BB037
D1EDDD8C AE7B379F 50C9D69D B35179EF
2FE898C4 8E4277A8 555CE714 E1FB0E43
D5D52613 C3D12E98 BC49967F 7652EED2
9D2D2E61 67610860 6D338B72 5CF95C69
E36B85CC 84991F19 7575D828 470A92AB
—— END LICENSE ——
```



## 关于备课笔记  
高一高二的与高三的不适合放在一起, 一方面是因为小节的安排有不同, 另一方面难道也会有不一样. 
故把新课的备课笔记与高三复习的备课笔记分成两个文件, 相互对照.  
    *  新课: 知识点,例题,习题(ABC)
    *  复习课: 高三貌似不适合讲课. 把题收集整理好就可以了. 适当的专题还是需要的.  
    
    
## others
1. pandoc -t beamer --latex-engine=xelatex --template=my_beamer_template slides.txt -o example004.pdf

pandoc -t beamer -i --latex-engine=xelatex --template=my_beamer_template slides.txt -o example004.pdf

其中的 -i 选项是为了让内容逐条显示(点击/空格etc)

% http://liumh.com/2014/07/05/pandoc-produce-slide-shows/  

% http://notes.11ten.net/markdown-beamer.html  

2. 关于rss: inoreader有ios/网页,可以同步; foxmail没有ios.

## office

1. [Nordri Tools: ppt插件](https://www.zhihu.com/question/52157612), 已改名为[islide](https://www.islide.cc/)

2. [dos一键获取已连wifi密码](https://laod.cn/black-technology/cmd-obtain-wifi-password.html)
``` 
for /f "skip=9 tokens=1,2 delims=:" %i in ('netsh wlan show profiles') do  @echo %j | findstr -i -v echo | netsh wlan show profiles %j key=clear
```
3. [关于makefile的例子](https://github.com/tzhuan/ntu-thesis/wiki)



# blog todo

1. [blog html5 slides](http://www.lancezhange.com/2015/11/24/iframe-for-presentation-embedding/)
[嵌入html5,用js](http://www.lancezhange.com/2015/11/23/jmpress-js-in-hexo/)

1. [about mathjax](http://www.lancezhange.com/2015/05/18/Hello-Hexo-and-Goodbay-Octopress/)

1. [maupassant主题](https://www.haomwei.com/technology/maupassant-hexo.html)


# maths todo
from github(mymd/mymaths)

## 问题征解
1. $P$是空间固定点, 过$P$的平面与三轴交点分别为$A,B,C$.   
问: 当$\triangle{ABC}$的面积最小时, 周长最小时, 四面体$O-ABC$的体积最小时, 表面积最小时, 
点$P$在$\triangle{ABC}$的什么位置? 或者是什么心? [链接](http://kuing.orzweb.net/viewthread.php?tid=4135&extra=page%3D1)


## todo
1. [虚拟对称轴法](http://kuing.orzweb.net/viewthread.php?tid=4093&rpid=17937&ordertype=0&page=1#pid17937)  
	<img src="../../../images/m1.png"  alt="图片名称"  style="zoom:80%"/>  
	<div align = center><img src="../../../images/m1.png"/></div>
	> 第二小问分离变量后，再用虚拟对称轴法搞定，呵呵！ 

2. [EMV定理](http://www.artofproblemsolving.com/community/c6h205183p1130901)
	* [例子1](http://zhidao.baidu.com/question/135293985758459725.html), 此链接中有有用信息.

3. ~~[数列型的不等式水母](http://kuing.orzweb.net/viewthread.php?tid=2374&extra=page%3D3)~~

4. ~~[关于$\ln{x}$的不等式](http://kuing.orzweb.net/viewthread.php?tid=2517&extra=&page=1)~~

5. [距离的最大最小值](http://kuing.orzweb.net/viewthread.php?tid=4032&extra=&page=1)

6. [互相垂直焦点弦的中点连线](http://kuing.orzweb.net/viewthread.php?tid=3901&extra=page%3D4)

7. [三角形分布](http://kuing.orzweb.net/viewthread.php?tid=3918&rpid=16969&ordertype=0&page=1#pid16969)

8. 常庚哲 数学竞赛中的函数[x] 中科大 1989

9. kuing论坛上帖子, 每一楼都得看, 水很少.

10. [Soddy圆](http://kuing.orzweb.net/viewthread.php?tid=3818&extra=page%3D10)

11. [单峰函数的广义对称](http://kuing.orzweb.net/viewthread.php?tid=3277&extra=page%3D10)

12. 驻点

13. [惯性矩不等式](http://kuing.orzweb.net/viewthread.php?tid=3567), kuingluing20151222 T1.5.5

14. 一元三次方程的求根公式, 关键是那个变换. [卡当公式](http://kuing.orzweb.net/viewthread.php?tid=3275); T2.2.11.

15. 轮换的经典设中间法: kuing T2.1.13的注

16. 做一个小学初中经典题目的集子. kuing T2.2.7

17. 切比雪夫多项式. kuing T2.3.2

18. T2.4.2

19. kuing在数学空间上写了个错题集, 之前看过部分, 有时间要看完.

20. 作差有理化放缩法 kuing T3.5.1 数学空间, 2013(4): 30-37.

21. 三角函数公式微型整理 数学空间, 2011(2): 8-15.

22. main33与main46中的高斯函数需要整合.

23. 关键在于意识, 比如cauchy不等式及其分式形式.

24. 半凹半凸定理. kuing T4.6.5 P426   kuing T4.6.50 P472

25. Hlawka不等式, Hlawka恒等式: kuing T4.6.58 P483

26. kuing T4.6.60,61,62貌似很经典.

27. 复数各个方向的自我加深, 另外还有极坐标.

28. 平面几何的几大定理: Pascal, M等.

29. 极点极线: (1) 自行参考高等几何的书籍(kuing P527)  (2) http://kuing.orzweb.net/viewthread.php?tid=4798

30. kuing T5.2.6 P676 椭圆上动点到定点距离最值问题,直线上动点到三定点的距离和最值问题,这些一般来说都会遇到四次方程,
除了特殊情况或者数据是精心设计过的才会有简单解.

31. pappus定理 kuing T5.2.56

32. > 由于转化出来的是下凸，意味着各种方法都可以随便撸，比如说切线法啊，配方+三角形不等式+均值啊等等 [链接](http://kuing.orzweb.net/viewthread.php?tid=4844)


# geogebra使用备注
from github(gitme)

1. 手工画图, 然后导出pgf/tikz, 再放到standalone.tex中生成pdf插入.tex中去:
	1. 把坐标系放大, 正常情况下$4\times 4$正好; 
	1. 图画好后, 将图放在第一象限, 最好贴着坐标轴, 理由在下一步;
	2. 在导出pgf/tizk代码时, 在对话框中填入$x_{\min},y_{\min}, x_{\max},y_{\max}$, 生成pgf/tikz代码; 
	3. documentclass选择为standalone, 拷贝代码, xelatex生成pdf.
![](../../../images/geogebra001.png)

2. 高级选项中的任何修改, 都要返回上级菜单, 选择"保存设置". 


1. 新增文件, 写好文件, 然后上传. 只有上传是git的事情, 其他都不是.  
``` 
git add files.md 
git commit -m "注解说明"
git push origin master
```  

3. git的日常  
上班: `git clone git@github.com:xyzio/gitme.git`  
下班:  
```
git add git.md 
git commit -m "注解说明"
git push origin master
```  

4. [多个github帐号的SSH key切换](http://ju.outofmemory.cn/entry/16775)

5. [用github Pages和Jekyll搭建blog](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html),
[另一种教程](http://www.cnfeat.com/blog/2014/05/11/how-to-build-a-blog/),   

[还有](https://www.ezlippi.com/blog/2015/03/github-pages-blog.html)  
> 在该目录下手动创建如下文件和文件夹，最终形成这样的结构：  
	*  _includes：默认的在模板中可以引用的文件的位置，后面会提到  
	*  _layouts：默认的公共页面的位置，后面会提到  
	*  _posts：博客文章默认的存放位置  
	*  .gitignore：git将忽略这个文件中列出的匹配的文件或文件夹，不将这些纳入源码管理  
	*  _config.yml：关于jekyll模板引擎的配置文件  
	*  index.html：默认的主页  


# 好玩的东西

1. [给博客加上一言经典语句](https://laod.cn/design/page/hitokoto-yiyan.html), [一言](http://hitokoto.cn/)  
F5刷新一次, 更新一次一句话.

1. [Microsoft Office 2013, 不能打开文件]()  
> 要把office的信任中心的设置修改下

1. [duckduck搜索](https://duckduckgo.com/), 
[猴油脚本: Douban Download Search（支持https）](https://greasyfork.org/zh-CN/scripts/21316-douban-download-search-%E6%94%AF%E6%8C%81https)的代码里面有关于duckduckgo示例.

1. [鸠摩搜索(电子书)](https://www.jiumodiary.com/): 用来搜书.

1. [用于国内外网盘内容搜索](http://www.pansou.com/) 

1. [Library Genesis （创世纪图书馆）](http://gen.lib.rus.ec/): 地球上最牛的（英文）电子书站点. 内容极其丰富，电子书质量极高！
这个站点让你免费下载超过 200 万本高质量书籍，包括科研论文、小说、漫画、杂志等。

1. [古腾堡计划](http://www.gutenberg.org/)

1. [Axmath](http://www.axmath.icoc.cc/): 公式编辑器, 收费, 国产, 评论说卸载时可能有问题, 所以拒绝使用.  

1. [Word中高效输入公式](https://zhuanlan.zhihu.com/p/27072646)
> Word2013中自带的公式输入已经很好了, 部分兼容LaTex语法. 把默认的字体替换一下, 更数学.  


1. [Windows下的高效工具](https://www.zhihu.com/question/22919326/answer/23499484)  
	* --TeraCopy: 用于copy大量文件, 但是收费, 所以不要.--
	* Chocolatey: Windows上的apt-get, 没试过.

1. [Windows软件列表](https://github.com/zmywly8866/Programer-s-tools-list)

1. [Capslock+](http://cjkis.me/capslock+/): 一个加强 Capslock 键的功能，以提高效率的工具. [使用说明就只看这一个.](https://www.zhihu.com/question/22919326/answer/201183511)

1. [FreeFileSync](https://sourceforge.net/projects/freefilesync/): 用于同步文件, 比如pc与u盘, 比如备份盘与工作盘. 记得Windows自家就有类似工具.

1. 
--------------------

1. [floatrow宏包](http://www.latexstudio.net/hulatex/package/float.htm), 使用实例参见[ab_preamble.tex](https://github.com/jermer/alg-book)  

1. [setspace宏包少用](http://bbs.ctex.org/forum.php?mod=viewthread&tid=68537)  

1. [epigraph宏包用来写章节头上的一句名人名言](http://www.cnblogs.com/Eufisky/p/3801317.html)

1.  做个glossary(名词/术语索引)还是很有作用的. 使用实例参见[ab_preamble.tex](https://github.com/jermer/alg-book).  

1. [ab_preamble.tex](https://github.com/jermer/alg-book)中的插图(一行多图)可以参考.  

-------------------
1. [st3的一些设置](https://jdhao.github.io/2017/03/19/windows-sublime-usage-related-issue/): 好.

1. [st3与markdown](https://jdhao.github.io/2017/03/04/Sublime-Windows-Markdown/)

1. [hexo-next](https://jdhao.github.io/2017/02/26/hexo-install-use-issue/)