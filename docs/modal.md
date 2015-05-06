---
layout: page
title: Modal
---

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}


##Layout
{% example html %}
<div style='height:600px;width:100%;background-color:#f1f1f1'>
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

{% endexample %}


##尺寸
这个待定，gary 稍后同步

##种类

###One Column

###Two Column

##动画
可以用 boot strip 默认的

{% example html %}
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">
  show modal
</button>

<div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
        <h4 class="modal-title" id="myModalLabel">创建新的标签</h4>
      </div>
      <div class="modal-body">
        
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">取消</button>
        <button type="button" class="btn btn-primary">创建</button>
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