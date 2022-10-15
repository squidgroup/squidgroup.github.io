---
layout: page
permalink: /members/
---

<div class="member-page">

  <h1 class="post-title">Current members</h1>
  <div class="member-container">
    {% for member in site.members %}
      {%- if member.type == "current" -%}
        {%- include member_card.html -%}
      {%- endif -%}
    {% endfor %}
  </div>
  
  
  <!---
  <hr class="rounded">

  <h1 class="post-title">Founding members</h1>
  <div class="member-container">
    {% for member in site.members %}
      {%- if member.type == "founder" -%}
        {%- include member_card.html -%}
      {%- endif -%}
    {% endfor %}
  </div>
  --->
  
  <hr class="rounded">
  
  <h1 class="post-title">Involved along the way</h1>
  <div class="member-container">
    {% for member in site.members %}
      {%- if member.type == "previous" -%}
        {%- include member_card.html -%}
      {%- endif -%}
    {% endfor %}
  </div>

</div>