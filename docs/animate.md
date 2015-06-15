---
layout: page
title: Animate
---

Animate 提供了 Mailcup 所有动画方案

你可以在下面的CSS文件里找到 `animate.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##引入动画
在需要用到的地方的div、a、button等标签，在 class 上添加添加 `{动画名称} mc-animate`。

{% example html %}
<div>
  <button class="">开始动画</button>

</div>
{% endexample %}

##所有可用的动画
在需要使用图标的地方直接使用

{% example html %}
<div>
  <button class="">开始动画</button>
  <div style='height:300px;width:100%;background-color:#f1f1f1'>
  <div class='mc-threadlist-section'>
    <div class='mc-section-header'>
      <span class='mc-text-content'>Follow up</span>
      <button class='mc-button-nobg'><span class='mc-icon-alldone'></span></button>
    </div>
    <div class='mc-section mc-section-marked'>
      <a class='mc-threadlist-item'>
        <div class='mc-threadlist-item-left'>
          <img class="mc-avatar-mid" src="../img/Mailcup-avatar-default.png"/>
        </div>
        <div class='mc-threadlist-item-content'>
          <div class='mc-threadlist-headline'>Jacky Li, Gate Johnason, me (5)</div>
          <div class='mc-threadlist-subject'>
            A World Of Indexes In Your Inbox - <span class="mc-threadlist-summary">Dubsmash saw a 2nd wind in terms of downloads, and TurboTax remained a top contender in revenue</span>
          </div>
        </div>
        <div class='mc-threadlist-mark'><span class="mc-icon-pin mc-color-icon-midblue"></span></div>
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg' onclick="closeanimation()"><span class="mc-icon-done"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin mc-color-icon-midblue"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>11:51 PM</div>
      </a>
    </div>
  </div>
  <div class='mc-threadlist-section'>
    <div class='mc-section-header'>
      <span class='mc-text-content'>Done</span>
      <button class='mc-button-nobg'><span class='mc-icon-alldone'></span></button>
    </div>
    <div class='mc-section mc-section-marked'>
      <a class='mc-threadlist-item'>
        <div class='mc-threadlist-item-left'>
          <img class="mc-avatar-mid" src="../img/Mailcup-avatar-default.png"/>
        </div>
        <div class='mc-threadlist-item-content'>
          <div class='mc-threadlist-headline'>Gongbao (JIRA)</div>
          <div class='mc-threadlist-subject'>
           [JIRA] (MAILCUP-630) 从 Message list 回退 到 Thread list，记录滚动的位置 - <span class="mc-threadlist-summary">  Gongbao updated Story MAILCUP-630 MAILCUP / Story MAILCUP-630</span>
          </div>
        </div>
        <div class='mc-threadlist-mark'><span class="mc-icon-done mc-color-icon-midgreen"></span></div>
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg' onclick="closeanimation()"><span class="mc-icon-done mc-color-icon-midgreen"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>11:51 PM</div>
      </a>
    </div>
  </div>
</div>
</div>
{% endexample %}
