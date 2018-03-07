---
title: LaTeX 笔记
date: 2018-02-22 09:56:22
tags: [tex, tips, package, updating]
categories: [工具]
keywords:
description: 如题
mathjax: true
---

# 切记
* .cls/.sty/package选择用default选项最好, 因为可移植性强.
* 抛弃CJK, 转投utf8.
* 放弃ctex套装, 不用miktex, 选择texlive. (据说mac下选择mactex).
* xelatex+ctex宏包
* 


# tips

1. [拼凑中文生僻字](https://yangwenbo.com/articles/latex-tips-2010-04.html)
```
	\hbox{\scalebox{0.4}[1]{王}\scalebox{0.6}[1]{莹}}
```
2. [为插图加框](https://yangwenbo.com/articles/latex-tips-2010-04.html)
```
	\fbox{\includegraphics[width=0.9\textwidth]{figname}}
```
3. latex中没有theorem环境, 所谓的theorem其实是一个集合名称, 可以通过定理环境来定义你需要的定理/引理/...等环境.(这个理解有问题)

4. newenvironment得到的是列表(item); 而newtheoremstyle得到是单个环境,如begin{example}, 无非给个counter, 比如例3.4.1.(这个理解有问题)

5. [smash: 以将已有的盒子拍扁，保持宽度不变，但将高度和深度变为零](http://zoho.is-programmer.com/user_files/zoho/File/latexlog.pdf)

6. 排版试卷直接用bhcexam宏包就可以了(2016-09-13), xelatex, 看test3与test4头文件的区别. D:\TEX_aux

7. [autoref命令直接产生“图1.1”“式1.1”等样](http://www.latexstudio.net/archives/7446)

1. [latex 表格列宽度固定的情况下让文字居中显示](http://jincheng.blog.51cto.com/4625177/1604688): 
```
	在列宽后加入<{\centering}, 即从{p{2cm}}改为{p{2cm}<{\centering}}
```

1. 当前（2015-05-04）相对成熟且稳定的技术是 xeCJK，推荐使用；更早的技术则不推荐使用；LuaTeX-ja 是日本方面开发的，基于 LuaTeX 引擎，有诸多问题，
建议观望. [知乎孟晨](https://www.zhihu.com/question/30090572)

2. 可以说几乎每个人都走过使用 CJK 宏包然后搞一大堆问题出来的弯路，我也不例外。不怪新手，百度一下“LaTeX 中文”，有一半以上还在拿 CJK 宏包说事儿的。
这在十年前不是弯路，而是支持中文的几乎唯二的道路之一（另一条是CCT）。但是这是一个很难配置的宏包，中文字体这一关就烦死个人，而且和其
他宏包在一起用的时候会出大大小小各种问题。所以为了你自己方便，也为了方便他人帮助你解决问题，用 LaTeX 排版中文请先学会使用 xeCJK 宏包。
[知乎Louis Stuart](https://www.zhihu.com/question/30090572)

3. 这两个警告在只加载amsmath时就出现
```
W: E:\yaodoc\desktop\texmtest\main01.tex:41 Font shape `OMX/cmex/m/n' in size <10.54> not available(Font) size <10.95> substituted  
W: E:\yaodoc\desktop\texmtest\main01.tex:0 Size substitutions with differences(Font) up to 0.41pt have occurred.  
```

4. 关于书签: UTF-8 + XeLaTeX(目前最最最最最最最最推荐的方式)[知乎孟晨](https://www.zhihu.com/question/25074347)

5. [关于中文书签](https://www.zhihu.com/question/25074347)




# 各种宏包
## enumitem
1. [ctex宏包的\chinese与enumitem宏包](https://github.com/CTeX-org/ctex-kit/issues/209)  
`\begin{enumerate}[label = \chinese* ]` 报错的解决方案:   
`\AddEnumerateCounter{\chinese}{\chinese}{\quad}`

2. [如何才能让enumitem的各级标题随着level改变大小](http://bbs.ctex.org/forum.php?mod=viewthread&tid=74847)
```
	\setlist[enum, 1]{label*=\arabic*., listparindent=21pt, font=\bfseries\tiny, before*=\erhao }
	\setlist[enum, 2]{label*=\arabic*., listparindent=21pt, font=\bfseries\tiny, before*=\sihao }
	\setlist[enum, 3]{label*=\arabic*., listparindent=21pt, font=\bfseries\tiny, before*=\wuhao }
```
3. 编号黑体化  
```
	\begin{enumerate}[font=\textbf]
```

4. 列表宏包: enumerate, enumitem, paralist


## 关于hyperref宏包
1. autoref: chapter,section,example,code,figure,table,equation.  
问题是相应的设置, 比如thechapter, 比如\label{chap:vector}对应的\autoref{chap:vector}, 这里的chap.  
\xxxautorefname, 其中的 xxx 可取: equation, theorem, footnote, item, figure, table, part, ppendix, chapter, 
section, subsection, subsubsection, paragraph, subparagraph, page.


## 常见宏包简介
1. [9 essential LaTeX packages everyone should use](http://www.howtotex.com/packages/9-essential-latex-packages-everyone-should-use/)
	* amsmath
	* geometry
	* graphicx
	* nag
	* microtype
	* siunitx
	* cleveref
	* hyperref
	* booktabs
2. 中文支持
	* ctex - 封装好的中文支持和版式调整工具，定义了许多方便的工具  
	* xeCJK - XeLaTeX 下的中文字体选择和禁则、压缩的处理  
	* fontspec - XeLaTeX 下的西文字体选择  
3. 页面布局类
	- geometry - 调整页面大小、页边距等尺寸  
	- fancyhdr - 设计页眉页脚  
	- titlesec - 设计章节标题格式  
	- titletoc - 设计目录格式  
4. 超链接和 PDF 的各种功能。  
	* hyperref - 超链接，PDF 书签，PDF 表单，PDF 元信息……  
	* media9 - 插入 Flash、视频等  
5. 图表和浮动体。
	* graphicx - 插图
	* xcolor - 颜色
	* tikz - 绘图
	* booktabs - 三线表
	* multirow - 列合并单元格（cell）
	* makecell - 在单元格内手动换行
	* longtable - 换页表格
	* tabu - 封装了各种接口的表格宏包，制表强烈推荐
	* threeparttable - 在表格中使用脚标，和 tabu 有冲突，补丁：https://gist.github.com/157a703e0ed8804e7696
	* diagbox - 斜线表头（作者： @刘海洋）
	* float - 提供了 H 选项，禁止浮动体浮动（除非必要，不建议这么干）
	* placeins - 提供了 \FloatBarrier 命令，限制浮动体浮动范围
6. 列表环境。
	* enumitem - 修改列表环境的各种间距、label 样式等的不二法门
7. 其他一些工具。
	* nag - 检查你是否使用了过时的宏包和命令的宏包
	* etoolbox - 主要是针对宏包和文档类开发者，不过提供了一些对环境的钩子，有时候很有用
	* xpatch - 修补命令用的
	* environ - 增强了 LaTeX 本来的 \newenvironment 的功能，解决了一些花括号不匹配导致的问题
	* fontawesome - 提供一些社交网站等网络世界常用的图标, 比如dropbox/facebook等.
1. 宏包替换
  *  biber 代替 bibtex
  * polyglossia 代替 babel
  * xindy 代替 makeindex
  * 画图用 TikZ + Asymptote 分工，代替 MetaPost、PSTricks 和 xfig等等其他所有绘图包









# 参考

7. 关于目录的页码涉及的宏包: fancyhdr, titlesec, tocloft
8. input需要指定后缀, include貌似不需要. 至少对于.tex文件如此.  
1. [生成索引(index)](https://www.texide.com/help/latex_bib_and_index_and_ref)  
9. 关于字体方面的警告(font shape之类的)的[说明](http://bbs.ctex.org/forum.php?mod=viewthread&tid=77584): 
T1/Amiri/m/n = 编码/是字族名/m代表中等粗细(不是粗体)/n代表upright(不是 italic)
10. [xindy](https://www.ctan.org/pkg/xindy)取代[makeindex](https://www.ctan.org/pkg/makeindex), 来自[zhihu邓博元](https://www.zhihu.com/question/21088362)
11. biber 取代 bibtex, polyglossia 取代 babel, xindy 取代 makeindex. [知乎邓博元](https://www.zhihu.com/question/21088362)
12. [XeLaTeX调用本地中文字体](https://lttt.blog.ustc.edu.cn/2012/09/05/%E8%BD%AC%E8%BD%BDxelatex%E8%B0%83%E7%94%A8%E6%9C%AC%E5%9C%B0%E4%B8%AD%E6%96%87%E5%AD%97%E4%BD%93.html)
13. [slashbox宏包已过时, 当前宏包是diagbox](https://github.com/wzpan/scnuthesis/commits?author=wzpan)
14. [url宏包过时, 被hyperref宏包代替, url的换行](https://liam0205.me/2017/05/17/help-the-url-command-from-hyperref-to-break-at-line-wrapping-point/)


