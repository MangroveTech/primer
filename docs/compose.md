---
layout: page
title: Compose
---

{% example html %}
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


</script>
{% endexample %}