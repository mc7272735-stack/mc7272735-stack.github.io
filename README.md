# Academic homepage template

这是一个纯 HTML + CSS 的学术个人主页模板，不需要安装框架，也不需要运行构建命令。

## 文件结构

```text
academic-homepage-template/
├── index.html
├── style.css
├── publications/
│   └── index.html
├── exploratory-research/
│   └── index.html
├── academic-activities/
│   └── index.html
├── album/
│   └── index.html
└── assets/
    └── profile-placeholder.svg
```

## 页面结构

主页在简历链接之后依次为：

1. Education
2. Preprints & Publications
3. Exploratory Research
4. Academic Activities
5. Teaching

Album 不在学术内容容器中，而是在页面最下方用一个紧凑入口单独呈现。

## 快速使用

1. 用 VS Code 打开整个文件夹。
2. 在 `index.html` 中搜索 `EDIT`，依次替换姓名、简介、邮箱、教育、精选论文、探索性研究、学术活动和教学信息。
3. 把个人照片放到 `assets`，修改 `profile-photo` 的 `src`。
4. 把简历命名为 `cv.pdf` 并放到 `assets`。
5. 分别编辑三个学术子页面中的完整列表。
6. 双击根目录的 `index.html` 即可预览。

## 首页精选条目

`Preprints & Publications` 和 `Exploratory Research` 都使用：

```html
<div class="showcase-list">
  <article class="showcase-item">
    ...
  </article>
</div>
```

在 `showcase-list` 中保留 1–5 个 `showcase-item` 即可；CSS 会自动适应条目数量和文字长度。Academic Activities 的三个子模块也使用相同结构。

## 论文完整列表

`publications/index.html` 不是表格。每篇论文使用一个 `collection-item`，可放置：

- 状态与年份
- 标题
- 作者
- 一至两句话描述
- arXiv、PDF、期刊或项目页面链接

## Album 照片排版

`album/index.html` 使用 12 列自适应网格。给 `photo-card` 添加一种尺寸类：

- `photo-card-wide`：整行大图
- `photo-card-landscape`：横图
- `photo-card-portrait`：竖图
- `photo-card-square`：方图

平板会自动变为两列，手机会自动变为单列；照片统一使用 `object-fit: cover`，不需要手动裁成完全相同的尺寸。

## 风格说明

模板保持纯白背景、灰黑文字和细分隔线，没有渐变、阴影或装饰性背景。个人照片宽度通过 `clamp()` 和媒体查询自适应。
