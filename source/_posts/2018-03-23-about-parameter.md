---
title: 关于参数讨论的一道小题
date: 2018-03-23 14:58:04
tags: [maths, 参数]
categories: 隔三差五
keywords:
mathjax: true
description: 
---

**题目** 已知函数$f(x)=2mx^2+2(m-4)x+1, g(x)=mx$, 若对于任意实数$x$, $f(x)$与$g(x)$至少有一个为正数, 则实数$m$的取值范围是___.  

**答案**: $(0,8)$.

**分析**: $f(x)=2m(x^2+x)-8x+1$, 过$(0,1)$与$(-1,9)$. 可惜没什么用.  

1. 当$m=0$时, 不符合题意;   
1. 当$m<0$时, $f(\pm\infty)<0, g(+\infty)<0$, 不符合题意.   
1. 当$m>0$时, 等价于对任意$x\leqslant0$, $f(x)>0$恒成立.  
当$m>0, x\leqslant0$时, $f(x)>0\iff 2m(x^2+x)>8x-1\iff \dfrac{x^2+x}{8x-1}<\dfrac{1}{2m}$.  
令$t=8x-1\in(-\infty,-1]$, 则$\dfrac{x^2+x}{8x-1}=\dfrac{1}{64}\left(t+\dfrac{9}{t}+10\right)\leqslant\dfrac{4}{64}$ (当且仅当 $x=-\dfrac{1}{4}$时等号成立).  
易得$0<m<8$.  

**注**: 其中分离参数的方法是个trick.  qed. 


