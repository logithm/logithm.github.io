---
title: 乱七八糟
date: 2018-02-27 20:56:13
type: "backup"
---



# FAQ
1. tkc7200的集成显卡, 从[右键中去掉相应的选项](http://tieba.baidu.com/p/2993389525): `regsvr32 /u igfxdtcm.dll`. (20180316)


# temp
1. [实时监测文件的变化(livereload)](http://www.hahack.com/codes/livereload-for-hexo/)
* `$ npm install hexo-livereload --save`
* 安装livereload的[浏览器插件](http://livereload.com/extensions/)

	ps: 没成功.



1. 人生能有几回搏啊, 自己喜欢的事情是做些文字工作, 比如coding, 要是早点能发现自己的喜好并且能为之一直投入的话, 是多么幸福的事情. 2018-02-27



# 备忘录 

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



# 好玩的东西

1. [给博客加上一言经典语句](https://laod.cn/design/page/hitokoto-yiyan.html), [一言](http://hitokoto.cn/)  
F5刷新一次, 更新一次一句话.

1. [Microsoft Office 2013, 不能打开文件]()  
> 要把office的信任中心的设置修改下

1. [duckduck搜索](https://duckduckgo.com/), 
[猴油脚本: Douban Download Search（支持https）](https://greasyfork.org/zh-CN/scripts/21316-douban-download-search-%E6%94%AF%E6%8C%81https)的
代码里面有关于duckduckgo示例.

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


