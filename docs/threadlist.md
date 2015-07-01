---
layout: page
title: Threadlist
---

##Inbox Page


{% example html %}

<div style='height:600px;width:100%;background-color:#ececec'>
  <div class='mc-threadlist-section'>
    <div class='mc-section-header'>
      <span class='mc-text-content'>Today</span>
      <button class='mc-button-nobg'><span class='mc-icon-done-all'></span></button>
    </div>
    <div class='mc-section'>
      <a class='mc-threadlist-item'>
        <div class='mc-threadlist-item-left'>
          <div class='mc-threadlist-item-unread'></div>
          <img class="mc-avatar-mid" src="../img/Mailcup-avatar-default.png"/>
        </div>
        <div class='mc-threadlist-item-content'>
          <div class='mc-threadlist-headline'><strong>Gary Chai</strong><span class="mc-icon-clip"></span></div>
          <div class='mc-threadlist-subject'>
            <span class="mc-label-info">Team</span> Please confirm your address - <span class="mc-threadlist-summary">Hey John, I see you profile and glad to help, please check the address blow if is right? If you think there has some other questions</span>
          </div>
        </div>
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg' onclick="closeanimation()"><span class="mc-icon-done"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>12:22 PM</div>
      </a>
    </div>
    <div class='mc-section'>
      <a class='mc-threadlist-item'>
        <div class='mc-threadlist-item-left'>
          <div class='mc-threadlist-item-unread'></div>
          <img class="mc-avatar-mid" src="../img/Mailcup-avatar-default.png"/>
        </div>
        <div class='mc-threadlist-item-content'>
          <div class='mc-threadlist-headline'><strong>Arthur li</strong>, me (2)</div>
          <div class='mc-threadlist-subject'>
            Daily Status of May 25 ,2015 - <span class="mc-threadlist-summary">Li fixing dsty-1288 
Sheng fixing dsty-1282 Liu fixing dsty-479 Adam fixing dsty-1281</span>
          </div>
        </div>
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg' onclick="closeanimation()"><span class="mc-icon-done"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>12:22 PM</div>
      </a>
    </div>
    <div class='mc-section'>
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
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg' onclick="closeanimation()"><span class="mc-icon-done"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>11:51 PM</div>
      </a>
    </div>
    <div class='mc-section mc-section-selected mc-section-last'>
      <a class='mc-threadlist-item'>
        <div class='mc-threadlist-item-left'>
          <img class="mc-avatar-mid" src="../img/Mailcup-avatar-default.png"/>
        </div>
        <div class='mc-threadlist-item-content'>
          <div class='mc-threadlist-headline'>Gong Bao</div>
          <div class='mc-threadlist-subject'>
           [JIRA] (MAILCUP-595) landing page - <span class="mc-threadlist-summary">MAILCUP / Story MAILCUP-595 landing  New technologies are changing every aspects of the business world. In this talk, Cheng Li will illustrate how Alibaba and Ant Financial </span>
          </div>
        </div>
        <div class='mc-threadlist-item-right'>
          <div><button class='mc-button-nobg'><span class="mc-icon-done"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-pin"></span></button></div>
          <div><button class='mc-button-nobg'><span class="mc-icon-label"></span></button></div>
        </div>
        <div class='mc-threadlist-date'>12:22 PM</div>
      </a>
    </div>
  </div>
  <div class='mc-threadlist-loadmore'>Loading more...</div>
</div>

<script type="text/javascript">

$(".mc-button-nobg").click(function() {
      var $p = $(this).parent().parent().parent().parent();
      var $this = $(this);
        $p.slideUp(200, function() {
            //移除父级div
            $p.remove();
        });
    });
</script>

{% endexample %}


##Follow up Page

{% example html %}
<div style='height:350px;width:100%;background-color:#f1f1f1'>
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
    <div class='mc-section mc-section-marked mc-section-selected'>
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
    <div class='mc-section mc-section-marked mc-section-selected'>
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
{% endexample %}
