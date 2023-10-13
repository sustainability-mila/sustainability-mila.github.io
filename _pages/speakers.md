---
title: Speakers
layout: page
permalink: /speakers
---
{% assign speakers = site.data.speakers | sort: "date" %}
{% for speaker in speakers %}
  {% if speaker.skip %}{% continue %}{% endif %}
    {% assign side = forloop.index0 | modulo: 2 %}
      {% if side == 0 %}
        {% include speaker-card.html %}
      {% else %}
        {% include speaker-card.html %}
      {% endif %}
{% endfor %}
