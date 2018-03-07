---
title: 函数单调性应用的一个例子
date: 2018-02-19 22:31:49
tags: [maths,函数, 单调性]
categories: [隔三差五]
keywords:
description: 这道题目是来自于那本题典. 所录两种解法皆不同于标答, 且都来自于学生.
mathjax: true
---

**问题: ** 单调函数$y=f(x)(x>0)$使得$y=f(a^x)-x$在$\mathbb{R}$上单调递增, $y=f(b^x)-x$
在$\mathbb{R}$上单调递减, 且$a,b>1$. 求证: $b<a$.  
**解法一: ** 
因为$f(a^x)=f(a^x)-x+x$, 所以$y=f(a^x)$单调递增, 则$y=f(x)=f(a^{\log_ax})$单调递增.  
因为$f(a^x)-f(b^x)=(f(a^x)-x)-(f(b^x)-x)$, 所以$y=f(a^x)-f(b^x)$单调递增.  
又$x=0$时, $f(a^x)-f(b^x)=0$, 则$x>0$时, $f(a^x)-f(b^x)>0$.  
故当$x>0$时, $a^x>b^x$. 又$a,b>1$, 则$a>b$.   

**解法二: **
(反证法) 显然$a\neq b$, 假设$b>a$, 则$\log_ab>1$且$0<\log_ba<1$.   
由单调性有$f(a^1)-1<f(a^{\log_ab})-\log_ab$, $f(b^1)-1<f(b^{\log_ba})-\log_ba$.  
那么$f(a)-1+\log_ab<f(b)<f(a)+1-\log_ba$, 则$\log_ab+\log_ba<2$.  
而这显然是不成立, 故假设不成立, 所以$b<a$. 

