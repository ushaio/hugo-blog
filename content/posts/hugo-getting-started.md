+++
date = '2025-01-15T10:00:00+08:00'
draft = false
title = 'Hugo静态网站生成器入门指南'
description = '详细介绍Hugo的安装、配置和基本使用方法'
tags = ['Hugo', '静态网站', '教程', 'GitHub Pages']
categories = ['HUGO']
author = 'Ushaio'
showToc = true
TocOpen = false
hidemeta = false
comments = false
disableHLJS = false
disableShare = false
searchHidden = false
+++

# Hugo静态网站生成器入门指南

Hugo是一个用Go语言编写的静态网站生成器，以其极快的构建速度和丰富的主题生态系统而闻名。

## 什么是Hugo？

Hugo是一个开源的静态网站生成器，特别适合构建：
- 个人博客
- 技术文档
- 企业网站
- 作品集网站

## 主要特点

### 1. 极速构建
- 毫秒级页面生成
- 实时热重载
- 大型网站快速构建

### 2. 零依赖
- 单一二进制文件
- 无需数据库
- 无需运行时环境

### 3. 强大的主题系统
- 丰富的主题库
- 易于自定义
- 响应式设计

## 安装Hugo

### Windows
```bash
# 使用Chocolatey
choco install hugo-extended

# 使用Scoop
scoop install hugo-extended

# 使用winget
winget install Hugo.Hugo.Extended
```

### macOS
```bash
brew install hugo
```

### Linux
```bash
# Ubuntu/Debian
sudo apt install hugo

# 或下载二进制文件
wget https://github.com/gohugoio/hugo/releases/latest
```

## 创建第一个网站

### 1. 创建新站点
```bash
hugo new site my-blog
cd my-blog
```

### 2. 添加主题
```bash
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### 3. 配置网站
编辑 `hugo.toml`：
```toml
baseURL = 'https://example.com'
languageCode = 'zh-cn'
title = '我的博客'
theme = 'PaperMod'
```

### 4. 创建文章
```bash
hugo new posts/my-first-post.md
```

### 5. 启动开发服务器
```bash
hugo server -D
```

## 内容管理

### Front Matter
每篇文章开头的元数据：
```toml
+++
title = '文章标题'
date = '2025-01-15'
tags = ['tag1', 'tag2']
categories = ['category1']
draft = false
+++
```

### 目录结构
```
content/
├── posts/          # 博客文章
├── pages/          # 静态页面
└── _index.md       # 首页内容

static/             # 静态文件
layouts/            # 自定义模板
themes/             # 主题文件
```

## 部署

### GitHub Pages
1. 创建GitHub仓库
2. 配置GitHub Actions
3. 推送代码自动部署

### Netlify
1. 连接GitHub仓库
2. 设置构建命令：`hugo`
3. 设置发布目录：`public`

## 高级特性

### 1. 短代码（Shortcodes）
```markdown
{{< youtube id="dQw4w9WgXcQ" >}}
```

### 2. 多语言支持
```toml
[languages]
  [languages.en]
    languageName = "English"
    weight = 1
  [languages.zh]
    languageName = "中文"
    weight = 2
```

### 3. 自定义CSS/JS
```toml
[params]
  custom_css = ["css/custom.css"]
  custom_js = ["js/custom.js"]
```

## 常用命令

```bash
# 创建新站点
hugo new site sitename

# 创建新文章
hugo new posts/article-name.md

# 启动开发服务器
hugo server

# 构建网站
hugo

# 查看帮助
hugo help
```

## 总结

Hugo是一个强大而灵活的静态网站生成器，适合各种规模的项目。其快速的构建速度、丰富的主题生态和简单的部署流程，使其成为现代Web开发的优秀选择。

通过本指南，你应该已经掌握了Hugo的基本使用方法。接下来可以探索更多高级特性，打造属于自己的完美网站。