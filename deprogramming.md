---
layout: default
title: "Deprogramming: micro-interventions for media-makers"
---

These short text prompts, along with their audio and video interpretations, are the products of our collaborative imagining in the Radio Deprogramming workshop. Deprogramming, we decided, can mean many things: disrupting routines, inverting diagrams, restoring relations to space, rupturing the ordinary, transporting while disorienting, flipping what's public and what's private in listening, offering footholds in the unscalable walls of communication systems, or perhaps dismantling the very medium-ness of a medium. The prompts are event scores, creative strategies, poetic ruptures, productive ambiguities, speculative fictions, project plans, and counter-imaginaries.
{: .prompts-intro }

<div class='prompts'>

  {% assign randomized = site.data.prompts | sample: 53 %}
  {% for prompt in randomized %}

    <div class='prompt'>
      <span class='prompt-meta'>{{ prompt.Author }}</span>
      <span class='prompt-meta'>{{ prompt.Medium}}</span>

      <p>{{ prompt.Text }}</p>

      {% if prompt.Audio2 == 'VIDEO' %}
      <span class='prompt-meta'>Video: {{ prompt.Audio1 }}</span>
      <video controls="controls">
        <source src="{{ prompt.AudioLink1 }}" type="video/mp4"></source>
      </video>
      {% else %}

        {% if prompt.AudioLink1 %}
        <span class='prompt-meta'>Audio: {{ prompt.Audio1 }}</span>
        <br />
        <audio controls="controls" preload="none">
          <source src="{{ prompt.AudioLink1 }}" type="audio/mpeg" ></source>
        </audio>
        <br />
        {% endif %}

        {% if prompt.AudioLink2 %}
        <span class='prompt-meta'>Audio: {{ prompt.Audio2 }}</span>
        <br />
        <audio controls="controls" preload="none">
          <source src="{{ prompt.AudioLink2 }}" type="audio/mpeg" ></source>
        </audio>
        <br />
        {% endif %}
      {% endif %}
    </div>

  {% endfor %}

</div>
