---
layout: page
title: Attachment
---

Attachment 提供了 Mailcup 所用到的附件图标方案，此处附件图标调用是使用SVG

你可以在下面的CSS文件里找到 `_attachment.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##引入图标
在需要使用图标的地方直接使用，在 HTML 上添加添加 `mc-attachment-{名称}` class。

{% example html %}
<span class="mc-attachment-ai">ai</span>
{% endexample %}

##所有可用的附件图标
在需要使用附件图标的地方直接使用

{% example html %}
<div class="row" style="margin:15px 0px 15px 0px">
<div class="col-md-3">
  <span class="mc-attachment-ai"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">ai</div>
</div>
<div class="col-md-3">
  <span class="mc-attachment-audio"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">audio</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-cal"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">cal</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-doc"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">doc</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-excl"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">excl</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-exe"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">exe</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-keynote"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">keynote</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-pdf"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">pdf</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-ppt"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">ppt</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-ps"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">ps</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-sketch"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">sketch</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-txt"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">txt</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-unknow"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">unknow</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-video"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">video</div>
</div>

<div class="col-md-3">
  <span class="mc-attachment-zip"></span>
  <div style="width:41px;text-align:center;margin:5px 0px 5px 0px">zip</div>
</div>
</div>
{% endexample %}