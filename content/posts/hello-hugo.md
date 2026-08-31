---
title: 'Hello Hugo'
date: 2026-08-30T19:30:00+08:00
lastmod: 2026-08-30T19:30:00+08:00
draft: false
tags: ['Hugo', 'GitHub Pages']
categories: ['环境搭建']
description: '站点搭起来的第一篇占位文章，用来验证渲染链路。'
ShowToc: true
TocOpen: false
---

## 站点跑通了

这是占位正文。如果能在 `https://tuxiaolai.github.io/` 上看到这段文字，说明
「Markdown → Hugo 构建 → GitHub Actions → GitHub Pages」这条链路已经全通。

## 代码块测试

贴一段 Qt 代码验证语法高亮：

```cpp
#include <QCoreApplication>
#include <QDebug>

int main(int argc, char *argv[])
{
    QCoreApplication a(argc, argv);
    qDebug() << "Hello from Hugo + PaperMod";
    return a.exec();
}
```

再来一段命令行：

```bash
hugo new content posts/my-new-post.md
hugo server -D
git add . && git commit -m "post: 新文章" && git push
```

## 表格测试

| 环节 | 工具 |
| --- | --- |
| 写作 | Markdown |
| 构建 | Hugo 0.165.0 (extended) |
| CI | GitHub Actions |
| 托管 | GitHub Pages |

## 日常流程

1. `hugo new content posts/xxx.md` 生成新文章
2. 编辑正文，把 `draft` 改成 `false`
3. `git push`，Actions 自动构建发布
