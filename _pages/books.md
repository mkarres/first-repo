---
title: "Books"
layout: archive
permalink: /books/
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
 {% if collection.label == 'books' %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% capture label %}{{ collection.label }}{% endcapture %}
    {% if label != written_label %}
      <h2 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h2>
      {% capture written_label %}{{ label }}{% endcapture %}
    {% endif %}
  {% endunless %}
  {% for post in collection.docs %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

