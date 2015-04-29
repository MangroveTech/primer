---
layout: page
title: Typography
---

Typography 提供了 Mailcup 所用到的字体方案

你可以在下面的CSS文件里找到 `_typography.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##.pagetitle
用作页面标题，会话详情页 Subject

{% example html %}
<span class="pagetitle">Inbox</span>
{% endexample %}

##.bigtext
用作 Table Item 里面的 Sender

{% example html %}
<span class="bigtext"><strong>Gary Chai</strong>, me</span>
{% endexample %}

##.mediumtext
用作 Table Item 的 Summary, Left Menu 的 Item title
{% example html %}
<span class="mediumtext">Hey guys, please check your inbox.</span>
{% endexample %}

##.smalltext
用作 Left Menu 的 Section title
{% example html %}
<span class="smalltext">LABELS</span>
{% endexample %}