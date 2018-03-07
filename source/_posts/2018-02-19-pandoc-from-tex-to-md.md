---
title: pandoc:将TEX文件转为md文件
date: 2018-02-19 21:06:48
tags: [pandoc,tex,md,maths,hexo]
categories: 工具
keywords: 
description: 为了将同一内容发布到不同的地方去, 那么就需要转换工具. 本文的目的就是利用pandoc这把刀, 将tex转为md(便于发布到hexo博客).
---

# 环境准备















# 一个例子
命令: `pandoc -s input.tex --mathjax -o output.md`  
input.tex:
```
%# -*- coding:utf-8 -*-
%!TEX program  = xelatex
\documentclass{ctexart}

\usepackage{amsmath,amssymb,amsthm}
\usepackage{enumitem}

\begin{document}
\newcommand{\me}{\mathrm{e}} 

\section{代数}
已知 $f(x)=\sum\limits_{k=1}^{2015}(|x+k|+|x-k|)$. 
若 $f(a^2-a-1)=f(2a-1)$, 则符合条件所有整数 $a$ 的和为\_\_\_\_.

\textbf{字母}: \textit{mathematics}. 加粗的汉字, 倾斜的字母.

\begin{enumerate}
\item 天南地北
\item 四面八方
\begin{itemize}
	\item 东面
	\item 南面
	\item 西面
	\item 北面
\end{itemize}
\item 江河湖海
\item 自定义的命令: $\me$.
\end{enumerate}

\newpage

\section{几何}

姐姐，今夜我在德令哈，夜色笼罩\\ 
姐姐，我今夜只有戈壁 \\

草原尽头我两手空空 \\
悲痛时握不住一颗泪滴 \\
姐姐, 今夜我在德令哈 \\
这是雨水中一座荒凉的城\\
 
除了那些路过的和居住的 \\
德令哈……今夜 \\
这是唯一的，最后的， 抒情。 \\
这是唯一的，最后的，草原。\\
 
我把石头还给石头\\
让胜利的胜利 \\
今夜青稞只属于他自己 \\
一切都在生长 \\

今夜我只有美丽的戈壁 空空 \\
姐姐，今夜我不关心人类，我只想你。\\

插图:\\
\includegraphics[scale=0.3]{a.jpg}
\end{document}
```
output.md:
```
代数
====

已知 $f(x)=\sum\limits_{k=1}^{2015}(|x+k|+|x-k|)$. 若
$f(a^2-a-1)=f(2a-1)$, 则符合条件所有整数 $a$ 的和为\_\_\_\_.

**字母**: *mathematics*. 加粗的汉字, 倾斜的字母.

1.  天南地北

2.  四面八方

    -   东面

    -   南面

    -   西面

    -   北面

3.  江河湖海

4.  自定义的命令: ${\mathrm{e}}$.

几何
====

姐姐，今夜我在德令哈，夜色笼罩\
姐姐，我今夜只有戈壁\
草原尽头我两手空空\
悲痛时握不住一颗泪滴\
姐姐, 今夜我在德令哈\
这是雨水中一座荒凉的城\
除了那些路过的和居住的\
德令哈……今夜\
这是唯一的，最后的， 抒情。\
这是唯一的，最后的，草原。\
我把石头还给石头\
让胜利的胜利\
今夜青稞只属于他自己\
一切都在生长\
今夜我只有美丽的戈壁 空空\
姐姐，今夜我不关心人类，我只想你。\
插图:\
![image](a.jpg)
```
说明: `\newpage`被忽略.  文本中的`\\`没有被正确转化, 公式中的`\\`是交给mathjax处理的. 空白的行被吞掉了. 



