---
layout: page
title: Checkbox
---

Checkbox 提供了 Mailcup 所用到的复选框样式

你可以在下面的CSS文件里找到 checkbox.scss.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

### 可用 checkbox

{% example html %}
<input type="checkbox" id="mc-checkbox-green" checked/><label for="mc-checkbox-green"></label> green
<input type="checkbox" id="mc-checkbox-blue" checked/><label for="mc-checkbox-blue"></label> blue
<input type="checkbox" id="mc-checkbox-orange" checked/><label for="mc-checkbox-orange"></label> orange
{% endexample %}

### label的选择

{% example html %}
<div class="btn-group">
  <button type="button" class="mc-button-nobg dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
    <span class="mc-icon-label"></span>
  </button>
  <ul class="dropdown-menu" role="menu" id="mc-label-select">
    <li><a>Label as:</a></li>
    <li class="divider"></li>
    <li><a><input type="checkbox" id="mc-checkbox-green" checked/><label for="mc-checkbox-green"></label> green</a></li>
    <li><a><input type="checkbox" id="mc-checkbox-blue" checked/><label for="mc-checkbox-blue"></label> blue</a></li>
    <li><a><input type="checkbox" id="mc-checkbox-orange" checked/><label for="mc-checkbox-orange"></label> orange</a></li>
    <li class="divider"></li>
    <li><a class="mc-icon-plus"> &nbsp;Create new...</a></li>
  </ul>
</div>
{% endexample %}