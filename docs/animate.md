---
layout: page
title: Animate
---

Animate 提供了 Mailcup 所有动画方案

你可以在下面的CSS文件里找到 `animate.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##引入动画
在需要用到的地方的div、a、button等标签，在 class 上添加添加 `{动画名称} mc-animated`。

{% example html %}
<div>
  <form>
      <select class="input input--dropdown js--animations">
          <option value="fadeIn">fadeIn</option>
          <option value="fadeOut">fadeOut</option>
      </select>
      <button class="mc-button-primary js--triggerAnimation">开始动画</button>
    </form>
  <div style='height:150px;width:100%;background-color:#f1f1f1'>
  <div class='mc-threadlist-section'>
    <div class='mc-section-header'>
      <span class='mc-text-content'>Follow up</span>
      <button class='mc-button-nobg'><span class='mc-icon-alldone'></span></button>
    </div>
    <div class='mc-section mc-section-marked' id="animationSandbox">
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
</div>
</div>
<script type="text/javascript">
function testAnim(x) {
    $('#animationSandbox').removeClass().addClass(x + ' mc-animated').one('webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend', function(){
      $(this).removeClass();
    });
  };

  $(document).ready(function(){
    $('.js--triggerAnimation').click(function(e){
      e.preventDefault();
      var anim = $('.js--animations').val();
      testAnim(anim);
    });

    $('.js--animations').change(function(){
      var anim = $(this).val();
      testAnim(anim);
    });
  });
</script>
{% endexample %}
