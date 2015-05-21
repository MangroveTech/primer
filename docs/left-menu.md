---
layout: page
title: Left Menu
---

* 如果在webmial中的最下方使用Settings，那么需要在`mc-leftmenu-section`后面加入`mc-fixed-bottom`

{% example html %}
<div style='height:500px;'>
  <div class='mc-leftmenu'>
    <div class='mc-leftmenu-logo'></div>
    <div class='mc-leftmenu-section'>
      <ul>
        <a class="active" href="#">
          <span class='active-ind'></span>
          <li><span class='mc-leftmenu-icon mc-icon-inbox'></span><strong>Inbox</strong></li>
        </a>
        <a href="#">
          <li><span class='mc-leftmenu-icon mc-icon-pin'></span>Follow up</li>
        </a>
        <a href="#">
          <li><span class='mc-leftmenu-icon mc-icon-done'></span>Done</li>
        </a>
      </ul>
    </div>
    <div class='mc-leftmenu-section'>
      <span class='mc-leftmenu-section-title'>
        <span class='glyphicon glyphicon-triangle-bottom'></span>
        LABELS
      </span>
      <ul>
        <a href="#"><li><span class="mc-leftmenu-item-label"></span>Team</li></a>
        <a href="#"><li><span class="mc-leftmenu-item-label"></span>Feedback</li></a>
      </ul>
    </div>
    <div class='mc-leftmenu-section'>
      <span class='mc-leftmenu-section-title'>
        <span class='glyphicon glyphicon-triangle-bottom'></span>
        OTHERS
      </span>
      <ul>
        <a href="#"><li>Spam</li></a>
        <a href="#"><li>Trash</li></a>
      </ul>
    </div>
    <div class="mc-leftmenu-section">
    <span class="mc-leftmenu-section-title">
      <span class="btn-group dropup">
      <span class='mc-leftmenu-section-text' data-toggle="dropdown" aria-expanded="false">
        <span class='mc-icon-setting'></span>
        Settings
      </span>
        <ul class="dropdown-menu mc-text-small" style="font-weight" role="menu">
          <li>Settings</li>
          <li>Domain Management</li>
          <li>Feedback & Help</li>
          <li>Sign out</li>
        </ul>
      </span>
    </span>
  </div>
  </div>
</div>

<script type="text/javascript">
  $('.mc-leftmenu-section-title .glyphicon').click(function() {
    if ($(this).attr('class').match('glyphicon-triangle-bottom')) {
      $(this).removeClass('glyphicon-triangle-bottom');
      $(this).addClass('glyphicon-triangle-right');
    } else {
      $(this).removeClass('glyphicon-triangle-right');
      $(this).addClass('glyphicon-triangle-bottom');
    }
    $(this).parent().next().slideToggle('fast');
  });
</script>
{% endexample %}