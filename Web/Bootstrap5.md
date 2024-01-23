---
title: Bootstrap
---

## 简介

Bootstrap是快速开发Web应用程序和网页的前端框架。

- 对HTML、CSS和Javascript进行了封装，便于使用
- 响应式栅格系统，适用于多种终端设备访问

## 安装

- 官网下载、CDN和包管理器（npm等）
- 将`bootstrap.min.css`加入网页头
- 将`bootstrap.bundle.min.js`在`</body>`前引入

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- 支持响应式布局 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  	<!-- 引入bootstrap -->
    <link href="/bootstrap/css/bootstrap.min.css" ref="stylesheet">
    <title>Document</title>
</head>
<body>
    <!-- content -->
    <!-- 引入js文件 -->
    <script src="/bootstrap/js/bootstrap.min.js"></script>
</body>
</html>
```

## 基础

约定：`.tag`表示可以作为class属性的内容。

### 容器

- `.container`：用于固定（最小）宽度并支持响应式布局（当viewport宽度较小时占据100%，较大时会在两边留出一定空余）的容器。
- `.container-{sm,md,lg,xl,xxl,xxxl}`：不同固定宽度的容器。
- `.container-fluid`：宽度始终为100%。

```html
<div class="container">.container</div>
<div class="container-sm">.container-sm</div>
<div class="container-md">.container-md</div>
<div class="container-lg">.container-lg</div>
<div class="container-xl">.container-xl</div>
<div class="container-xxl">.container-xxl</div>
<div class="container-fluid">.container-fluid</div>
```

### 网格

- `.col-`：所有宽度
- `.col-sm-`：viewport宽度不小于576px
- `.col-md-`：viewport宽度不小于768px
- `.col-lg-`：viewport宽度不小于992px
- `.col-xl-`：viewport宽度不小于1200px
- `.col-xxl-`：viewport宽度不小于1400px

自动按比例放大：如果你要为大于等于768px的viewport进行相同的列划分，只需要对md进行设置

```html
<!-- 所有宽度三列等分 -->
<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>
<!-- 不小于sm四列等分，小于sm四块堆叠 -->
<div class="row">
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
</div>
<!-- 不等宽列 -->
<div class="row">
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-8">.col-sm-8</div>
</div>
```

列数量限制：列数不能超过12。

### 文字排版

- 文字：默认`font-size: 1rem`和`line-height: 1.5`
  - 默认颜色`.text-body`、重要颜色`.text-primary`等
  - 不透明度`.text-black-50`
  - 背景颜色`.bg-primary`等
- 段落`<p>`：默认`margin-top: 0`和`margin-buttom: 1rem`
  - 左对齐`.text-left`
  - 居中对齐`.text-center`
  - 右对齐`.text-end`
- 标题`<h1>`\~`<h6>`（或`.h1`\~`.h6`）：自适应的`font-size`和较粗的`line-height`
  - display标题`.display-1`~`.display-6`：相较同等级标题更大的`font-size`和更细的`line-height`
  - small辅助文本`<small>`（或`.small`）：相较同等级标题较小的`font-size`
- 强调`<mark>`（或`.mark`）
- 虚下划线`<abbr>`：悬停时光标带有问号，`title`属性为悬停时的提示
- 块引用`<blockquote class="blockquote">`和`<footer class="blockquote-footer">`
- 定义列表`<dl>`与`<dt>`和`<dd>`
- 代码片段`<code>`
- 键盘文本`<kbd>`
- 多行文本`<pre>`

### 其他功能

- 表格`<table>`：大小，边框，颜色，滚动条

- 图像`<img>`：形状，对齐，自动调节大小

- 警告框`.alert`

- 按钮`.btn`：大小（全宽），轮廓，悬停，激活/不可用

- 按钮组`<div class="btn-group">`

- 徽章`<span class="badge">`

- 进度条`.progress`和`.progress-bar`：标签，颜色，条纹（动画）

- 加载器`.spinner-border`或`.spinner-grow`：可配合按钮

- 分页`.pagination`和`.page-item`

- 列表组`.list-group`和`.list-group-item`：可横向，可配合徽章

- 卡片`.card`、`.card-header`、`.card-body`和`.card-footer`

- 下拉列表`.dropdown`：可改变位置，可配合按钮组

  ```html
  <div class="dropdown">
    <button type="button" class="btn btn-primary dropdown-toggle" data-bs-toggle="dropdown">
      下拉按钮
    </button>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">链接 1</a></li>
      <li><a class="dropdown-item" href="#">链接 2</a></li>
      <li><a class="dropdown-item" href="#">链接 3</a></li>
    </ul>
  </div>
  ```

- 可折叠`.collapse`：可实现手风琴（多个可折叠项目只展开一个）

- 导航`.nav`、`nav-item`和`nav-link`

- 导航栏`.navbar`

- 轮播`.carousel`

- 弹出窗口`.modal`

- 悬停提示`data-bs-toggle="tooltip"`

- 弹出框`data-bs-toggle="popover"`

- 轻量悬浮窗`.toast`

- 根据页面位置自动更新导航列表的链接`data-bs-spy="scroll"`

- 可激活的侧边栏`offcanvas`

