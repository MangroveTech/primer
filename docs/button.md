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
<button class='btn btn-primary' style="margin:5px;">提交</button><button class='btn btn-default'>暂停</button><button class='btn btn-link'>取消</button>
{% endexample %}

##尺寸

* 默认尺寸，不需要指定
* `.mc-button-small` 小尺寸
* `.mc-button-big` 大尺寸

{% example html %}
<button class='btn btn-primary btn-sm'>Small button</button>
<button class='btn btn-primary'>Default button</button> 
<button class='btn btn-primary btn-lg'>Big button</button>
{% endexample %}


##种类

* `.mc-button-primary` 高优先级的按键  
* `.mc-button-standard` 普通按键 
* `.mc-button-danger` 危险按键

{% example html %}
<button class='btn btn-primary'>Primary button</button>
<button class='btn btn-default'>Default button</button>
<button class='btn btn-danger'>Danger button</button>
{% endexample %}


##状态

* `.mc-button-active` 激活状态 
* 不可用状态，添加 `disabled` 属性

{% example html %}
<button class='btn btn-default active'>Active button</button>
<button class='btn btn-primary' disabled="disabled">Disabled button</button>
{% endexample %}

##样式

* 只包含 icon
* 同时包含 文字和 icon
* 链接按键

{% example html %}
<button class='btn btn-link'>Link Button</button>
{% endexample %}
