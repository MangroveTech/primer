---
layout: page
title: Button
---

Buttons 提供了 Mailcup 所有按键方案

你可以在下面的CSS文件里找到 `button.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##排序规则

当有多个按键组时，应该按重要(偏向性)，从左至右排列

{% example html %}
<button class='mc-button-primary' style="margin:5px;">提交</button>
<button class='mc-button'>暂停</button>
<button class='mc-button-link'>取消</button>
{% endexample %}

##种类

* `.mc-button` 普通按键 
* `.mc-button-primary` 高优先级的按键  
* `.mc-button-danger` 危险按键

{% example html %}
<button class='mc-button'>Default button</button>
<button class='mc-button-primary'>Primary button</button>
<button class='mc-button-danger'>Danger button</button>
{% endexample %}


##尺寸

* 默认尺寸，不需要指定
* `.mc-button-small` 小尺寸
* `.mc-button-big` 大尺寸

{% example html %}
<button class='mc-button-primary mc-button-small'>Small button</button>
<button class='mc-button-primary'>Default button</button> 
<button class='mc-button-primary mc-button-big'>Big button</button>
{% endexample %}


##状态

* 激活状态，添加 `active` 类
* 不可用状态，添加 `disabled` 属性

{% example html %}
<button class='mc-button active'>Active button</button>
<button class='mc-button-primary' disabled="disabled">Disabled button</button>
{% endexample %}

##样式

* 只包含 icon
* 同时包含 文字和 icon
* 链接按键

{% example html %}
<button class='mc-button-link'>Link Button</button>
{% endexample %}
