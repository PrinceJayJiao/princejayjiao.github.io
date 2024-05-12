---
title: 从零开始配置mac开发环境
date: 2024-05-13 02:42:11
tags: ['mac']
---



首先你需要安装clashx 并且选择适合你的代理，确保一些资源的访问

# 安装常用app或命令行工具
## 安装homebrew 
### 终端设置代理
由于clashx主要针对浏览器配置代理，所以我们需要手动配置终端代理

```shell
export http_proxy=http://127.0.0.1:7890
http_proxy=http://127.0.0.1:7890
all_proxy=sock5://127.0.0.1:7890
```

### 安装homebrew
这个链接是homebrew官网


