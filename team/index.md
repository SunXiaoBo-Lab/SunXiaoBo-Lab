---
title: Team
nav:
  order: 3
  tooltip: About our team
---
<!-- 包含用户图标 -->
{% include icon.html icon="fa-solid fa-users" %}

<!-- 团队名称 -->
<h1>孙晓波生物信息实验室</h1>

<!-- 包含额外的HTML内容 -->
{% include section.html %}

<!-- 显示PI成员 -->
<h2>Principal Investigator (PI)</h2>
{% include list.html data="members" component="portrait" filter="role == 'pi'" %}

<!-- 显示硕士研究生 -->
<div class="students-split">
  <div class="Master">
    <h3>Master</h3>
    {% include list.html data="members" component="portrait" filter="description == 'Master'" %}
  </div>

  <!-- 显示本科生 -->
  <div class="Undergraduate">
    <h3>Undergraduate</h3>
    {% include list.html data="members" component="portrait" filter="description == 'Undergraduate'" %}
  </div>
</div>

<!-- # {% include icon.html icon="fa-solid fa-users" %}Team

孙晓波生物信息实验室

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
<!-- {% include list.html data="members" component="portrait" filter="role != 'pi'" %} -->

<!-- {% include section.html background="images/background.jpg" dark=true %} -->

<!-- Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{% include section.html %}

{% capture content %}

{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %} -->