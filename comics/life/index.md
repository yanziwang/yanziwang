---
layout:  page
title: 归档
description: 归档
---
<div class="posts home" style="margin-top: -20px">
    <div class="content indeximg">
        <p class="center">
            <a href="/archive" style="border-bottom: 0px">
            <img src="/images/life.png" style="width:200px; height:200px" />
            </a>
        </p>
        <p class="center">生活倒霉蛋</p>
    </div>
</div>

<ul class="archive" style="margin-top: 30px">
{% for post in site.categories.life %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  <li class="item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>