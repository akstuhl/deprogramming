---
layout: default
title: "Deprogramming: micro-interventions for media-makers"
---

{% include stream.html %}

This stream features our workshop participants' interpretations of each other's prompts, along with the recordings from [Radio Naked](listening.html#radio-naked) in a randomized order. It plays on a [π-box](https://p-node.org/documentation/pibox/what-is-a-pibox).
{: .stream-footer }

<div class='prompts'>

  {% assign randomized = site.data.prompts | sample: 53 %}
  {% for prompt in randomized %}

    <div class='prompt'>
      <span class='prompt-meta'>{{ prompt.Author }}</span>
      <span class='prompt-meta'>{{ prompt.Medium}}</span>

      <p>{{ prompt.Text }}</p>
    </div>

  {% endfor %}

</div>
