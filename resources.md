---
title: Reference
permalink: /resources/
---


{% assign reference_types = "public|students" | split: "|" %}

{% for type in reference_types %}

{% if type == 'public' %}
### **For the general public**  

 {% elsif type == 'students' %}

<br>
### **For students and lab members**
{% endif %}

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains type %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div> 

{% endfor %}

