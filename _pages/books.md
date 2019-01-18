---
layout: posts
permalink: /books/
title: "Notebooks"
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---
Here are my notes and exercises from fun workbooks 

{% include base_path %}
{% assign base_path = base_path | append: permalink %}
{% include group-by-array collection=site.books field="tags" %}

#{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
#{% endfor %}
