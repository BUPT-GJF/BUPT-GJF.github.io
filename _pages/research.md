---
layout: archive
title: "科学研究"
permalink: /research/
author_profile: true
---

{% include base_path %}

<script>
function toggleSection(id, btnId) {
  var x = document.getElementById(id);
  var btn = document.getElementById(btnId);
  if (x.style.display === "none") {
    x.style.display = "block";
    btn.innerHTML = "收起列表 (Collapse)";
  } else {
    x.style.display = "none";
    btn.innerHTML = "展开全部 (Show All)";
  }
}
</script>

<style>
.show-more-btn {
  background-color: #f2f3f3;
  border: 1px solid #ccc;
  color: #333;
  padding: 8px 16px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  margin: 10px 0;
  cursor: pointer;
  border-radius: 4px;
}
.show-more-btn:hover {
  background-color: #e6e6e6;
}
ul.patent-list {
  margin-left: 10px; /* 调整整体左边距 */
  list-style-type: disc; /* 强制显示圆点 */
}
ul.patent-list li {
  margin-bottom: 5px; /* 条目间距 */
}
</style>

## 1. 研究领域 (Research Areas)

智算融合网络、智慧协同网络、智慧路由、异质异构网络安全。

---

## 2. 科研项目 (Research Projects)

* 智算融合网络异构资源弹性适配机制，进行，许长桥

* 认知互联网体系结构与服务模型研究，结项，关建峰

* 未来移动互联网的流媒体认知传输控制协议研究，结项，许长桥

* 智慧协同的绿色移动流媒体服务研究，结项，许长桥

---

## 3. 发明专利 (Patents)

<ul class="patent-list">
{% for post in site.patents reversed limit:5 %}
  <li>
      <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a>
  </li>
{% endfor %}
</ul>

<div id="more-patents" style="display:none;">
  <ul class="patent-list">
  {% for post in site.patents reversed offset:5 %}
    <li>
        <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a>
    </li>
  {% endfor %}
  </ul>
</div>

<button id="btn-patents" class="show-more-btn" onclick="toggleSection('more-patents', 'btn-patents')">展开全部 (Show All)</button>

---

## 4. 著作成果 (Books)

<ul class="patent-list">
{% for post in site.books reversed %}
  <li>
      <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a><br>
      <small>出版社: {{ post.publisher }} ({{ post.date | date: "%Y" }})</small>
  </li>
{% endfor %}
</ul>

---

## 5. 论文成果 (Publications)

<ul class="patent-list">
{% for post in site.publications reversed limit:5 %}
  <li>
      {% if post.authors %}{{ post.authors }}. {% endif %}
      "<strong>{{ post.title }}</strong>." 
      <i>{{ post.venue }}</i>, 
      {{ post.date | date: "%Y" }}.
      {% if post.paper_level %}
        <span style="color: #d9534f; font-weight: bold; font-size: 0.85em;"> [{{ post.paper_level }}]</span>
      {% endif %}
      {% if post.paperurl %}
        <a href="{{ post.paperurl }}" target="_blank">[PDF]</a>
      {% endif %}
  </li>
{% endfor %}
</ul>

<div id="more-papers" style="display:none;">
  <ul class="patent-list">
  {% for post in site.publications reversed offset:5 %}
    <li>
        {% if post.authors %}{{ post.authors }}. {% endif %}
        "<strong>{{ post.title }}</strong>." 
        <i>{{ post.venue }}</i>, 
        {{ post.date | date: "%Y" }}.
        {% if post.paper_level %}
          <span style="color: #d9534f; font-weight: bold; font-size: 0.85em;"> [{{ post.paper_level }}]</span>
        {% endif %}
        {% if post.paperurl %}
          <a href="{{ post.paperurl }}" target="_blank">[PDF]</a>
        {% endif %}
    </li>
  {% endfor %}
  </ul>
</div>

<button id="btn-papers" class="show-more-btn" onclick="toggleSection('more-papers', 'btn-papers')">展开全部 (Show All)</button>