---
layout: page
title: Compose
---

## 标准Compose样式
### 在放入angular项目中的时候，应该注意显示的控制最好使用angular进行控制，此处关于cc、bcc部分无法直接使用上去。

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
    <div class="mc-compose-tokenfield">
    <div class="mc-compose-tokenfield-right">
    <div style="clear:both"></div>
    
    <div class="mc-compose-tokenfield-left">
          To&nbsp;
        </div>
        <div class="mc-compose-tokenfield-item" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
        <span class="mc-cc bcc">Bcc</span>
        <span class="mc-cc cc">Cc</span>
    </div>
    </div>

    <div class="mc-compose-tokenfield cc">
    <div class="mc-compose-tokenfield-right cc">
    <div style="clear:both"></div>
       <div class="mc-compose-tokenfield-left">
       Cc&nbsp;
       </div>
       <div class="mc-compose-tokenfield-item" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
     </div>
     </div>

    <div class="mc-compose-tokenfield bcc">
     <div class="mc-compose-tokenfield-right bcc">
    <div style="clear:both"></div>
       <div class="mc-compose-tokenfield-left">
         Bcc&nbsp;
       </div>
       <div class="mc-compose-tokenfield-item" ng-app="mailcup" ng-controller="mailcupCtrl">
          <selectize config='myConfig' options='myOptions' ng-model="myModel"></selectize>
        </div>
     </div>
     </div>

    <div class='mc-compose-body'>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" />
      </div>
      <div class="mc-compose-body-content">

       <div class="mc-compose-body-editor ng-pristine ng-valid ng-touched" contenteditable="true" ng-model="content"></div>
       <div class="mc-attachemnt-container" contenteditable="false">
          <div class="mc-attachment-box ng-scope" ng-repeat="attachment in attachments">
           <button type="button" class="close" ng-click="deleteAttachment(attachment.id)">×</button>
           <span class="mc-attachment-unknow"></span>
           <div class="mc-attachment-info">
             <div class="mc-attachment-title ng-binding">Filehub.sketch</div>
             <div class="mc-attachment-size ng-binding">2.4 MB</div>
           </div>
         </div>
         <div class="mc-attachment-box ng-scope" ng-repeat="attachment in attachments">
           <button type="button" class="close" ng-click="deleteAttachment(attachment.id)">×</button>
           <span class="mc-attachment-unknow"></span>
           <div class="mc-attachment-info">
             <div class="mc-attachment-title ng-binding">Mailcup-avatar-default.png</div>
             <div class="mc-attachment-size ng-binding">1.3 kB</div>
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
    $('.mc-compose-tokenfield-right.cc').css('display', 'block');
    $('.mc-compose-tokenfield-right.cc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-tokenfield-right.cc').css('display', 'none');
        $('span.cc').css('display', 'block');
      }
    });
  });
  $('span.bcc').click(function() {
    $('span.bcc').css('display', 'none');
    $('.mc-compose-tokenfield-right.bcc').css('display', 'block');
    $('.mc-compose-tokenfield-right.bcc input').blur(function() {
      if (!$(this).val()) {
        $('.mc-compose-tokenfield-right.bcc').css('display', 'none');
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
