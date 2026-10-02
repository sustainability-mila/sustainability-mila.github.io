---
layout: page
title: Team
permalink: /team
---
Meet the amazing organisers of the Mila Sustainability Reading Group, in random order!

{% assign current_people = site.data.team | where: "current", true %}
{% assign past_people = site.data.team | where: "current", false %}

<div class="columns container">
  <div class="column is-one-fifth"></div>
  <div class="column">
    <h2 class="title is-3">Current Members</h2>
  </div>
  <div class="column is-one-fifth"></div>
</div>

{% assign people = current_people | sample: current_people.size %}

{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}

  {% if side == 0 %}
    {% include team-card.html %}
  {% else %}
    {% include team-card.html %}
  {% endif %}
{% endfor %}

<div class="columns container">
  <div class="column is-one-fifth"></div>
  <div class="column">
    <h2 class="title is-3">Past Members</h2>
  </div>
  <div class="column is-one-fifth"></div>
</div>

{% assign people = past_people | sample: past_people.size %}

{% for person in people %}
  {% assign side = forloop.index0 | modulo: 2 %}

  {% if side == 0 %}
    {% include team-card.html %}
  {% else %}
    {% include team-card.html %}
  {% endif %}
{% endfor %}
