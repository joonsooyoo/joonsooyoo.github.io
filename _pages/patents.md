---
layout: archive
title: "Patents"
permalink: /patents/
author_profile: true
---

{% if site.patent_category %}
  {% for category in site.patent_category %}
    {% assign title_shown = false %}
    {% for post in site.patents reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
<h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.patents reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
