---
layout: tab
---
<center>
<div class="card shadow p-3 mb-5 black col-md-7">
<h4>Blog</h4>
</div>
</center>
{% for post in site.posts) %}
  {% assign remainder = forloop.index0 | modulo: 3 %}
  {% if remainder == 0 and forloop.index0 != 1 %}
  </div>
  {% endif %}
  {% if remainder == 0 %}
  <div class="row"> 
  {% endif %}
  {% if remainder == 1 %}
  <div class="card black shadow-lg p-3 mb-5 col-md-4" style="margin-left: 50px;">
  {% else %}
  <div class="card black shadow-lg p-3 mb-5 col-md-3" style="margin-left: 50px;">
  {% endif %}
    <div class="card-title">
      {{ post.title }}
      {% if post.image %}
      <img src="{{ post.image }}" class="media rounded-circle" style="float: right; opacity: 0.8">
      {% endif %}
    <div class="nd">
      Blog Post No. {{ post.number }}
      <br>
      Date: {{ post.date | date_to_string }}
    </div>
    </div>
    <div class="card-body">
      {{post.content}}
    </div>
  </div>
{% endfor %}
<br>
