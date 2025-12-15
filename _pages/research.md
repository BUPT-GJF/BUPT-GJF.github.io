---
layout: archive
title: "科学研究"
permalink: /research/
author_profile: true
---

{% include base_path %}

## 1. 研究领域 (Research Areas)

智算融合网络、智慧协同网络、智慧路由、异质异构网络安全。

---

## 2. 科研项目 (Research Projects)

* 智算融合网络异构资源弹性适配机制，进行，许长桥

* 糖尿病肾病的“疾病-症候-症状关联”的临床评价指标体系与技术规范数据库的建立及挖掘，结项，关建峰

* 认知互联网体系结构与服务模型研究，结项，关建峰

* 未来移动互联网的流媒体认知传输控制协议研究，结项，许长桥

* 智慧协同的绿色移动流媒体服务研究，结项，许长桥

---

## 3. 发明专利 (Patents)

{% for post in site.patents reversed %}
  * **[{{ post.title }}]({{ post.url }})**
{% endfor %}

---

## 4. 著作成果 (Books)

{% for post in site.books reversed %}
  * **[{{ post.title }}]({{ post.url }})**
{% endfor %}
---

## 5. 论文成果 (Publications)


{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}