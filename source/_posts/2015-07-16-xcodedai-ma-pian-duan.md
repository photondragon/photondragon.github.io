---
layout: post
title: "Xcode代码片段Snippets"
date: 2015-07-16 22:53:21 +0800
comments: true
categories: 实用技巧
---

代码片段Snippets主要用于加速代码的输入速度。通过把常用的代码设置为Snippet，并分配一个简短的快捷字符串，你只需要输入这个快捷字符串，再按下tab键，xcode就会自动帮你输入预设的代码段。

<!--more-->

#创建代码段

选中一段代码，然后拖到右下角的Code Snippet Library窗口中，将创建一个自定义代码块。滚动列表到最下面，你将看到刚刚新建的代码片段，如下图

![snippets-1](/images/post/2015-07-16-xcodedai-ma-pian-duan/snippets-1.jpg)

双击刚刚新建的代码片段"My Code Snippet"，在弹出窗口中点"Edit"按钮

![snippets-2](/images/post/2015-07-16-xcodedai-ma-pian-duan/snippets-2.jpg)

然后分别输入  
1. 代码片段的名称，比如：Table View Sections  
2. 代码片段的快捷键，比如：tablesections  
3. 占位符，比如：<#number of section#>  

![snippets-3](/images/post/2015-07-16-xcodedai-ma-pian-duan/snippets-3.jpg)

然后在@implementation~@end块中输入tablesections，将弹出代码片段提示框，选中你想要的代码片段，按回车

![snippets-4](/images/post/2015-07-16-xcodedai-ma-pian-duan/snippets-4.jpg)

#保存代码片段到github

Xcode代码段默认保存在`~/Library/Developer/Xcode/UserData/CodeSnippets`目录下  
首先登录github网站，新建一个代码仓库，比如我的代码仓库地址为https://github.com/photondragon/xcodesnippets  
然后打开终端，输入如下指令：

```
cd ~/Library/Developer/Xcode/UserData/CodeSnippets
git init
git remote add origin git@github.com:photondragon/xcodesnippets.git
git push origin master
```

#将代码片段部署到新机器上

打开终端，输入：

```
mkdir -p ~/Library/Developer/Xcode/UserData/CodeSnippets
cd ~/Library/Developer/Xcode/UserData/CodeSnippets
git init
git remote add origin https://github.com/photondragon/xcodesnippets.git
git pull origin master
```