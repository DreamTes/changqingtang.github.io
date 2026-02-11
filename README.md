# Changqing Tang Academic Homepage

这是一个基于 **Jekyll + GitHub Pages** 的学术主页仓库，用于展示个人简介、论文、报告、教学与博客内容。

## 在线预览与发布

本仓库可以直接依赖 GitHub Pages 自动构建，无需本地环境即可预览更新。

1. 代码推送到 `main` 分支。
2. 在 GitHub 仓库 `Settings -> Pages` 中确认发布来源为当前仓库分支。
3. 发布地址通常为：
   - 用户主页仓库：`https://dreamtes.github.io/`
   - 项目仓库：`https://dreamtes.github.io/changqingtang.github.io/`

## 目录结构

- `_config.yml`：站点全局配置（站点标题、作者信息、社交链接等）
- `_data/navigation.yml`：顶部导航菜单
- `_pages/`：About、CV、Guide 等独立页面
- `_publications/`：论文条目（每篇一个 Markdown 文件）
- `_talks/`：报告/演讲条目
- `_teaching/`：教学条目
- `_posts/`：博客文章
- `files/`：PDF、附件等下载文件
- `images/`：图片资源
- `assets/`、`_sass/`：前端样式与脚本

## 首次配置（必做）

编辑 `_config.yml`，至少修改以下字段：
- `title`、`name`、`description`
- `url`（你的站点 URL）
- `repository`（`DreamTes/changqingtang.github.io`）
- `author` 下的头像、机构、邮箱、学术链接

编辑 `_pages/about.md`，替换模板默认介绍为你的个人简介。

## 内容更新示例

- 新增论文：在 `_publications/` 新建 `YYYY-MM-DD-title.md`
- 新增报告：在 `_talks/` 新建 `YYYY-MM-DD-title.md`
- 上传论文 PDF：放到 `files/`，在条目里用 `paperurl` 引用
- 调整导航：修改 `_data/navigation.yml`

## 本地预览（可选）

如果你之后需要更快调样式，可本地运行：

```bash
bundle install
npm install
bundle exec jekyll serve -l -H localhost
```

访问 `http://localhost:4000`。

## 常见问题

### `Scrape Talk Locations / build (push)` 失败

当前仓库包含 `.github/workflows/scrape_talks.yml`，该工作流会执行 `talkmap.ipynb`。若仓库中不存在该 notebook，会快速失败。

可选处理：
- 不使用 talk 地图功能：删除该 workflow 文件；
- 使用该功能：补充 `talkmap.ipynb` 并确保依赖可安装。
