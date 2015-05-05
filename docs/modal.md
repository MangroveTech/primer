---
layout: page
title: Modal
---

测试测试

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}


##Header, Body, Footer
这里要注意 Footer 的交互效果

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