---
layout: post
title: "使用Jekyll和GitHub Pages搭建个人博客全过程"
date: 2024-01-15 14:30:00 +0800
categories: [技术, 教程]
tags: [Jekyll, GitHub Pages, 博客搭建, GitHub Actions]
author: wxy
excerpt: "详细记录使用Jekyll和GitHub Pages从零开始搭建个人博客的完整过程"
---

# 使用Jekyll和GitHub Pages搭建个人博客全过程

最近成功搭建了这个个人博客，使用Jekyll静态网站生成器和GitHub Pages免费托管服务。在这里记录一下完整的搭建过程，希望对想要搭建个人博客的朋友有所帮助。

## 项目概况

- **博客名称**: BlogWXY
- **技术栈**: Jekyll + GitHub Pages + GitHub Actions
- **主题**: Minima (Jekyll默认主题)
- **部署方式**: 自动化CI/CD

## 搭建步骤

### 1. 项目初始化

首先创建了项目目录结构：
```
personal-blog/
├── _config.yml          # Jekyll配置文件
├── Gemfile              # Ruby依赖管理
├── index.md             # 网站首页
├── .gitignore           # Git忽略文件
├── _posts/              # 博客文章目录
├── assets/js/main.js    # JavaScript文件
└── .github/workflows/   # GitHub Actions工作流
    └── pages.yml
```

### 2. Jekyll配置

在 `_config.yml` 中配置了博客的基本信息：
- 网站标题和描述
- 作者信息
- GitHub Pages相关设置
- 插件配置（SEO、RSS订阅等）

### 3. 依赖管理

通过 `Gemfile` 配置了所需的Ruby gems：
- Jekyll核心
- Minima主题
- 常用插件（jekyll-feed、jekyll-sitemap、jekyll-seo-tag）
- GitHub Pages兼容性

### 4. 自动化部署

配置了GitHub Actions工作流实现自动化部署：

**工作流特点**：
- 监听main分支的push事件
- 自动安装Ruby环境和依赖
- 使用Jekyll构建静态网站
- 自动部署到GitHub Pages

**关键配置**：
```yaml
- name: Build with Jekyll
  run: bundle exec jekyll build --baseurl "${{ steps.pages.outputs.base_path }}"
  env:
    JEKYLL_ENV: production
```

### 5. 内容创建

- 创建了首页介绍
- 制定了文章编写规范
- 设置了文章模板格式

## 文章编写规范

每篇文章需要遵循以下格式：

**文件命名**: `YYYY-MM-DD-文章标题.md`

**YAML前置内容**:
```yaml
---
layout: post
title: "文章标题"
date: 2024-01-15 14:30:00 +0800
categories: [分类1, 分类2]
tags: [标签1, 标签2]
author: wxy
---
```

## 部署流程

1. **本地编写文章** → 在`_posts`目录创建markdown文件
2. **Git提交推送** → `git add . && git commit -m "新文章" && git push`
3. **自动构建** → GitHub Actions自动触发构建流程
4. **自动部署** → 构建完成后自动部署到GitHub Pages
5. **访问博客** → 通过 `https://BHSF35.github.io/personal-blog` 访问

## 技术亮点

### 1. 全自动化流程
- 零手动操作的部署流程
- 代码推送即自动发布

### 2. SEO优化
- 自动生成sitemap
- 优化的页面元数据
- RSS订阅支持

### 3. 响应式设计
- Minima主题提供良好的移动端体验
- 清晰的文章排版

### 4. 版本控制
- 完整的Git版本管理
- 文章修改历史可追溯

## 遇到的问题和解决方案

### 问题1: GitHub Actions工作流配置
**问题**: 初始配置中baseurl引用错误
**解决**: 正确设置step id并引用输出

### 问题2: Jekyll配置优化
**问题**: 需要适配GitHub Pages环境
**解决**: 添加github-pages gem确保兼容性

## 后续优化计划

1. **自定义主题**: 开发个性化主题样式
2. **评论系统**: 集成Gitalk或Disqus评论
3. **搜索功能**: 添加文章搜索功能
4. **统计分析**: 集成Google Analytics
5. **CDN加速**: 优化静态资源加载速度

## 总结

通过Jekyll和GitHub Pages搭建个人博客是一个很好的选择：
- **免费**: GitHub Pages提供免费托管
- **简单**: Markdown编写，Git管理
- **专业**: 自动化部署，SEO友好
- **可扩展**: 丰富的插件生态系统

这个博客将成为我记录技术学习和生活感悟的平台。如果你也想搭建类似的博客，可以参考这个流程，或者直接fork我的仓库开始你的博客之旅！

---

*如果这篇文章对你有帮助，欢迎在GitHub上给项目点个star！*
