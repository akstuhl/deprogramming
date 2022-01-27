---
layout: default
title: Workshop meeting plans
---

{% for item in site.meeting %}

### [{{ item.title }}]({{ item.url }})

{% if item.content-in-list %}
{{ item.content | markdownify }}
{% endif %}

{% endfor %}
