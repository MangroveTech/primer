---
layout: page
title: Typography
---

Typography 提供了 Mailcup 所用到的字体方案

你可以在下面的CSS文件里找到 `_typography.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##.mc-text-pagetitle
用作页面标题，会话详情页 Subject

{% example html %}
<span class="mc-text-pagetitle">Inbox</span>
{% endexample %}

##.mc-text-headline
用作 Table Item 里面的 Sender

{% example html %}
<span class="mc-text-headline"><strong>Gary Chai</strong>, me</span>
{% endexample %}

##.mc-text-content
用作 Table Item 的 Summary, Left Menu 的 Item title
{% example html %}
<span class="mc-text-content">Hey guys, please check your inbox.</span>
{% endexample %}

##.mc-text-small
用作 Left Menu 的 Section title
{% example html %}
<span class="mc-text-small">LABELS</span> <br>
<span class="mc-text-small">OTHERS</span> <br><br>

<span class="mc-text-small">标签</span> <br>
<span class="mc-text-small">其他</span> <br>
{% endexample %}