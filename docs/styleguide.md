---
layout: page
title: styleguide
---


## 命名规则

因为 Mailcup-client 基于 BootStrap，所以有以下命名规则：

* 可以使用 BootStrap 原有样式，如 `<button class="btn btn-primary"></button>`。
* 自定义样式写法如 `mc-button-small`、`mc-avatar-big`，第一部分为 `mc`（mailcup 缩写），第二部分为组件名（与左侧列表名相同），第三部分为组件内类名。
* 所有组件（左侧列表）以一个单词概括命名，如：用 sidebar 代替 left menu，用 navbar 代替 nav bar。
* Icon font在设计和制作成webfont的命名应该遵循`mc-icon{图标名称}`，图标名称中有具体分类表示的可以命名成`mc-icon-arrow-down`、`mc-icon-list-text`、`mc-icon-text-bold`的形式，设计师在进行矢量图制作的时候应该注意对每个图标进行命名，工程制作字体实现则应遵循设计师所规定的名称.

## 注意事项

`{example html}` 之间包裹的示例 html 不能有注释 `<!-- -->`，否则会出现样式问题。
