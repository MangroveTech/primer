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
        <button class='mc-button-primary'>Create</button>
        <button class='mc-button-link'>Cancel</button>
      </div>
    </div>

  </div>
</div>

{% endexample %}

##FileHub

###用于在FileHub的使用

{% example html %}

<div style='height:400px;width:100%;background-color:#f1f1f1'>
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
          <a href="#" class="list-group-item">
            Account
          </a>
          <a href="#" class="list-group-item">Label</a>
          <a href="#" class="list-group-item">Group</a>
          <a href="#" class="list-group-item">Notification</a>
          <a href="#" class="list-group-item active">Filehub</a>
        </div>
      </div>
      <div class="col-sm-9">
        <div class='mc-modal-body-right'>
          <form class="form-horizontal">
            <table class="mc-table table-hover">
              <tbody>
                <tr>
                  <td>
                    <div class="mc-attachment-filehub">
                      <span class="mc-attachment-zip"></span>
                      <div class="mc-attachment-info">
                        <div class="mc-attachment-title">Mailcup-PD-0.5.2.zip</div>
                        <div class="mc-attachment-size">144.2kb</div>
                      </div>
                    </div>
                  </td>
                  <td><button class='mc-button-link'>Download</button></td>
                  <td><button class='mc-button-link-danger'>Delete</button></td>
                </tr>
              </tbody>
            </table>
            <table class="mc-table table-hover">
              <tbody>
                <tr>
                  <td>
                    <div class="mc-attachment-filehub">
                      <span class="mc-attachment-zip"></span>
                      <div class="mc-attachment-info">
                        <div class="mc-attachment-title">Mailcup-PD-0.5.2.zip</div>
                        <div class="mc-attachment-size">144.2kb</div>
                      </div>
                    </div>
                  </td>
                  <td><button class='mc-button-link'>Download</button></td>
                  <td><button class='mc-button-link-danger'>Delete</button></td>
                </tr>
              </tbody>
            </table>
            <table class="mc-table table-hover">
              <tbody>
                <tr>
                  <td>
                    <div class="mc-attachment-filehub">
                      <span class="mc-attachment-zip"></span>
                      <div class="mc-attachment-info">
                        <div class="mc-attachment-title">Mailcup-PD-0.5.2.zip</div>
                        <div class="mc-attachment-size">144.2kb</div>
                      </div>
                    </div>
                  </td>
                  <td><button class='mc-button-link'>Download</button></td>
                  <td><button class='mc-button-link-danger'>Delete</button></td>
                </tr>
              </tbody>
            </table>
            <table class="mc-table table-hover">
              <tbody>
                <tr>
                  <td>
                    <div class="mc-attachment-filehub">
                      <span class="mc-attachment-zip"></span>
                      <div class="mc-attachment-info">
                        <div class="mc-attachment-title">Mailcup-PD-0.5.2.zip</div>
                        <div class="mc-attachment-size">144.2kb</div>
                      </div>
                    </div>
                  </td>
                  <td><button class='mc-button-link'>Download</button></td>
                  <td><button class='mc-button-link-danger'>Delete</button></td>
                </tr>
              </tbody>
            </table>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>

{% endexample %}
