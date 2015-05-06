---
layout: page
title: Form
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##尺寸

###默认尺寸
适用于较小的view，采用 3:8 的珊隔布局的水平排列表单


{% example html %}

<div style='height:400px;width:100%;background-color:#f1f1f1'>
  <div class='mc-modal'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>New Label</div>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-close"></span>
      </button>
    </div>
    <div class='mc-modal-body'>
      <form class="form-horizontal">
        <div class="form-group">
          <label for="inputAvatar" class="col-sm-3 control-label">Avatar</label>
          <div class="col-sm-8">
            <img class="mc-avatar-big" src="https://avatar.tower.im/2458b7b4c2814259813404ce21749c2e"/><br>
          </div>
        </div>
        <div class="form-group">
          <label for="inputLabelName" class="col-sm-3 control-label">Label Name</label>
          <div class="col-sm-8">
            <input type="email" class="form-control" id="inputLabelName" placeholder="Please input label's name">
          </div>
        </div>
        <div class="form-group">
          <label for="inputLabelColor" class="col-sm-3 control-label">Label Color</label>
          <div class="col-sm-8">
            <button id="inputLabelColor" class='mc-button'>Blue  <span class="caret"></span></button>
          </div>
        </div>
      </form>
    </div>
  </div>
</div>

{% endexample %}


###大尺寸
适用于较大的view，采用 3:8 的珊隔布局的水平排列表单

{% example html %}

<div style='height:500px;width:100%;background-color:#f1f1f1'>
  <div class='mc-modal mc-modal-big'>
    <div class='mc-modal-header'>
      <div class='mc-modal-title'>New Label</div>
      <button type="button" class="mc-button-nobg">
        <span class="mc-icon-close"></span>
      </button>
    </div>
    <div class='mc-modal-body'>
      <form class="form-horizontal">
        <div class="form-group">
          <label for="inputLabelName" class="col-sm-3 control-label">Label Name</label>
          <div class="col-sm-8">
            <input class="form-control" id="inputLabelName" placeholder="Please input label's name">
          </div>
        </div>
        <div class="form-group">
          <label for="inputLabelColor" class="col-sm-3 control-label">Label Color</label>
          <div class="col-sm-8">
            <button id="inputLabelColor" class='mc-button'>Blue  <span class="caret"></span></button>
          </div>
        </div>
        <div class="form-group">
          <label for="inputLabelColor" class="col-sm-3 control-label">Filter</label>
          <div class="col-sm-8">
            <button id="inputLabelColor" class='mc-button-primary mc-button-small'>Add Filter</button>
            <span id="helpBlock" class="help-block">Label incoming messages automatically.  <a href='#'> Learn more</a></span>
          </div>
        </div>
        <div class="form-group">
          <label for="inputLabelColor" class="col-sm-3 control-label">Action</label>
          <div class="col-sm-8">
            <button id="inputLabelColor" class='mc-button-primary mc-button-small'>Add Action</button>
            <span id="helpBlock" class="help-block">Manage action of messages been labeled.  <a href='#'> Learn more</a></span>
          </div>
        </div>
      </form>
    </div>
    <div class='mc-modal-footer'>
      <div class='mc-modal-footer-right'>
        <button class='mc-button-primary' disabled='disabled'>Create</button>
        <button class='mc-button-link'>Cancel</button>
      </div>
    </div>

  </div>
</div>

{% endexample %}
