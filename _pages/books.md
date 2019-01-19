---
title: "Books"
layout: archive
permalink: /books/
collection: books
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
 {% if collection.label == 'books' %}
  {% for post in collection.docs %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

