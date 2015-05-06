---
layout: page
title: Token
---

## 测试

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

{% example html %}

<link rel="stylesheet" href="../bower_components/selectize/dist/css/selectize.default.css ">
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
    {id: 1, title: 'Spectrometer'},
    {id: 2, title: 'Star Chart'},
    {id: 3, title: 'Laser Pointer'}
  ];

  $scope.myConfig = {
    create: true,
    valueField: 'id',
    labelField: 'title',
    delimiter: '|',
    placeholder: 'Pick something',
    onInitialize: function(selectize){
      // receives the selectize object as an argument
    },
    // maxItems: 1
  };
});
</script>

{% endexample %}