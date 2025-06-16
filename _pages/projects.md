---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## Current Projects
{% for post in site.projects reversed %}
  {% if post.project_duration contains 'Present' %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Past Projects
{% for post in site.projects reversed %}
  {% unless post.project_duration contains 'Present' %}
    {% include archive-single.html %}
  {% endunless %}
{% endfor %}
