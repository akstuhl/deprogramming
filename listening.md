---
layout: default
title: Listening syllabus
---

{% assign reversed = site.listening | sort: "year" | reverse %}
{% assign sorted = reversed | sort: "pin" | reverse %}
{% for item in sorted %}
<div class="item-heading">

  <span class="item-anchor">
    <a href="#{{ item.title | slugify }}">#</a>
  </span>
  <h3 id="{{ item.title | slugify }}">{{ item.title }}</h3>
  <span class="item-meta">
    {{ item.creator }} · {{ item.year }}
    {% if item.link-url %}
    <a href="{{ item.link-url }}" target="_blank" class="item-link">↗</a>
    {% endif %}
  </span>

</div>

{{ item.content | markdownify }}

{% endfor %}
