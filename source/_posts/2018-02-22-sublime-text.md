---
title: Sublime Text 3 笔记
date: 2018-02-22 08:53:33
tags: [sublime, package, updating]
categories: 工具
keywords:
description: sublime text 3是个轻量级的文本工具, 功能强大在插件上.
---


插件(plugins), snippets, 宏(macros).

# 基本情况

## 安装与破解

* [官网](https://www.sublimetext.com/3)下载,当前版本3143, 然后输入[注册码](http://www.jianshu.com/p/04e1b65dd2c0). 
貌似版本不一致也没关系, 至少还没报错.
* [安装本地的package control](https://packagecontrol.io/installation): 调出控制台, copy, paste. 

## settings

* 当前配置都是在 `menu->preferences->setting-user` 下进行修改的. 这样的话就不影响全局的设置.
```
    // 当前行高亮
    "highlight_line": true,

    // 窗口失焦立即保存文件
    "save_on_focus_lost": true,    

    // 关闭自动更新
    "update_check": false,
```


# 快捷键
* 调出控制台(console), 即底部的命令行: Ctrl+\`. 其中\`与~是同一个键, 即左单引号.
* 打开悬浮对话框(command palette): ctrl+shift+p.
* ctrl+shift+l: 多行编辑

* 这里设置按Ctrl+Shift+C复制文件路径，按F2即可在Chrome浏览器预览效果(如果需要的话，也可以根据自己的需要为Firefox，Safari，IE，Opera等加上)，
当然你也可以自己定义喜欢的快捷键，最后注意代码中的浏览器路径要以自己电脑里的文件路径为准。  
```
	[   
	{ "keys": ["ctrl+shift+c"], "command": "copy_path" },
	//chrome
	{ "keys": ["f2"], "command": "side_bar_files_open_with",
	        "args": {
	            "paths": [],
	            "application": "C:\\Users\\jeffj\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe",
	            "extensions":".*"
	        }
	}
	]
```

* [跳出括号](https://ruby-china.org/topics/4824)



## 文档编辑快捷键
* C+M: 快速移动光标到括号开始或结束

* 一些参考
1. [如何优雅地使用 Sublime Text 3](http://www.imooc.com/article/3810)
2. [Sublime Text 3快捷键汇总](http://blog.csdn.net/article/details?id=31791881)










# 插件
## 基础
1. 插件管理 [package control](https://packagecontrol.io/installation) 的安装: 其实就是把相应的代码copy到控制台(console)中, 然后回车等待
安装结束, 重启即可.
2. 至于某插件到底做什么用, 看[插件官网](https://packagecontrol.io/)是最简单的. 
3. 插件的安装方法: 
	* 已经安装package control的前提下, c+s+p调出悬浮对话框, 找到package install, 再找到想要的插件, 回车即可.
	* 下载完整的插件包, 解压, 放入`%APPDATA%\Sublime Text 3\Packages` ,  
	即 `C:\Users\yao\AppData\Roaming\Sublime Text 3\Packages`．

##  通用插件: 
1. converttoutf8: 将非utf8的编码转为utf8编码.
2. BracketHighlighter: 高亮显示匹配的括号、引号和标签.
3. [SideBarEnhancements](http://www.jeffjade.com/2015/12/15/2015-04-17-toss-sublime-text/): 更强大的是，该插件还能让我们自定义快捷
键呼出某个浏览器以预览页面！


## 个性化插件

1. color theme
	*  语法高亮其实就是一个color theme, 这个东西可以自己写, 放入(C:\Users\yao\AppData\Roaming\Sublime Text 3\Packages\User), 比如这
个目录下的[Monokai-custom.tmTheme](http://riny.net/2013/sublime-markdown/) 就是个例子, 但是这个theme有问题. 
	*  各个color theme所支持的语言集合不一致, 至于需要某theme支持某语言, 这个应该可以在menu->preferences->settings-user中设定.

2. [git](http://jinfang.life/posts/4fb342fc/)


## 在sublime3中使用latex

1. 最最重要的是pdflatex中的编码问题, 看来要把所有tex文件都转换为utf8(不带bom)了, 否则即使有convert2utf8宏包仍然会一不注意就乱码了.

1. [LaTeXing](https://packagecontrol.io/packages/LaTeXing) 貌似功能强大.

2. 竟然有[TikZ](https://packagecontrol.io/packages/TikZ). 
   [例子1](http://dz.sdut.edu.cn/blog/subaochen/2016/02/sublime-text-3%E7%9A%84%E4%B8%80%E4%BA%9B%E4%BD%BF%E7%94%A8%E7%BB%8F%E9%AA%8C/),
   [例子2](http://docs.latexing.com/stable/tutorials/tikz-with-latexing.html),

3. [LaTeXtools](https://packagecontrol.io/packages/LaTeXTools) 看起来比[LaTeXing](https://packagecontrol.io/packages/LaTeXing)强大.

4. [geogebra可以导出tikz](https://www.geogebra.org/)

5. [easy-todo宏包](https://www.ctan.org/tex-archive/macros/latex/contrib/easy-todo)

6. [todonotes宏包](https://www.ctan.org/pkg/todonotes)

6. [diagxy宏包](https://www.ctan.org/pkg/diagxy): 图论.

7. [multido宏包](https://www.ctan.org/pkg/multido): 在某处重复/有规律地输入内容.  `\multido{\i=2+-3}{10}{\i, }`

8. [pstricks下有很多实现不同功能的子宏包](https://www.ctan.org/tex-archive/graphics/pstricks/contrib/)

1. [LaTeXTools 插件教程](http://blog.yuelong.info/post/st-latextools-readme-1.html)
2. [订制 Sublime Text 下 LaTeXTools 插件的编译脚本](http://liam0205.me/tags/LaTeXTools/ "LaTeXTools编译命令重新")
3. [LaTeXTools 各种编译器的重新设置](http://liam0205.me/2014/12/14/advanced-builder-latextools/)  这篇文档非常重要. 然而并没有什么鸟用.
1. [关于Sumatra的反向搜索设置](http://isunnydays.lofter.com/post/260ea5_8b9a2a)   

> 打开SumetraPDF选项，修改命令行为："D:\pg\Sublime Text 3\sublime_text.exe" "%f:%l" 
> 或者"C:\Program Files\Sublime Text 3\sublime_text.exe" "%f:%l" 
> 注意路径按照自己的安装的盘符进行对应修改；
> window下用ctex一般SumetraPDF是和WinEdt关联的，其原始命令为："D:\CTEX\WinEdt\WinEdt.exe" "[Open(|%f|);SelPar(%l,8);]"
> 如果有一天想改回去，可用使用这个恢复和WinEdt的反向搜索。  

1. [LaTeX-cwl](https://github.com/LaTeXing/LaTeX-cwl) 用于代码补齐, 需要和latexing配合使用. 离线安装比较好, 然后修改latex-cwl中的各个文件.
	latex-cwl 文件夹中很多cwl文件对我来说并没有用, 直接删除, 甚至可以自己写一个需要的代码补全与提示列表, 只用后缀是cwl, 内容是类似的列表即可.
6. 神奇的latexing. 若disabled latexing宏包, 会导致latextools的C-S-B快捷键对应的编译命令失效.

# 参考
1. [Sublime Text 3 全程详细图文原创教程](http://www.cnblogs.com/wind128/p/4409422.html). 
ps: 该文有相当多的newbie信息.
2. [Sublime Text 3 配置和使用方法](https://www.zybuluo.com/king/note/47271)

