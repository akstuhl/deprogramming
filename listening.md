---
layout: default
title: Listening syllabus
---

{% include stream.html %}

This stream, for now, features selections from the listening syllabus in random order. It plays on a [π-box](https://p-node.org/documentation/pibox/what-is-a-pibox).
{: .stream-footer }

{% assign reversed = site.listening | reverse %}
{% assign sorted = reversed | sort: "pin" | reverse %}
{% for item in sorted %}
<div class="item-heading">

  <span class="item-anchor">
    <a href="#{{ item.title | slugify }}">#</a>
  </span>
  <h3 id="{{ item.title | slugify }}">{{ item.title }}</h3>
  <span class="item-meta">
    {{ item.creator }}&nbsp;·&nbsp;{{ item.year }}
    {% if item.link-url %}
    <a href="{{ item.link-url }}" target="_blank" class="item-link">↗</a>
    {% endif %}
  </span>

</div>

{{ item.content | markdownify }}

{% endfor %}
