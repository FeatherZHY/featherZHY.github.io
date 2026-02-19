# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Hexo blog source repository** for FeatherZHY's personal blog, deployed on GitHub Pages.

**Branch Structure:**
- `source` - Hexo source files (Markdown posts, configs, themes)
- `master` - Generated static site (deployed to GitHub Pages)

## Technology Stack

- **Generator**: Hexo
- **Theme**: NexT (Mist scheme)
- **Language**: Simplified Chinese (zh-Hans)
- **Deployment**: GitHub Pages via hexo-deployer-git

## Common Commands

```bash
# Start local development server
npx hexo server

# Create a new post
npx hexo new post "文章标题"

# Generate static files
npx hexo generate

# Deploy to GitHub Pages (generates + deploys)
npx hexo deploy

# Generate and deploy in one command
npx hexo deploy -g
```

## Architecture

### Directory Structure
- `source/_posts/` - Blog posts in Markdown format
- `themes/next/` - NexT theme files (Git submodule)
- `scaffolds/` - Templates for new posts
- `public/` - Generated static output (gitignored, created on deploy)
- `_config.yml` - Hexo main configuration
- `themes/next/_config.yml` - Theme configuration

### URL Structure
Posts follow: `/{year}/{month}/{day}/{post-title}/`

### Front-matter Format
```yaml
---
title: 文章标题
date: 2026-02-20 07:44:10
categories: 分类名
tags:
  - 标签1
  - 标签2
---
```

## Deployment

The blog uses `hexo-deployer-git` to deploy. Configuration in `_config.yml`:
```yaml
deploy:
  type: git
  repo: https://github.com/FeatherZHY/featherZHY.github.io.git
  branch: master
```

**Important:** The `master` branch is overwritten on each deploy. Never edit `master` directly.

## Theme Configuration

The blog uses NexT with Mist scheme. Key settings:
- Scheme: Mist (in `themes/next/_config.yml`)
- Language: zh-Hans (in `_config.yml`)
- No custom domain configured

## Working with This Repository

1. Always work on the `source` branch
2. Run `npx hexo server` to preview locally
3. Commit source changes: `git add -A && git commit -m "..."`
4. Push source: `git push origin source`
5. Deploy: `npx hexo deploy`
