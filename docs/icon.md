---
layout: page
title: Icon
---

Icon 提供了 Mailcup 所用到的图标字体方案

你可以在下面的CSS文件里找到 `_icon.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##引入图标
在需要使用图标的地方直接使用，在 HTML 上添加添加 `mc-icon-{图标名称}` class。

{% example html %}
<span class="mc-icon-clip"> clip</span>
{% endexample %}

##所有可用的图标
在需要使用图标的地方直接使用

{% example html %}
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-template btn-lg"> template</span></div>
<div class="col-md-3"><span class="mc-icon-clip btn-lg"> clip</span></div>
<div class="col-md-3"><span class="mc-icon-back btn-lg"> back</span></div>
<div class="col-md-3"><span class="mc-icon-close btn-lg"> close</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-done-all btn-lg"> done-all</span></div>
<div class="col-md-3"><span class="mc-icon-done btn-lg"> done</span></div>
<div class="col-md-3"><span class="mc-icon-caret-down btn-lg"> caret-down</span></div>
<div class="col-md-3"><span class="mc-icon-arrow-down btn-lg"> arrow-down</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-focus btn-lg"> focus</span></div>
<div class="col-md-3"><span class="mc-icon-pin btn-lg"> pin</span></div>
<div class="col-md-3"><span class="mc-icon-font-color btn-lg"> font-color</span></div>
<div class="col-md-3"><span class="mc-icon-forward btn-lg"> forward</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-inbox btn-lg"> inbox</span></div>
<div class="col-md-3"><span class="mc-icon-label btn-lg"> label</span></div>
<div class="col-md-3"><span class="mc-icon-more btn-lg"> more</span></div>
<div class="col-md-3"><span class="mc-icon-clock btn-lg"> clock</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-plus btn-lg"> plus</span></div>
<div class="col-md-3"><span class="mc-icon-reply btn-lg"> reply</span></div>
<div class="col-md-3"><span class="mc-icon-reply-all btn-lg"> reply-all</span></div>
<div class="col-md-3"><span class="mc-icon-search btn-lg"> search</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-setting btn-lg"> setting</span></div>
<div class="col-md-3"><span class="mc-icon-list-text btn-lg"> list-text</span></div>
<div class="col-md-3"><span class="mc-icon-list-num btn-lg"> list-num</span></div>
<div class="col-md-3"><span class="mc-icon-text btn-lg"> text</span></div>
</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-text-bold btn-lg"> text-bold</span></div>
<div class="col-md-3"><span class="mc-icon-text-italic btn-lg"> text-italic</span></div>
<div class="col-md-3"><span class="mc-icon-text-size btn-lg"> text-size</span></div>
<div class="col-md-3"><span class="mc-icon-underline btn-lg"> underline</span></div>

</div>
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3"><span class="mc-icon-unfocus btn-lg"> unfocus</span></div>
<div class="col-md-3"><span class="mc-icon-spam btn-lg"> spam</span></div>
<div class="col-md-3"><span class="mc-icon-trash btn-lg"> trash</span></div>

</div>
{% endexample %}

##图标尺寸
图标大小分为三种

* 默认尺寸，不需要指定
* `.btn-sm` 小尺寸
* `.btn-lg` 大尺寸

{% example html %}
<span class="mc-icon-clip btn-sm"> clip</span>
<span class="mc-icon-clip"> clip</span>
<span class="mc-icon-clip btn-lg"> clip</span>
{% endexample %}

##应用实例
可以把它们应用到按钮、工具条中的按钮组、导航或输入框等地方

{% example html %}
<button type="button" class="btn btn-default btn-lg" aria-label="Left Align">
  <span class="mc-icon-pin" aria-hidden="true"> Confirm</span>
</button>

<button type="button" class="btn btn-default" aria-label="Left Align">
  <span class="mc-icon-pin" aria-hidden="true"> Confirm</span>
</button>
{% endexample %}

##颜色
可以使用Mailcup所提供的配色

{% example html %}
<span class="mc-icon-clip btn-lg" style="color:red"> clip</span>
<span class="mc-icon-clip btn-lg" style="color:blue"> clip</span>
{% endexample %}