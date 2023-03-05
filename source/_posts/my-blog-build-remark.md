---
title: my-blog-build-remark
date: 2023-03-05 10:38:58
tags: ['hexo','fluid']
---
折腾了好久，终于把这个b东西搞定了，我写个简单的教程吧  
本教程只针对windows用户在 github pages 上部署hexo博客。  
我采用的主题是next主题，比较简约。  

## 安装hexo
1. 安装 node.js
推荐新手使用官方安装程序安装 链接在这里：https://nodejs.org/en/
安装时一定要勾选 add to path（如果你是新手，请一定要记住这个，否则环境变量的配置对你来讲可能不简单）
2. 安装 git
https://git-scm.com/download/win  
一般选择64-bit (除非你用32-bit的windows，讲真我还没见过)  
3. 安装hexo  
新手推荐直接使用 npm 全局安装。
```
npm install -g hexo-cli
```
## 建立博客根目录
``` shell
hexo init 'folder' 
 ```
其中'folder'为你喜欢的名字 (不用加引号)

``` shell
cd <folder>
npm install
```


## 基本配置
你可以在/根目录/_config.yml中修改你的配置  
hexo官网有非常详细的教程
https://hexo.io/zh-cn/docs/configuration 

## next主题


1. clone 主题
改为next主题的时候遇到了很大一个坑，官网给的github链接实际上是废弃版本，你需要clone的是
``` shell
git clone https://github.com/theme-next/hexo-theme-next.git themes/next
```
其他的按照官网配置即可  
官网链接 http://theme-next.iissnan.com/  
2. 修改配置  
在站点配置文件中，改为
```yml
theme: next
```

## 部署
hexo deploy 即可

{% asset_img 1.png This is an example image %}