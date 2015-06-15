---
layout: page
title: Modal
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}


##Layout
{% example html %}
<div style='height:30px;width:100%;'>
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal1">
  show modal
</button>
<div class="modal fade" id="myModal1" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class='mc-modal'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>New Label</div>
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
    <div class='mc-modal-body'>
      <p>利用 CSS 来实现对象的垂直居中有许多不同的方法，比较难的是选择那个正确的方法。我下面说明一下我看到的好的方法和怎么来创建一个好的居中网站。
      </p>
      <p>
        使用 CSS 实现垂直居中并不容易。有些方法在一些浏览器中无效。下面我们看一下使对象垂直集中的5种不同方法，以及它们各自的优缺点。(可以看看测试页面，有简短解释。
      </p>
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
        <button class='mc-button-primary'>Create</button>
        <button class='mc-button-link'>Cancel</button>
      </div>
    </div>
  </div>
  </div>

</div>

<script type="text/javascript">
  $('#myModal1').modal({
    show: false
  });
</script>

{% endexample %}


##尺寸
* 正常尺寸 560px 默认值
* `mc-modal-big` 720px 大尺寸

{% example html %}
<div style='height:30px;width:100%;'>
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal2">
  show modal
</button>
<div class="modal fade" id="myModal2" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class='mc-modal mc-modal-big'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>Settings</div>
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
    <div class='mc-modal-body'>
      <br><br><br><br>
    </div>
    <div class='mc-modal-footer'>
      <div class='mc-modal-footer-right'>
        <button class='mc-button-primary'>Save</button>
        <button class='mc-button-link'>Cancel</button>
      </div>
    </div>
  </div>
  </div>

</div>

<script type="text/javascript">
  $('#myModal2').modal({
    show: false
  });
</script>

{% endexample %}

##种类
* 默认为单列
* 在 `mc-modal-body` 中添加 `mc-modal-body-left` 和 `mc-modal-body-right` 可变为双列

{% example html %}
<div style='height:30px;width:100%;'>
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal3">
  show modal
</button>
<div class="modal fade" id="myModal3" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class='mc-modal mc-modal-big'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>Settings</div>
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
    <div class='mc-modal-body-twocolumn'>
      <div class="col-sm-3 mc-modal-body-left">
        <div class="list-group">
          <a href="#" class="list-group-item active">
            Account
          </a>
          <a href="#" class="list-group-item">Label</a>
          <a href="#" class="list-group-item">Group</a>
          <a href="#" class="list-group-item">Notification</a>
          <a href="#" class="list-group-item">Filehub</a>
        </div>
      </div>
      <div class="col-sm-9">
        <div class='mc-modal-body-right'>
          <form class="form-horizontal">
            <div class="form-group">
              <div for="inputAvatar" class="col-sm-3 control-label">Avatar</div>
              <div class="col-sm-8">
                <img class="mc-avatar-big" src="https://avatar.tower.im/2458b7b4c2814259813404ce21749c2e"/><br>
              </div>
            </div>
            <div class="form-group">
              <div for="inputLabelName" class="col-sm-3 control-label">Name</div>
              <div class="col-sm-8">
                <input type="name" class="form-control" id="inputName" placeholder="Please input your name">
              </div>
            </div>
            <div class="form-group">
              <div for="inputSignature" class="col-sm-3 control-label">Signature</div>
              <div class="col-sm-8">
                <div id="inputSignature" contenteditable="true" class='mc-modal-signature-editor'>--<br>Sent by Mailcup</div>
              </div>
            </div>
            <div class="form-group">
              <div for="save" class="col-sm-3 control-label"></div>
              <div class="col-sm-8">
              <button class='mc-button'>Save</button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
  </div>

</div>
<script type="text/javascript">
  $('#myModal3').modal({
    show: false
  });
</script>

{% endexample %}

##动画
可以用 boot strip 默认的

{% example html %}
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">
  show modal
</button>

<div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class='mc-modal'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>Settings</div>
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
    <div class='mc-modal-body-twocolumn'>
      <div class="col-sm-2">
        <div class='mc-modal-body-left'>
          <div class="active">Account</div>
          <div>Labels</div>
          <div>Groups</div>
          <div>Templates</div>
          <div>Notifications</div>
        </div>
      </div>
      <div class="col-sm-10">
        <div class='mc-modal-body-right'>
          <div class="mc-form-group">
            <div class="col-sm-3">name</div>
            <div class="col-sm-9"><input class="form-control" /></div>
          </div>
          <div class="mc-form-group">
            <div class="col-sm-3">namname</div>
            <div class="col-sm-9"><input class="form-control" /></div>
          </div>
          <div class="mc-form-group">
            <div class="col-sm-3">namname</div>
            <div class="col-sm-9"><input class="form-control" /></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<script type="text/javascript">
  $('#myModal').modal({
    show: false
  });
</script>
{% endexample %}

##用以兼容angular-bootstrap
* 这里的样式只有宽度为 720px 的大尺寸

{% example html %}
<div style='height:30px;width:100%;'>
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal2">
  show modal
</button>
<div class="modal fade" id="myModal2" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class='modal-content'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>Settings</div>
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
    <div class='mc-modal-body'>
      <br><br><br><br>
    </div>
    <div class='mc-modal-footer'>
      <div class='mc-modal-footer-right'>
        <button class='mc-button-primary'>Save</button>
        <button class='mc-button-link'>Cancel</button>
      </div>
    </div>
  </div>
  </div>

</div>

<script type="text/javascript">
  $('#myModal2').modal({
    show: false
  });
</script>

{% endexample %}