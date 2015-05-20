---
layout: page
title: Token
---

## Token

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

{% example html %}

<link rel="stylesheet" href="../bower_components/bootstrap/dist/css/bootstrap.min.css ">
<link href="//code.jquery.com/ui/1.10.3/themes/smoothness/jquery-ui.css" type="text/css" rel="stylesheet">
<link href="../bower_components/bootstrap-tokenfield/dist/css/bootstrap-tokenfield.min.css" type="text/css" rel="stylesheet">
<link href="../bower_components/bootstrap-tokenfield/dist/css/tokenfield-typeahead.min.css" type="text/css" rel="stylesheet">
<script type="text/javascript" src="../bower_components/jquery/dist/jquery.js"></script>
<script type="text/javascript" src="../bower_components/bootstrap-tokenfield/dist/bootstrap-tokenfield.min.js"></script>
<script type="text/javascript" src="../bower_components/angular/angular.js"></script>

<div ng-app="mailcup">
  <tokenfield></tokenfield>
</div>

<script type="text/javascript">

angular.module('mailcup', [])
  .directive('tokenfield', function () {
    return {
      restrict: 'EA',
      replace: true,
      transclude: true,
      scope: false,
      template: '<input type="text" class="form-control" id="tokenfield" value="red,green,blue" />',
      controller: function ($scope) {

      },
      link: function($scope, element, attrs) {
        angular.element('#tokenfield').tokenfield({
          autocomplete: {
            source: ['red','blue','green','yellow','violet','brown','purple','black','white'],
            delay: 100
          },
          showAutocompleteOnFocus: true
        })
      }
    };
  });

</script>

{% endexample %}