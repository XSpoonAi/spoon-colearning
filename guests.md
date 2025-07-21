---
layout: default
title: Lecture Guests
nav_order: 2
---

## Lecture Guests

<div class="staff-grid">
{% assign all_guests = site.staffers | sort: "index" %}
{% for staffer in all_guests %}
  <div class="staff-card">
    <img src="{{ staffer.picture }}" alt="{{ staffer.name }}" />
    <p>
      <strong><a href="{{ staffer.external_url }}" target="_blank">{{ staffer.name }}</a></strong><br>
      {{ staffer.role }}<br>
      <em>{{ staffer.email }}</em>
    </p>
  </div>
{% endfor %}
</div>

