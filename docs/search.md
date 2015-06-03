---
layout: page
title: Search
---


* 此处不用改，将下面所有的 2 级标题制成索引...
{:toc}

## Search Autocomplate

{% example html %}

<div style='height:400px;width:100%;background-color:#ececec'>
  <input type="text" class="mc-searchfield" placeholder="Search" value="app" style="box-shadow: inset 0 1px 1px rgba(0,0,0,0.075),0 0 8px rgba(102,175,233,0.6);border-color: #66afe9;outline: 0; width:400px;">
  <div class='mc-search-result' style="float: right;clear: right;margin: -1px 20px 0 0;">
    <div class='mc-search-result-section'>
      <div class='mc-search-result-info'>
        <span class='mc-icon-search'></span>
      </div>
      <div class='mc-search-result-content'>
        app
      </div>
    </div>
    <div class='mc-search-result-section'>
      <div class='mc-search-result-info'>
        <span class='mc-icon-search'></span>
      </div>
      <div class='mc-search-result-content'>
        application
      </div>
    </div>
    <div class='mc-search-result-section'>
      <div class='mc-search-result-info'>
        <span class='mc-icon-search'></span>
      </div>
      <div class='mc-search-result-content'>
        your application
      </div>
    </div>
    <div class='divider'></div>
    <div class='mc-search-result-section'>
      <div class='mc-search-result-info'>
        <img class="mc-avatar-small" src="../img/Mailcup-avatar-default.png"/>
      </div>
      <div class='mc-search-result-content'>
        Mike Johnson (mike.johnson@app.com)
      </div>
    </div>
    <div class='mc-search-result-section'>
      <div class='mc-search-result-info'>
        <img class="mc-avatar-small" src="../img/Mailcup-avatar-default.png"/>
      </div>
      <div class='mc-search-result-content'>
        App annie (info@appannie.com)
      </div>
    </div>    
  </div>
</div>

<script type="text/javascript">
$(".mc-searchfield").focus();
</script>
{% endexample %}

## Search Result

{% example html %}

<div style='height:400px;width:100%;background-color:#ececec'>
  <div class='mc-navbar'>
    <div class='mc-navbar-titlearea'>
        <button type="button" class="mc-navbar-backbutton">
          <span class="mc-icon-back" aria-hidden="true"></span>
        </button>
        <input type="text" class="mc-searchfield" placeholder="Search" value="Gary Chai" style="width:400px;">
    </div>
    <div class='mc-navbar-functionarea'>
      <div class='mc-navbar-subject'>Search Result</div>
    </div>
  </div>
</div>
{% endexample %}
