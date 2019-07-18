---
title: hexo博客-常见问题
comments: true
categories:
  - 技术帖
tags:
  - hexoBlog
date: 2019-07-18 00:15:05
---

## 博客在 github 访问访问慢？

> 在 coding page 上部署实现国内外分流

1. 申请 coding 账户，新建项目 同 GitHub
2. 添加 ssh key 同 GitHub
3. 修改\_config.yml

```bash
  deploy:
    type: git
    repo:
      github: <github项目地址 url>,master
      coding: <coding项目地址 url>,master
```

4. 部署

```bash
  hexo g
  hexo d
```

5. coding 控制台 开启 pages

 >菜单目录中 -> 代码 pages 服务

 ## 第三方主题 没有办法上传到自己的项目中？

 在使用第三方主题的时候，难免要对主题进行微调。但是调整后的主题文件 是无法上传上去的。这时候，你换台电脑来写博客，就还得再来一遍。【别问我，我是怎么知道的😂】

那么针对上面问题，有两个解决办法：
1. 删掉 第三方主题 的.git 
> git不能嵌套上传，最好是显示隐藏文件，检查一下有没有，否则上传的时候会出错，导致你的主题文件无法上传


## 关于博客版本管理