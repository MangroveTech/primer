---
layout: page
title: Notification
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##种类

###Label
只有文字

###Button
文字＋按键

{% example html %}

<div style='height:200px;width:100%;background-color:#f1f1f1;'>
  <div class='mc-notification'>
    Loading...
  </div>

  <br><br><br>

  <div class='mc-notification'>
    Mark as 'CSMail' <button class='mc-button-link'>Always do this</button> <button class='mc-button-link'>Undo</button></div>
</div>

{% endexample %}

##Animation
从下方弹出，停留5秒后，从下方