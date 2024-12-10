<!--
 * @Author: error: error: git config user.name & please set dead value or install git && error: git config user.email & please set dead value or install git & please set dead value or install git
 * @Date: 2024-12-10 09:13:14
-->
---
title: Team
nav:
  order: 3
  tooltip: About our team
---

<!-- # {% include icon.html icon="fa-solid fa-users" %}Team
孙晓波生物信息实验室
{% include section.html %}
{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait" filter="role != 'pi'" %}
{% include section.html background="images/background.jpg" dark=true %}
硕士研究生
{% include section.html %}
{% capture content %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% endcapture %}
本科生
{% include section.html %}
{% capture content %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% endcapture %}
{% include grid.html style="square" content=content %} -->


# {% include icon.html icon="fa-solid fa-users" %}Team

孙晓波生物信息实验室

{% include section.html %}

## 实验室负责人

{% assign pi = site.data.members | where: "role", "pi" %}
{% for member in pi %}
  <div class="member">
    {% include figure.html image=member.photo alt=member.name %}
    <p>{{ member.name }}</p>
    <p>{{ member.description }}</p>
  </div>
{% endfor %}

## 合作伙伴

{% assign partners = site.data.members | where: "role", "partner" %}
<div class="partners">
  {% for member in partners %}
    <div class="partner">
      {% include figure.html image=member.photo alt=member.name %}
      <p>{{ member.name }}</p>
      <p>{{ member.description }}</p>
    </div>
  {% endfor %}
</div>

## 硕士研究生

{% assign grad_students = site.data.members | where: "role", "graduate_student" %}
<div class="grad-students">
  {% for member in grad_students %}
    <div class="member">
      {% include figure.html image=member.photo alt=member.name %}
      <p>{{ member.name }}</p>
      <p>{{ member.description }}</p>
    </div>
  {% endfor %}
</div>

## 本科生

{% assign undergrad_students = site.data.members | where: "role", "undergraduate_student" %}
<div class="undergrad-students">
  {% for member in undergrad_students %}
    <div class="member">
      {% include figure.html image=member.photo alt=member.name %}
      <p>{{ member.name }}</p>
      <p>{{ member.description }}</p>
    </div>
  {% endfor %}
</div>

## 已毕业学生

{% assign alumni = site.data.members | where: "role", "alumni" %}
<ul class="alumni">
  {% for member in alumni %}
    <li>{{ member.name }}</li>
  {% endfor %}
</ul>