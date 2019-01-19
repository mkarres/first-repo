---
title: "Books"
layout: archive
permalink: /books/
collection: books
author_profile: true
header:
  image: "/images/highSierraTrail.jpg"
---

Reviews and worksheets for books that I've read

{% for collection in site.collections %}
 {% if collection.label == 'books' %}
  {% for post in collection.docs %}
    {% unless collection.output == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
 {% endif %}
{% endfor %}

