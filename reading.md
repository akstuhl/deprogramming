---
layout: default
title: Recommended readings
---

<p class='bulletin'>📢&nbsp;&nbsp;Registered workshop participants: please refer to your email for readings that do not have open-access links here.</p>

{% for item in site.reading %}
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
