---
layout: page
title: Dropdown
---

Dropdown 提供了 Mailcup 所有下拉/上拉菜单样式

你可以在下面的CSS文件里找到 `dropdown.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##方向

* 默认为下拉菜单
* `mc-dropdown-up` 上拉菜单

{% example html %}
<div class="btn-group">
  <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
    Dropdown <span class="caret"></span>
  </button>
  <ul class="dropdown-menu" role="menu">
    <li><a href="#">转发全部</a></li>
    <li><a href="#">打印全文</a></li>
    <li class="divider"></li>
    <li><a href="#">删除会话</a></li>
  </ul>
</div>

<div class="btn-group dropup">
  <button type="button" class="btn btn-link dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
    Dropup
  </button>
  <ul class="dropdown-menu" role="menu">
    <li><a href="#">Settings</a></li>
    <li><a href="#">Domain Manger</a></li>
    <li class="divider"></li>
    <li><a href="#">Sign out</a></li>
  </ul>
</div>

{% endexample %}

##类型

###菜单

###Auto Complate
Token Field, 搜索结果

###Labels Selector

{% example html %}
<div class="btn-group">
  <button class='mc-button-nobg dropdown-toggle' data-toggle="dropdown" aria-expanded="false"><span class='mc-icon-done'></span></button>
  </button>
  <ul class="dropdown-menu" role="menu">
    <li><a>Label as:</a></li>
    <li class="divider"></li>
    <li><a href="#"><input type="checkbox" id="mc-checkbox-green" checked/><label for="mc-checkbox-green"></label> Team</a></li>
    <li><a href="#"><input type="checkbox" id="mc-checkbox-blue" checked/><label for="mc-checkbox-blue"></label> Support</a></li>
    <li><a href="#"><input type="checkbox" id="mc-checkbox-orange" checked/><label for="mc-checkbox-orange"></label> Hiring</a></li>
    <li class="divider"></li>
    <li><a href="#">Create new...</a></li>
  </ul>
</div>
{% endexample %}
