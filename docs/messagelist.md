---
layout: page
title: Messagelist
---

{% example html %}

<div style='height:800px;width:100%;background-color:#f1f1f1'>
  <div class='mc-messagelist'>
    <div class='mc-section'>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-avatar-mid'></div>
        </div>
        <div class='mc-messagelist-item-content'>
          <div class='mc-messagelist-headline'><strong>Gary Chai</strong></div>
          <div class='mc-messagelist-content'>Hey Zachary, I see you profile and glad to help, please check the</div>
        </div>
        <span class='divider'></span>
      </div>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-avatar-mid'></div>
        </div>
        <div class='mc-messagelist-item-content'>
          <div class='mc-messagelist-headline'><strong>Zachary Foster</strong></div>
          <div class='mc-messagelist-content'>Hey Gary, thanks for the reply, this is a very glad to help</div>
        </div>
      </div>
    </div>
  </div>

  <div class='mc-messagelist'>
    <div class='mc-section'>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-avatar-mid'></div>
        </div>
        <div class='mc-messagelist-item-content'>
          <div class='mc-messagelist-headline'><strong>Gary Chai</strong></div>
          <div class='mc-messagelist-content'>to Jack, Zachary
            <div class="btn-group">
              <button type="button" class="mc-button-nobg dropdown-toggle" data-toggle="dropdown" aria-expanded="false">
              <span class="mc-icon-arrow-down"></span>
              </button>
              <ul class="dropdown-menu" role="menu" id="mc-messagelist-info">
                <li><a><span>From: </span> shuangchun@mailcup.com</a></li>
                <li><a><span>To: </span> shuangchun@mailcup.com</a></li>
                <li><a><span>Cc: </span> shuangchun@mailcup.com</a></li>
                <li><a><span>Date: </span> 2014-10-20 10:30</a></li>
              </ul>
            </div>
          </div>
        </div>
        <div class='mc-messagelist-item-body'>
          Hey Gary and Mangrove Team:<br><br>

          This is an important message regarding future branches and pull requests.<br><br>

          For work that is NOT green screen related, please branch off of master. Please create pull requests to merge into master<br><br>

          git checkout master<br>
          git pull<br>
          git checkout -b myfeature<br><br><br>


          Only for green screen work, please branch off of edge, and create pull requests to merge into edge.<br><br>

          git checkout edge<br>
          git pull<br>
          git checkout -b mygreenscreenwork<br><br>

          For the pending pull requests, just leave them as is and I will figure out the best way to get them over to master.<br><br>

          Thanks,<br>
          Zack
        </div>
    </div>
  </div>

</div>

{% endexample %}