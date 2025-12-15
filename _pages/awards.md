---
layout: archive
title: "获奖荣誉"
permalink: /awards/
author_profile: true
---

{% include base_path %}

<style>
/* 列表样式优化 */
ul.award-list {
  margin-left: 20px; 
  list-style-type: disc; 
}
ul.award-list li {
  margin-bottom: 15px; 
}
/* 辅助信息样式 (年份、级别) */
.award-meta {
  font-size: 0.85em;
  color: #666;
  font-style: italic;
  display: block; 
  margin-top: 2px;
}
</style>


<ul class="award-list">
{% for post in site.awards reversed %}
  <li>
      <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a>
      
      <span class="award-meta">
        {{ post.date | date: "%Y" }} | {{ post.excerpt }}
      </span>
  </li>
{% endfor %}
</ul>
