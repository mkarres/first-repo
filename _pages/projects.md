---
title: "Projects"
layout: archive
permalink: /projects/
collection: projects
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---

Various projects 

{% for collection in site.collections %}
 {% if collection.label == 'projects' %}
  {% for post in collection.docs %}
    {% unless collection.output == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

