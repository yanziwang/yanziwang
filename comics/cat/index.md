---
layout:  page
title: 归档
description: 归档
---
<div class="posts home">
    <div class="content indeximg">
        <p class="center">
            <a href="/archive" style="border-bottom: 0px">
            <img src="/images/cat.png" style="width:100px; height:100px" />
            </a>
        </p>
        <p class="center">闹眼子居酒屋漫画集</p>
    </div>
</div>

<ul class="archive" style="margin-top: 30px">
{% for post in site.categories.cat %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  <li class="item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>