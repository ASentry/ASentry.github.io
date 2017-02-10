---
layout: post
title: 创建博客
author: ASentry
header-img: "img/firstblog.jpg"
catalog: ture
---
>*如果我们过于爽快地承认失败，就可能使自己发觉不了我们非常接近于正确。*  

   
## 前言 ##

以ASentry为名的Blog终于突破了层层困难开通了。   
之前一些时候总有一些想法，去建立一个属于自己的博客。可总是遇到了一些不可预料的问题而搁置下来，而前几日php老师提出我们应建立属于自己的blog时，我便顺水推舟建立了这个略显简陋的blog。不过颇具成就感。
   
## 正文 

关于利用github+jekyll结合的方式创建Blog的方法在网上有很多，但是对于我们这种刚接触这个庞大世界的在校大学生来说它们给了我们沉痛的一击，以至于我们有可能丧失如此建立Blog的信心。因而我的第一篇博客就来以我这个菜鸟的视角告诉大家完整的建立过程。  

---
### 配置 ###
关于配置环境的问题我在此介绍Git,Ruby,python,jekyll 

--- 
### Git ###
关于Git的安装及使用[廖雪峰的教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/ "廖雪峰的教程")中有详细简介我概不赘述。  
Git的GUI与很多，个人认为比较好用的是[TortoiseGit（乌龟Git）](https://tortoisegit.org/download/ "TortoiseGit（乌龟Git）")。不过github提供的桌面客户端也是极为好用，而且功能齐全、操作也相对简单。唯一缺点国内下载github客户端速度有些缓慢。 

--- 
### Ruby、Python、jekyll ###
---
#### Ruby、Python     

Ruby的安装基本上是傻瓜式安装，只需记住在安装时勾选上Add Ruby executables to your PATH（不勾选你可能会出ruby不是内部或外部命令的错误，只需手动配置PATH即可解决），最后打开命令行输入ruby -v查看是否安装成功即可。然后就需要安装devkit，为了方便管理建议在Ruby目录下建立一个devkit文件夹将其安装在其中即可。而后在devkit文件夹内按下shift+鼠标右键选择在此处打开命令行输入ruby dk.rb init初始化创建config.yml文件（创建完成后需打开查看文末是否包含Ruby安装路径）。而后执行ruby dk.rb review和ruby dk.rb install即可。  
使用命令```gem sources```查看gem源 
在镜像源的使用上国内淘宝的镜像源已经不能够使用，而官方的镜像源不翻墙速度慢到极致。因而我们开始使用https://gem.ruby-china.org/这个镜像源。  
使用命令更换gem源         
```gem sourcrs -r https://rubygems.org/ ```     
```gem sources -a https://gem.ruby-china.org/```    
更换完成后查看显示如下结果   
![](http://i.imgur.com/Ti39cxr.jpg)    
你有可能在此遇到关于一个Error关于SSH的问题这时你需要在系统环境变量内新建一个SSH\_CERT\_FILE的变量。可以下载[这个文件](http://curl.haxx.se/ca/cacert.pem "SSH")将其复制到本地Ruby安装目录下的cacert.pem（需要新建）文件下，然后让SSH\_CERT\_FILE指向这个文件。   
使用系统命令```set SSH_CERT_FILE=cacert.pem的地址```配置路径   
报错图：    
![](http://i.imgur.com/wfX9uBI.png)  
SSH配置好后添加gem源会出现以下提示表示添加成功  
![](http://i.imgur.com/2ssIkJ0.png)    
Python[安装](https://www.python.org/downloads/ "安装")直接下一步即可，若你不使用代码高亮等一些基于Python的插件可略过此步。
     
#### jekyll     

安装jekyll执行  
```gem install jekyll```      
输入```jekyll -v```查看是否安装成功，安装成功会出现版本号  
![](http://i.imgur.com/fsjQpY5.jpg)  
然后在jekyll目录下使用命令```jekyll new MyBlog```创建博客  
![](http://i.imgur.com/g5HtNa4.jpg)    
好了至此你应该已经成功的安装了jekyll接下来你就可以在github上fork别人的库或者自己来编写自己的博客了。  
**ps:**配置好这一切你还可能遇到提示bundle等有关问题，所以你需要执行```bundle install```来解决这个问题。而后你可能会遇到类似于Error: jekyll-paginate的问题这些均可用```gem install jekyll-paginate```解决。 

---
### 后记 ###
---
第一篇博客的完成无疑是激动，在编写过程中也听取一些同学遇到的问题将其加入其中。或许这篇博客不是最完整的jekyll+github建立博客的教程，但我想很多像我一样的小白能在本文中找到启发从而把复杂而模糊的安装的过程清晰化。也欢迎大家的指正与借鉴。



 





