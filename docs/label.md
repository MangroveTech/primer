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

##Label的颜色定义
* 用下面的任何一个类即可改变标签的外观

{% example html %}
<span class="mc-label-grey">Grey</span>
<span class="mc-label-blue">Blue</span>
<span class="mc-label-red">Red</span>
<span class="mc-label-cyan">Cyan</span>
<span class="mc-label-yellow">Yellow</span>
<span class="mc-label-green">Success</span>
{% endexample %}

##Label的小方块
* 需要加一个类叫做`mc-label-box`

{% example html %}
<span class="mc-label-grey mc-label-box">&nbsp;</span>
<span class="mc-label-blue mc-label-box">&nbsp;</span>
<span class="mc-label-red mc-label-box">&nbsp;</span>
<span class="mc-label-cyan mc-label-box">&nbsp;</span>
<span class="mc-label-yellow mc-label-box">&nbsp;</span>
<span class="mc-label-green mc-label-box">&nbsp;</span>
{% endexample %}

##Token
* 结合angular和angular-selectize使用

{% example html %}

<link rel="stylesheet" href="../bower_components/selectize/dist/css/selectize.bootstrap3.css ">
<script type="text/javascript" src="../bower_components/jquery/dist/jquery.js"></script>
<script type="text/javascript" src="../bower_components/selectize/dist/js/standalone/selectize.min.js"></script>
<script type="text/javascript" src="../bower_components/angular/angular.js"></script>
<script type="text/javascript" src="../bower_components/angular-selectize2/dist/selectize.js"></script>

<div ng-app="mailcup" ng-controller="mailcupCtrl">
  <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
</div>

<script type="text/javascript">
angular.module('mailcup', ['selectize']).controller('mailcupCtrl', function($scope) {
  $scope.myModel = 1;

  $scope.myOptions = [
    {address: 'chun@mailcup.com', name: 'Spectrometer'},
    {address: 'zhao@mailcup.com', name: 'Star Chart'},
    {address: 'chai@mailcup.com', name: 'Three'},
    {address: 'gb@mailcup.com', name: 'Second'},
    {address: 'ck@mailcup.com', name: 'Four five'}
  ];

  $scope.myConfig = {
    create: true,
    valueField: 'address',
    labelField: 'name',
    delimiter: '|',
    searchField: ['name', 'address'],
    placeholder: 'Input emial address',
    onInitialize: function(selectize){
      // receives the selectize object as an argument
    },
    render: {
        item: function(item, escape) {
          // console.log('item', item)
          return '<div>' +
              (item.name ? '<span class="name">' + escape(item.name) + '</span>' : '') +
              (item.address ? '<span class="email">' + escape('<' + item.address + '>') + '</span>' : '') +
          '</div>';
        },
        option: function(item, escape) {
          var label = item.name || item.address;
          var caption = item.name ? item.address : null;
          return '<div>' +
              '<span class="name" style="color:#000">' + escape(label) + '</span>' +
              (caption ? '<span class="email" style="color:#000">' + escape('<' + caption + '>') + '</span>' : '') +
          '</div>';
        }
      },
    // maxItems: 5
  };
});
</script>

{% endexample %}



* 出现在需要输入联系人的Textfield里
* 双击可变为 email 地址进行编辑
* 可选中，可拖拽交换位置(如果实现成本太高可以先不做)