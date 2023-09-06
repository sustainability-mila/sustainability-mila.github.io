---
layout: page-floatbutton
title: Team
permalink: /team
---
The Mila GFN Workshop is organized by volunteer students and friends from [Mila](https://mila.quebec) interested in GFlowNets and its applications to science and technology.

{% assign people = site.data.team | sample: site.data.team.size %}
{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}
    {% if side == 0 %}
      {% include team-card.html %}
    {% else %}
      {% include team-card.html %}
    {% endif %}
{% endfor %}
