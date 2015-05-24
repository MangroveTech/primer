---
layout: page
title: Navbar
---

##Root
{% example html %}
<div style='height:200px;width:100%;background-color:#f1f1f1'>
  <div class='mc-navbar'>
    <div class='mc-navbar-titlearea'>
        <span class='mc-navbar-title'>Inbox</span>
        <input type="text" class="mc-searchfield" placeholder="Search">
    </div>
    <div class='mc-navbar-functionarea'>
        <button class='mc-navbar-newbutton'>New message</button>
    </div>
  </div>
</div>
{% endexample %}

##Content
{% example html %}
<div style='height:200px;width:100%;background-color:#f1f1f1'>
  <div class='mc-navbar'>
    <div class='mc-navbar-titlearea'>
        <button type="button" class="mc-navbar-backbutton">
          <span class="mc-icon-back" aria-hidden="true"></span>
        </button>
        <input type="text" class="mc-searchfield" placeholder="Search">
        <div class='mc-navbar-toolbutton'>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-done"></span>
          </button>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-pin"></span>
          </button>
          <div class="btn-group">
            <button type="button" class="mc-button-nobg dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
              <span class="mc-icon-label"></span>
            </button>
            <ul class="dropdown-menu" role="menu" id="mc-label-select">
              <li><a>Label as:</a></li>
              <li class="divider"></li>
              <li><a><input type="checkbox" id="mc-checkbox-green" checked/><label for="mc-checkbox-green"></label> green</a></li>
              <li><a><input type="checkbox" id="mc-checkbox-blue" checked/><label for="mc-checkbox-blue"></label> blue</a></li>
              <li><a><input type="checkbox" id="mc-checkbox-orange" checked/><label for="mc-checkbox-orange"></label> orange</a></li>
              <li class="divider"></li>
              <li><a class="mc-icon-plus"> &nbsp;Create new...</a></li>
            </ul>
          </div>
          <div class="btn-group">
            <button type="button" class="mc-button-nobg dropdown-toggle"  data-toggle="dropdown">
              <span class="mc-icon-more"></span>
            </button>
            <ul class="dropdown-menu" role="menu">
              <li><a href="#">转发全部</a></li>
              <li><a href="#">打印全文</a></li>
              <li class="divider"></li>
              <li><a href="#">删除会话</a></li>
            </ul>
          </div>
        </div>
    </div>
    <div class='mc-navbar-functionarea'>
      <div class='mc-navbar-subject'>这里是邮件的标题</div>
    </div>
  </div>
</div>
{% endexample %}

##Search
