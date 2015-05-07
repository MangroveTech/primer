---
layout: page
title: Label
---

Label 提供了 Mailcup 所有的Mailcup标签显示方案

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##基础label样式
* 使用label最基础的方法
* 在label的使用中，默认样式中的文字大小是10px
* `mc-label-*`的遵循了设计图设计，只有文字为10px一种

{% example html %}
<span class="mc-label">Label</span>
{% endexample %}

##Label可用变体
* 用下面的任何一个类即可改变标签的外观

{% example html %}
<span class="mc-label">Label</span>
<span class="mc-label-primary">Primary</span>
<span class="mc-label-danger">Danger</span>
<span class="mc-label-info">Info</span>
<span class="mc-label-warning">Warning</span>
<span class="mc-label-success">Success</span>
{% endexample %}

##Token
* 右侧有 close 按键

{% example html %}
<span class="mc-label" data-dismiss="alert">Shuangchun &times;</span>
{% endexample %}

* 出现在需要输入联系人的Textfield里
* 双击可变为 email 地址进行编辑
* 可选中，可拖拽交换位置(如果实现成本太高可以先不做)