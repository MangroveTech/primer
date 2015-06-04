---
layout: page
title: Messagelist
---

{% example html %}

<div style='height:800px;width:100%;background-color:#ececec'>
  <div class='mc-messagelist'>
    <div class='mc-section'>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-messagelist-item-left-mark'></div>
          <div class='mc-avatar-mid'></div>
        </div>
        <div class='mc-messagelist-item-content'>
          <div class="mc-messagelist-date ng-binding"> 4:33 PM
            <div class="btn-group mc-replybox-header-replystatus">
              <button class='mc-messagelist-info-button mc-button-link' type="button" id="replyDropdown" data-toggle="dropdown" aria-expanded="true"><span class="caret" ></span></button>
              <ul class="dropdown-menu mc-dropdown-menu" role="menu" aria-labelledby="replyDropdown">
                <li role="presentation"><a ng-click="replyToOne(message)" role="menuitem" tabindex="-1">Reply</a></li>
                <li role="presentation" ng-show="message.to.length + message.from.length + message.cc.length > 2" class="ng-hide"><a ng-click="replyToAll(message)" role="menuitem" tabindex="-1">Reply to all</a></li>
                <li role="presentation"><a ng-click="forwardMsg(message)" role="menuitem" tabindex="-1">Forward</a></li>
              </ul>
            </div>
          </div>
          <div class='mc-messagelist-headline'>Gary Chai</div>
          <div class='mc-messagelist-content'>Koala is a GUI application for Less, Sass, Compass and CoffeeScript compilation, to help web developers to use them more efficiently. Koala can run in windows, linux and mac</div>
        </div>
        <span class='divider'></span>
      </div>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-messagelist-item-left-mark'></div>
          <div class='mc-avatar-mid'></div>
        </div>
        <div class='mc-messagelist-item-content'>
          <div class="mc-messagelist-date ng-binding"> 4:33 PM
            <div class="btn-group mc-replybox-header-replystatus">
              <button class='mc-messagelist-info-button mc-button-link' type="button" id="replyDropdown" data-toggle="dropdown" aria-expanded="true"><span class="caret" ></span></button>
              <ul class="dropdown-menu mc-dropdown-menu" role="menu" aria-labelledby="replyDropdown">
                <li role="presentation"><a ng-click="replyToOne(message)" role="menuitem" tabindex="-1">Reply</a></li>
                <li role="presentation" ng-show="message.to.length + message.from.length + message.cc.length > 2" class="ng-hide"><a ng-click="replyToAll(message)" role="menuitem" tabindex="-1">Reply to all</a></li>
                <li role="presentation"><a ng-click="forwardMsg(message)" role="menuitem" tabindex="-1">Forward</a></li>
              </ul>
            </div>
          </div>
          <div class='mc-messagelist-headline'>Zachary Foster</div>
          <div class='mc-messagelist-content'>Hey Gary, thanks for the reply, this is a very glad to help</div>
        </div>
        <span class='divider'></span>
      </div>
      <div class='mc-messagelist-item'>
        <div class='mc-messagelist-item-left'>
          <div class='mc-avatar-mid'></div>
        </div>

        <div class='mc-messagelist-item-content'>
          <div class="mc-messagelist-date ng-binding"> 4:33 PM
            <div class="btn-group mc-replybox-header-replystatus">
              <button class='mc-messagelist-info-button mc-button-link' type="button" id="replyDropdown" data-toggle="dropdown" aria-expanded="true"><span class="caret" ></span></button>
              <ul class="dropdown-menu mc-dropdown-menu" role="menu" aria-labelledby="replyDropdown">
                <li role="presentation"><a ng-click="replyToOne(message)" role="menuitem" tabindex="-1">Reply</a></li>
                <li role="presentation" ng-show="message.to.length + message.from.length + message.cc.length > 2" class="ng-hide"><a ng-click="replyToAll(message)" role="menuitem" tabindex="-1">Reply to all</a></li>
                <li role="presentation"><a ng-click="forwardMsg(message)" role="menuitem" tabindex="-1">Forward</a></li>
              </ul>
            </div>
          </div>
          <div class='mc-messagelist-headline'>Gary Chai</div>

          <div class="mc-messagelist-content">To me, Jack Wang
            <button type="button" class="mc-messagelist-deatil-button btn btn-link" data-toggle="popover" data-content='<table rules="none" class="table table-condensed table-bordered"><tbody><tr><th scope="row">from:</th><td>Zachary Foster (zfoster@clearslide.com)</td></tr><tr><th scope="row">to:</th><td>Gary Chai (gary@clearslide.com)<br>Arthur li (arthurli1991@gmail.com)</td></tr><tr><th scope="row">cc:</th><td colspan="2">Larry the Bird (arthurli1991@gmail.com)</td></tr><tr><th scope="row">date:</th><td colspan="2">Fri,May 29,2015 at 2:50 PM</td></tr></tbody></table>' aria-expanded="false">
            <span class="caret"></span>
            </button>
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
<script type="text/javascript">

$(function () {
  $('[data-toggle="popover"]').popover({
    html:true,
    placement:'bottom',
    trigger:'click'
  })
})

</script>

  {% endexample %}