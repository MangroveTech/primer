---
layout: page
title: Token
---

## Token

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

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

  $scope.dbclick = function() {
    console.log('DBCLICK');
  };

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
              (item.name ? '<span class="name" ng-click="dbclick()">' + escape(item.name) + '</span>' : '')
              + '</div>';
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