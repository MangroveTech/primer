---
layout: page
title: Modal
---

测试测试

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

### Modal

bootstrap 原生 modal.

{% example html %}
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">
  show modal
</button>

<div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
        <h4 class="modal-title" id="myModalLabel">Modal title</h4>
      </div>
      <div class="modal-body">
        程科是狗
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
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