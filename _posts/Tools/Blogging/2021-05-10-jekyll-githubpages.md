---
title: 搭建个人博客：Jekyll + Github Pages + VSCode
author: zjpzhao
date: 2021-05-10 16:13:00 +0800
categories: [Tools]
tags: [Jekyll,Blog,TODO]

---

## 本地编译
在本地根目录执行`$ bundle exec jekyll s`然后在浏览器中查看<http://localhost:4000/>  
其他命令行用法参照<https://www.jekyll.com.cn/docs/usage/>

---

## 网页自动生成目录
jekyll自动识别二级标题，并生成博客右侧的目录content（注意只能是二级标题！）

---

## 粘贴图片工具-VSCode插件*Paste Image*
<br>

![](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-24-47.png){: width="80%"}
_按照配置样例修改settings.json_

<br>

在*settings.json*中加入
```json
"pasteImage.showFilePathConfirmInputBox": true,
"pasteImage.path": "${projectRoot}/assets/img/${currentFileNameWithoutExt}",
"pasteImage.basePath": "${projectRoot}",
"pasteImage.forceUnixStyleSeparator": true,
"pasteImage.prefix": "/"
```
（以上代码参照vscode插件Extension: *Paste Image*下载处教程）
效果如下：

<br>

![保存路径预览](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-24-17.png){: width="80%"}
_保存路径预览_

<br>

![保存和生成链接代码](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-24-34.png){: width="80%"}
_保存和生成链接代码_

<br>

注意，直接复制图片**文件**然后粘贴是不行的，会在右下角报错：
![](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-26-14.png){: width="50%"}
_报错不识别_

<br>

ERROR原因是:直接复制文件不会进入剪贴板（推测与文件操作用的不是一套剪贴板）  
解决方法是:打开这张图片然后复制到剪贴板

![](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-27-49.png){: width="50%"}
_在图片浏览器中复制到剪贴板_

![](/assets/img/2021-05-10-jekyll-githubpages/2021-05-10-16-40-12.png){: width="50%"}
_成功复制到剪贴板_

<br>
---
