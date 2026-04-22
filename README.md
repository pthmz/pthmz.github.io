# pthmz.github.io

个人博客网站，使用 MkDocs 和 Material 主题构建，通过 GitHub Actions 自动部署到 GitHub Pages。

## 技术栈

- **静态网站生成**：[MkDocs](https://www.mkdocs.org/) 1.6.1
- **主题**：[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 9.7.6
- **依赖管理**：[uv](https://github.com/astral-sh/uv)
- **部署**：
  - [GitHub Actions](https://github.com/features/actions)（CI/CD 流程）
  - [GitHub Pages](https://pages.github.com/)（静态站点托管）

## 构建流程

1. **本地开发**：
   - 启动开发服务器：`uv run mkdocs serve`
   - 访问：`http://localhost:8000`

2. **构建静态网站**：
   - 执行：`uv run mkdocs build`
   - 输出目录：`site/`

3. **GitHub Pages 设置**：
   - 进入 GitHub 仓库 → **Settings** → **Pages**
   - **Source** 选择：`Deploy from a branch`
   - **Branch** 选择：`gh-pages`，右侧选择 `/(root)`
   - 点击 **Save**

4. **自动部署**：
   - 推送到 `main` 分支后，GitHub Actions 会自动：
     - 安装依赖
     - 构建网站
     - 部署到 `gh-pages` 分支
     - GitHub Pages 自动发布

## 目录结构

```
pthmz.github.io/
├── .github/workflows/  # GitHub Actions 工作流
├── docs/               # 文档源码
│   ├── blog/           # 博客文章
│   └── index.md        # 首页
├── overrides/          # 主题覆盖
├── site/               # 构建输出（自动生成）
├── mkdocs.yml          # MkDocs 配置
├── pyproject.toml      # 项目配置
└── uv.lock             # 依赖锁定
```

## 主要功能

- **响应式设计**：适配各种设备
- **明暗模式**：支持主题切换
- **全文搜索**：快速查找内容
- **RSS 订阅**：支持内容订阅
- **代码高亮**：美化代码显示
- **自动部署**：推代码即发布

## 快速开始

1. **克隆仓库**：
   ```bash
   git clone https://github.com/pthmz/pthmz.github.io.git
   cd pthmz.github.io
   ```

2. **安装依赖**：
   ```bash
   uv install
   ```

3. **启动开发服务器**：
   ```bash
   uv run mkdocs serve
   ```

4. **构建网站**：
   ```bash
   uv run mkdocs build
   ```

## 部署状态

[![Deploy to GitHub Pages](https://github.com/pthmz/pthmz.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/pthmz/pthmz.github.io/actions/workflows/deploy.yml)

## 访问地址

- **网站**：https://pthmz.github.io
- **仓库**：https://github.com/pthmz/pthmz.github.io
