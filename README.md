# FeatherZHY's Blog

这是使用 Hexo + NexT 主题搭建的个人博客。

## 分支说明

- `source` - Hexo 源文件（文章、配置、主题）
- `master` - 生成的静态网站（GitHub Pages 部署）

## 常用命令

```bash
# 本地预览
npx hexo server

# 新建文章
npx hexo new post "文章标题"

# 生成静态文件
npx hexo generate

# 部署到 GitHub Pages
npx hexo deploy

# 生成并部署
npx hexo deploy -g
```

## 目录结构

```
.
├── _config.yml          # Hexo 主配置
├── source/
│   └── _posts/          # 文章目录
├── themes/
│   └── next/            # NexT 主题
└── scaffolds/           # 文章模板
```

## 配置信息

- **主题**: NexT Mist
- **语言**: 简体中文 (zh-Hans)
- **部署地址**: https://featherzhy.github.io

## 注意事项

1. 编辑文章在 `source/_posts/` 目录
2. 修改主题配置在 `themes/next/_config.yml`
3. 每次修改后需要 `hexo deploy` 才能生效
4. 主题使用了 Git 子模块，克隆时需要 `git submodule update --init --recursive`
