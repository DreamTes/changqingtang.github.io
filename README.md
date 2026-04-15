# DreamTes Academic Homepage

这是一个基于 **Jekyll + GitHub Pages** 的精简学术主页仓库，当前仅保留论文展示与博客功能。

## 在线地址

- 主页：`https://dreamtes.github.io/`

## 当前结构

- `_config.yml`：站点全局配置（标题、作者信息、社交链接）
- `_data/navigation.yml`：顶部导航（Publications / Blog Posts）
- `_pages/`：页面入口（首页、论文汇总、博客归档、404、sitemap）
- `_publications/`：论文条目（每篇一个 Markdown 文件）
- `_posts/`：博客文章
- `_includes/`、`_layouts/`、`_sass/`、`assets/`：主题模板与样式脚本
- `files/`：附件下载（PDF、补充材料等）
- `images/`：头像、favicon 等图片资源

## 内容维护

- 新增论文：在 `_publications/` 新建 `YYYY-MM-DD-title.md`
- 新增博客：在 `_posts/` 新建 `YYYY-MM-DD-title.md`
- 上传附件：放入 `files/`，在对应 Markdown 里引用链接
- 调整菜单：编辑 `_data/navigation.yml`

## 基础配置

请先修改 `_config.yml` 中的占位信息：
- `title`、`name`、`description`
- `author`（姓名、机构、邮箱、学术链接）

## 本地预览（可选）

```bash
bundle install
npm install
bundle exec jekyll serve -l -H localhost
```

访问 `http://localhost:4000`。

## 发布方式

推送到 `main` 分支后，GitHub Pages 会自动构建并发布。
】


x x x x x x x x s
