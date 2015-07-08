---
layout: page
title: Replybox
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##未激活

{% example html %}

<div style='height:100px;width:100%;background-color:#ececec'>
  <div class='mc-replybox'>
    <div class='mc-replysection mc-replybox-unactive'>
      <div class='mc-replybox-header'>
        <img class="mc-avatar-mid" src="https://avatar.tower.im/2458b7b4c2814259813404ce21749c2e"/>
        <div class="mc-replybox-placeholder">Reply to all</div>
        <div class='mc-replybox-header-right'>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-reply"></span>
          </button>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-reply-all"></span>
          </button>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-forward"></span>
          </button>
        </div>
      </div>
    </div>

  </div>
</div>

{% endexample %}

##激活

{% example html %}

<div style='height:400px;width:100%;background-color:#f1f1f1'>
  <div class='mc-replybox'>
    <div class='mc-replysection'>
      <div class='mc-replybox-header'>
        <img class="mc-avatar-mid" src="https://avatar.tower.im/2458b7b4c2814259813404ce21749c2e"/>
        <div class="mc-replybox-header-info">
          <div class="btn-group mc-replybox-header-replystatus">
            <button type="button" class="btn btn-link dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
              Reply all <span class="caret"></span>
            </button>
            <ul class="dropdown-menu" role="menu">
              <li><a href="#">Reply to Jessie</a></li>
              <li><a href="#">Forward</a></li>
              <li class="divider"></li>
              <li><a href="#">Edit recipients</a></li>
            </ul>
          </div>
          <div class='mc-replybox-header-recipients'>
            Jessie Zhang, Kevin Li
          </div>
        </div>
      </div>
      <div class='mc-replbox-body'>
        <div class='mc-replybox-editor' contenteditable="true">
          <br>
          <br>
          <br>
          <div class="gmail_quote">Wed Jul 08 2015 11:19:36 GMT+0800 (CST) ck<span dir="ltr">&lt;<a href="mailto:ck@just.test.mailcup.com" target="_blank">ck@just.test.mailcup.com</a>&gt;</span>:
            <br>
            <blockquote class="gmail_quote" style="margin:0 0 0 .8ex;border-left:1px #ccc solid;padding-left:1ex">
                <div dir="ltr">hehe
                    <br>
                    <br>
                    <div>--</div>
                    <div>程科</div>from mailcup
                    <br>
                    <br>
                    <blockquote id="quoteDetail" style="margin:0 0 0 .8ex;border-left:1px #ccc solid;padding-left:1ex" ng-show="show">
                        <div>ck
                            \<ck@just.test.mailcup.com\>于Mon Jul 06 2015 18:41:07 GMT+0800 (CST)写到:
                              <div>
                                  <br>hehe
                                  <br>
                                  <br>
                              </div>
                        </div>
                    </blockquote>
                </div>
            </blockquote>
          </div>
          <br><br>--<br>Send from Mailcup
        </div>
      </div>
      <div class='mc-modal-footer'>
        <div class='mc-modal-footer-left'>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-text"></span>
          </button>
          <button type="button" class="mc-button-nobg">
            <span class="mc-icon-clip"></span>
          </button>
        </div>
        <div class='mc-modal-footer-right'>
          <button class='mc-button-primary'>Send</button>
        </div>
      </div>
    </div>
  </div>
</div>

{% endexample %}


