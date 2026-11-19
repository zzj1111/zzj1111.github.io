# zzj1111.github.io

Zijian Zhang 的个人学术主页：<https://zzj1111.github.io>

基于 [al-folio](https://github.com/alshedivat/al-folio) v1.x starter（2026-11-16 的 `main`，commit `fde4cbf`）。主题本身（布局、样式、脚本）由 `Gemfile` 里的 `al_folio_core` 等 gem 提供，这个仓库只放内容和配置。

## 改内容时改哪里

| 想改什么 | 改哪个文件 |
| --- | --- |
| 首页自我介绍、照片下方的文字 | `_pages/about.md` |
| 论文 | `_bibliography/papers.bib` |
| 首页 news | `_news/` 下每条一个 `.md` |
| CV 页（经历、教育、奖项、服务、技能） | `_data/cv.yml` |
| 邮箱、Scholar、GitHub 等图标 | `_data/socials.yml` |
| 头像 | `assets/img/prof_pic.jpg` |
| 论文左侧的会议徽章（颜色、链接） | `_data/venues.yml` |
| 合作者姓名上的主页链接 | `_data/coauthors.yml` |
| 站点标题、描述、功能开关 | `_config.yml`（改完需要重新构建才生效） |

### 加一篇论文

在 `_bibliography/papers.bib` 里加一条 BibTeX。文件里的先后顺序就是页面上同一年内的顺序。除标准字段外，常用的自定义字段：

- `abbr`：左侧徽章文字（`ICML`、`Preprint` 等，对应 `_data/venues.yml`）
- `selected = {true}`：同时显示在首页的 selected publications
- `arxiv = {2611.14515}`、`code = {...}`、`website = {...}`、`pdf = {...}`、`slides = {...}`、`poster = {...}`：生成对应按钮
- `note = {...}`：会议行下面的一行小字（例如 `Under review`），不会出现在 Bib 弹窗里
- `preview = {xxx.png}`：缩略图，图片放在 `assets/img/publication_preview/`
- 共同一作：在姓后面加 `*`（如 `Zhang*, Zijian`），并加 `annotation = {* Equal contribution}`

论文中稿后：把 `@article` 改成 `@inproceedings`，`journal` 换成 `booktitle`，改 `abbr`，删掉 `note`。

### 加一条 news

复制 `_news/` 里任意一个文件，改文件名、`date` 和正文即可。首页显示最新 8 条（`_pages/about.md` 里的 `announcements.limit`），全部在 `/news/`。

只知道月份的事件（例如某次报告）：`date` 写当月 1 号，并加一行 `month_only: true`，页面上只显示 "Feb 2026"。这个功能来自本仓库的 `_includes/news.liquid`，它覆盖了主题里的同名文件；升级主题后如果 news 显示异常，先对比这个文件。

### CV 的 PDF

PDF 放在 `assets/ZijianZhang_CV.pdf`，CV 页和首页图标栏都有入口（由 `_pages/cv.md` 和 `_data/socials.yml` 里的 `cv_pdf` 控制）。更新时用同名文件覆盖即可；注意这是公开文件，不要包含手机号、审稿分数等信息。

## 部署

推送到 `main` 后，GitHub Actions 的 **Deploy site** 会构建站点并发布到 `gh-pages` 分支（不要手动改这个分支）。仓库设置要求：

- Settings → Actions → General → Workflow permissions：**Read and write permissions**
- Settings → Pages → Source：**Deploy from a branch**，分支选 **gh-pages**

## 本地预览

```bash
docker compose pull
docker compose up
# 打开 http://localhost:8080
```

## 注意

- 不要单独改 `Gemfile`：CI 按 `Gemfile.lock` 安装依赖，两者不一致会构建失败。要升级主题请运行 `bundle update` 并一起提交 `Gemfile.lock`。
- `_config.yml` 里的 `baseurl:` 必须保留且留空。
- 更多用法见 al-folio 文档：<https://github.com/alshedivat/al-folio/blob/main/docs/CUSTOMIZE.md>

## License

主题与 starter 代码来自 al-folio，遵循 MIT License（见 `LICENSE`）。
