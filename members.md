---
layout: page
permalink: /members/
---

<h2>Founding members</h2>
<div class="member-container">
  {% for member in site.members %}
    {%- if member.type == "founder" -%}
      {%- include member_card.html -%}
    {%- endif -%}
  {% endfor %}
</div>

<h2>Current members</h2>
<div class="member-container">
  {% for member in site.members %}
    {%- if member.type == "current" -%}
      {%- include member_card.html -%}
    {%- endif -%}
  {% endfor %}
</div>

<h2>Involved along the way</h2>
<div class="member-container">
  {% for member in site.members %}
    {%- if member.type == "previous" -%}
      {%- include member_card.html -%}
    {%- endif -%}
  {% endfor %}
</div>