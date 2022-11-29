---
layout: tab
---
<center>
<div class="card shadow p-3 mb-5 black col-md-7">
<h4 class="focus">Blog</h4>
</div>
{% for post in site.posts %}
  <div class="card black shadow-lg p-3 mb-5 col-md-8 focus" style="margin-left: 50px;">
    <div class="card-title">
      {{ post.title }}
    <div class="nd">
      Blog Post No. {{ post.number }}
      <br>
      Date: {{ post.date | date_to_string }}
    </div>
    {% if post.image %}
      <img src="{{ post.image }}" class="media rounded-circle" style="opacity: 0.8; margin-top: 15px;">
      {% endif %}
    </div>
    <div class="card-body">
      {{post.content}}
    </div>
  </div>
{% endfor %}
</center>
<br>