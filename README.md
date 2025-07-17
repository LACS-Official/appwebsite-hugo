# 软件资源网站

🌐 **基于Hugo的软件资源展示网站**

这是一个使用Hugo静态网站生成器构建的软件资源展示网站，采用自定义主题设计。

## ✨ 特性

- 🎨 **现代化设计** - 响应式布局，移动端友好
- 🚀 **高性能** - 静态文件，快速加载
- 📱 **多语言支持** - 国际化配置
- 🔍 **SEO优化** - 搜索引擎友好
- 📝 **内容管理** - 支持Markdown编写

## 🏗️ 项目结构

```
hugo-website/
├── content/                 # 网站内容
│   ├── software/           # 软件资源页面
│   ├── about/              # 关于页面
│   └── contact/            # 联系页面
├── themes/                 # Hugo主题
│   └── software-resource-theme/
├── static/                 # 静态资源
├── layouts/                # 布局模板
├── config/                 # 配置文件
├── data/                   # 数据文件
├── i18n/                   # 国际化文件
└── hugo.toml              # Hugo配置
```

## 🚀 快速开始

### 1. 环境要求

- Hugo 0.100+
- Git

### 2. 本地开发

```bash
# 克隆项目
git clone <your-repo-url>
cd hugo-website

# 启动开发服务器
hugo server -D

# 访问网站
# http://localhost:1313
```

### 3. 构建网站

```bash
# 构建生产版本
hugo --minify

# 输出目录: public/
```

## 📝 内容管理

### 添加软件资源

```bash
# 创建新的软件资源页面
hugo new software/new-software.md
```

### 编辑内容

编辑 `content/software/` 目录下的Markdown文件：

```markdown
---
title: "软件名称"
description: "软件描述"
date: 2024-01-01
categories: ["分类"]
tags: ["标签"]
---

软件详细介绍内容...
```

## 🎨 主题定制

主题文件位于 `themes/software-resource-theme/`：

- `layouts/` - 页面布局模板
- `static/` - 静态资源文件
- `assets/` - 需要处理的资源文件

## 🚀 部署

### Vercel部署

```bash
# 安装Vercel CLI
npm install -g vercel

# 部署
vercel --prod
```

### Netlify部署

1. 连接GitHub仓库
2. 设置构建命令: `hugo --minify`
3. 设置发布目录: `public`

### GitHub Pages部署

```bash
# 构建网站
hugo --minify --baseURL "https://username.github.io/repo-name/"

# 推送到gh-pages分支
git subtree push --prefix public origin gh-pages
```

## 🔧 配置

### 网站配置

编辑 `hugo.toml` 文件：

```toml
baseURL = "https://your-domain.com"
languageCode = "zh-cn"
title = "软件资源网站"
theme = "software-resource-theme"

[params]
  description = "专业的软件资源展示平台"
  author = "Your Name"
```

### 多语言配置

在 `i18n/` 目录下添加语言文件：

```yaml
# i18n/zh-cn.yaml
- id: home
  translation: "首页"
- id: about
  translation: "关于我们"
```

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🤝 贡献

欢迎提交Issue和Pull Request！

---

**开始使用**: 运行 `hugo server -D` 启动本地开发服务器
