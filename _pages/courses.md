---
title: "Courses"
layout: archive
permalink: /courses/
collection: courses
author_profile: true
header:
  image: "/images/queenstown.jpg"
---

Notes and workbooks for online courses

{% for collection in site.collections %}
 {% if collection.label == 'courses' %}
  {% for post in collection.docs %}
    {% unless collection.output == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

