---
layout: page
title: Table
---

Table 提供了 Mailcup 所有表格方案

你可以在下面的CSS文件里找到 `table.scss`.

* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

##尺寸

{% example html %}
<table class="mc-table table-hover">
      <tbody>
        <tr>
          <th scope="row"><span class="mc-leftmenu-item-label"></span>Team</th>
          <td><button class='mc-button-link'>Edit</button></td>
          <td><button class='mc-button-link-danger'>Remove</button></td>
        </tr>
        <tr>
          <th scope="row"><span class="mc-leftmenu-item-label"></span>Feedback</th>
          <td><button class='mc-button-link'>Edit</button></td>
          <td><button class='mc-button-link-danger'>Remove</button></td>
        </tr>
        <tr>
          <th scope="row"><span class="mc-leftmenu-item-label"></span>Product</th>
          <td><button class='mc-button-link'>Edit</button></td>
          <td><button class='mc-button-link-danger'>Remove</button></td>
        </tr>
      </tbody>
</table>
{% endexample %}
