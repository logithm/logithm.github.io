---
title: 函数中不应该出现复数
date: 2018-03-26 11:12:11
tags: [maths, complex number, function]
categories: 隔三差五
keywords:
mathjax: true
description: 中学的函数中, 出现复数并不是个好现象. 
---

**题目:** 已知$f(x)=\dfrac{1}{2}abx-\log_3(3^x+1)$为偶函数, $g(x)=2^x+\dfrac{a+b}{2^x}$为奇函数, 其中$a,b\in\mathbb{C}$, 
则$\sum\limits_{k=1}^{2010}(a^k+b^k)$=___.  
**答案:** 0.  
**解析:** 由$f(-1)=f(1), g(0)=0$, 易得$ab=1,a+b=-1$, 此时$f(x),g(x)$满足题意.   
而$a,b$显然是$x^2+x+1=0$的两个根,  
即$\{a,b\}=\{\omega,\bar{\omega}\}$, 其中$\omega$为1的虚根.     
故$\omega^{3k-2}+\bar{\omega}^{3k-2}=\omega^{3k-1}+\bar{\omega}^{3k-1}=-1$, $\omega^{3k}+\bar{\omega}^{3k}=2$,   
故$\sum=0$.  

**注:** 在函数中添加复数的知识, 是个不好的苗头. 中学里的函数限定在实数范围里, 要是引入复数的话, 那就过渡到复变函数了. 
为了考察复数, 也不应该这样搞啊.