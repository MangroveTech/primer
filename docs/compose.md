---
layout: page
title: Compose
---

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
        To&nbsp;
        <input />
        <span class="bcc">Bcc</span>
        <span class="cc">Cc</span>
      </div>
      <div class="mc-compose-body-label cc">
        Cc&nbsp;
        <input />
      </div>
      <div class="mc-compose-body-label bcc">
        Bcc&nbsp;
        <input />
      </div>
      <div class="mc-compose-body-label">
        <input placeholder="Subject" /><span class="mc-label-info">Label</span>
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
    {id: 1, title: 'Spectrometer'},
    {id: 2, title: 'Star Chart'},
    {id: 3, title: 'Three'},
    {id: 4, title: 'Second'},
    {id: 5, title: 'Four five'}
  ];

  $scope.myConfig = {
    create: true,
    valueField: 'id',
    labelField: 'title',
    delimiter: '|',
    placeholder: 'Input emial address',
    onInitialize: function(selectize){
      // receives the selectize object as an argument
    },
    // maxItems: 5
  };
});

</script>
{% endexample %}