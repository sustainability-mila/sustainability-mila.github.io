---
layout: page-floatbutton
title: Team
permalink: /team
---
Meet the wonderful organisers of the Mila Sustainability Reading Group, in random order!

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
