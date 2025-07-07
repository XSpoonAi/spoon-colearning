---
layout: default
title: Lecture Guests
nav_order: 2
---

# Lecture Guests

<div style="display: flex; flex-wrap: wrap; gap: 40px; justify-content: center; margin-top: 2rem;">

{% assign sorted_guests = site.staffers | sort: "index" %}
{% for guest in sorted_guests %}
  <div style="text-align: center; width: 240px;">
    <img src="{{ site.baseurl }}/{{ guest.picture }}" alt="{{ guest.name }}" style="border-radius: 50%; width: 120px; height: 120px; object-fit: cover; box-shadow: 0 0 6px rgba(0,0,0,0.2); margin-bottom: 10px;">
    <p><a href="{{ guest.url }}" style="font-weight: bold; font-size: 16px;">{{ guest.name }}</a></p>
    <p style="margin: 0;">{{ guest.role }}</p>
    <p style="font-style: italic;">{{ guest.email }}</p>
  </div>
{% endfor %}

</div>
