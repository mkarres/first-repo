---
title: "Deep Learning"
layout: archive 
permalink: /deep-learning/
collection: deeplearning
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---

Notes about Deep Learning

{% for collection in site.collections %}
 {% if collection.label == 'deeplearning' %}
  {% for post in collection.docs %}
    {% unless collection.output == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

