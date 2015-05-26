---
layout: page
title: Notification
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##种类

###Label
只有文字

###Button
文字＋按键

{% example html %}

<div style='height:200px;width:100%;background-color:#f1f1f1;'>
  <div class='mc-notification'>
    Loading...
  </div>

  <br><br><br>

  <div class='mc-notification'>
    Mark as 'CSMail' <button class='mc-button-link'>Always do this</button> <button class='mc-button-link'>Undo</button></div>
</div>

{% endexample %}

##Animation
从下方弹出，停留5秒后，从下方

{% example html %}
<script type="text/javascript" src="../bower_components/jquery/dist/jquery.js"></script>
<script type="text/javascript" src="../bower_components/toastr/toastr.min.js"></script>

<button class="btn btn-danger" href="click" id="showToastr">Click</button>

<script type="text/javascript">
  // toastr.options = {
  //   "closeButton": false,
  //   "debug": false,
  //   "toastClass": '',
  //   "positionClass": "toast-bottom-center",
  //   // "messageClass": 'mc-notification-center',
  //   "containerId": null,
  //   "onclick": null,
  //   "showDuration": "300",
  //   "hideDuration": "1000",
  //   "timeOut": "5000",
  //   "extendedTimeOut": "1000",
  //   "showEasing": "swing",
  //   "hideEasing": "linear",
  //   "showMethod": "fadeIn",
  //   "hideMethod": "fadeOut",
  //   "iconClasses": {
  //     "error": '',
  //     "info": '',
  //     "success": '',
  //     "warning": ''
  //   }
  // }
  toastr.options = {
    "closeButton": false,
    "debug": false,
    "newestOnTop": false,
    "progressBar": false,
    "toastClass": "mc-notification-center",
    "positionClass": "",
    "preventDuplicates": false,
    "onclick": null,
    "showDuration": "300",
    "hideDuration": "1000",
    "timeOut": "5000",
    "extendedTimeOut": "1000",
    "showEasing": "swing",
    "hideEasing": "linear",
    "showMethod": "fadeIn",
    "hideMethod": "fadeOut"
  }

  $('#showToastr').click(function () {
    toastr.error("创建失败!");
  });
</script>

{% endexample %}