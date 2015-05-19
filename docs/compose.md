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
        <input />
      </div>
      <div class="mc-compose-body-label bcc">
        <div style="float:left">
          Bcc&nbsp;
        </div>
        <input />
      </div>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" />
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
    placeholder: '',
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
        <input />
      </div>
      <div class="mc-compose-body-label bcc">
        <div style="float:left">
          Bcc&nbsp;
        </div>
        <input />
      </div>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" />
        <span class="mc-label-info">Mailcup</span>
        <span class="mc-icon-label mc-span-right"></span>
      </div>
      <div class='mc-compose-body-editor' contenteditable="true">
      </div>
      <div class="mc-compose-body-editor">
      <div class="mc-col-xs-6 alert alert-dismissible">
        <div class="alert mc-alert alert-dismissible">
          <button type="button" role="alert" data-dismiss="alert" aria-label="Close" class="close mc-alert-close"><span aria-hidden="true">&times;</span></button>
          <div class="mc-alert-text">
            <span class="mc-attachment-doc"></span>
          </div>
          <div class="mc-alert-text">
            <div class="mc-alert-title">Report.pdf</div>
            <div class="mc-alert-filesize">120Kb</div>
          </div>
        </div>
        </div>
        <div class="mc-col-xs-6 alert alert-dismissible">
        <div class="mc-alert">
          <button type="button" role="alert" data-dismiss="alert" aria-label="Close" class="close mc-alert-close"><span aria-hidden="true">&times;</span></button>
          <div class="mc-alert-text">
            <span class="mc-attachment-doc"></span>
          </div>
          <div class="mc-alert-text">
            <div class="mc-alert-title">Report.pdf</div>
            <div class="mc-alert-filesize">120Kb</div>
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
    placeholder: '',
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