---
layout: page
title: Compose
---

## 标准Compose样式

{% example html %}

<link rel="stylesheet" href="../bower_components/selectize/dist/css/selectize.bootstrap3.css ">
<script type="text/javascript" src="../bower_components/jquery/dist/jquery.js"></script>
<script type="text/javascript" src="../bower_components/selectize/dist/js/standalone/selectize.min.js"></script>
<script type="text/javascript" src="../bower_components/angular/angular.js"></script>
<script type="text/javascript" src="../bower_components/angular-selectize2/dist/selectize.js"></script>

<div style='height:600px;width:100%;background-color:#f1f1f1'>
  <div class='mc-compose'>
    <div class='mc-compose-header'>
      <div class='mc-compose-title'>New message</div>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-close"></span>
      </button>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-focus"></span>
      </button>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-unfocus"></span>
      </button>
    </div>
    <div class='mc-compose-body'>
      <div class="mc-compose-body-label to">
        <div style="float:left">
          To&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
        <span class="mc-cc bcc">Bcc</span>
        <span class="mc-cc cc">Cc</span>
      </div>
      <div class="mc-compose-body-label cc">
        <div style="float:left">
        Cc&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
      </div>
      <div class="mc-compose-body-label bcc">
        <div style="float:left">
          Bcc&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
      </div>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" />
        <span class="mc-label-info">Mailcup</span>
        <span class="mc-icon-label mc-span-right"></span>
      </div>
      <div class='mc-compose-body-editor' contenteditable="true">
      </div>
    </div>
    <div class='mc-compose-footer'>
     <div class='mc-compose-footer-left'>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-clip"></span>
       </button>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-text"></span>
       </button>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-template"></span>
       </button>
     </div>
     <div class='mc-compose-footer-right'>
       <button class='mc-button-primary'>Send</button>
     </div>
   </div>
  </div>
</div>

<script type="text/javascript">
  $('span.cc').click(function() {
    $('span.cc').css('display', 'none');
    $('.mc-compose-body-label.cc').css('display', 'block');
    $('.mc-compose-body-label.cc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-body-label.cc').css('display', 'none');
        $('span.cc').css('display', 'block');
      }
    });
  });
  $('span.bcc').click(function() {
    $('span.bcc').css('display', 'none');
    $('.mc-compose-body-label.bcc').css('display', 'block');
    $('.mc-compose-body-label.bcc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-body-label.bcc').css('display', 'none');
        $('span.bcc').css('display', 'block');
      }
    });
  });

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

## 附件展示Compose样式

{% example html %}

<link rel="stylesheet" href="../bower_components/selectize/dist/css/selectize.bootstrap3.css ">
<script type="text/javascript" src="../bower_components/jquery/dist/jquery.js"></script>
<script type="text/javascript" src="../bower_components/selectize/dist/js/standalone/selectize.min.js"></script>
<script type="text/javascript" src="../bower_components/angular/angular.js"></script>
<script type="text/javascript" src="../bower_components/angular-selectize2/dist/selectize.js"></script>

<div style='height:600px;width:100%;background-color:#f1f1f1'>
  <div class='mc-compose'>
    <div class='mc-compose-header'>
      <div class='mc-compose-title'>New message</div>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-close"></span>
      </button>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-focus"></span>
      </button>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-unfocus"></span>
      </button>
    </div>
    <div class='mc-compose-body'>
      <div class="mc-compose-body-label to">
        <div style="float:left">
          To&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
        <span class="mc-cc bcc">Bcc</span>
        <span class="mc-cc cc">Cc</span>
      </div>
      <div class="mc-compose-body-label cc">
        <div style="float:left">
        Cc&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
      </div>
      <div class="mc-compose-body-label bcc">
        <div style="float:left">
          Bcc&nbsp;
        </div>
        <div class="mc-select" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
      </div>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" />
        <span class="mc-label-info">Mailcup</span>
        <span class="mc-icon-label mc-span-right"></span>
      </div>
      <div class='mc-compose-body-editor' contenteditable="true">
        <div class="mc-col-xs-6">
        <div class="alert mc-alert alert-dismissible" role="alert">
          <button type="button" class="close" data-dismiss="alert" aria-label="Close" style="right:0px;margin:5px"><span aria-hidden="true">&times;</span></button>
          <div style="float:left">
            <span class="mc-icon-template" style="font-size:46px;"></span>
          </div>
          <div style="float:left">
            <div style="font-size:12px;color:black;margin-top:8px;margin-left:5px">Report.pdf</div>
            <div style="font-size:12px;color:gery;margin-top:5px;margin-left:5px">120Kb</div>
          </div>
        </div>
        </div>
        <div class="mc-col-xs-6">
        <div class="alert mc-alert alert-dismissible" role="alert">
          <button type="button" class="close" data-dismiss="alert" aria-label="Close" style="right:0px;margin:5px"><span aria-hidden="true">&times;</span></button>
          <div style="float:left">
            <span class="mc-icon-template" style="font-size:46px;"></span>
          </div>
          <div style="float:left">
            <div style="font-size:12px;color:black;margin-top:8px;margin-left:5px">Report.pdf</div>
            <div style="font-size:12px;color:gery;margin-top:5px;margin-left:5px">120Kb</div>
          </div>
        </div>
        </div>
      </div>
    </div>
    <div class='mc-compose-footer'>
     <div class='mc-compose-footer-left'>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-clip"></span>
       </button>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-text"></span>
       </button>
       <button type="button" class="mc-button-nobg">
         <span class="mc-icon-template"></span>
       </button>
     </div>
     <div class='mc-compose-footer-right'>
       <button class='mc-button-primary'>Send</button>
     </div>
   </div>
  </div>
</div>

<script type="text/javascript">
  $('span.cc').click(function() {
    $('span.cc').css('display', 'none');
    $('.mc-compose-body-label.cc').css('display', 'block');
    $('.mc-compose-body-label.cc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-body-label.cc').css('display', 'none');
        $('span.cc').css('display', 'block');
      }
    });
  });
  $('span.bcc').click(function() {
    $('span.bcc').css('display', 'none');
    $('.mc-compose-body-label.bcc').css('display', 'block');
    $('.mc-compose-body-label.bcc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-body-label.bcc').css('display', 'none');
        $('span.bcc').css('display', 'block');
      }
    });
  });

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