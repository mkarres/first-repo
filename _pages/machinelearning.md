---
title: "Machine Learning"
layout: archive 
permalink: /machine-learning/
collection: machinelearning
author_profile: true
header:
  image: "/images/disneySea.jpg"
---

Notes about Machine Learning

{% for collection in site.collections %}
 {% if collection.label == 'machinelearning' %}
  {% for post in collection.docs %}
    {% unless collection.output == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

