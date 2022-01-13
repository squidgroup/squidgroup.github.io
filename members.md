---
layout: page
title: Members
permalink: /members/
---

<div class="members">
  {% for member in site.members %}
  <div class="member">
    <div class="container">
    
      <img alt="Member photo" src="{{ site.images_path | relative_url }}members/{{ member.photo }}" onerror="this.onerror=null; this.src='{{ site.images_path | relative_url }}squid_logo.png'">
    
      <h3>
        <!-- <a href="{{ member.url | prepend: site.baseurl }}"> -->
          {{ member.name }}
        <!-- </a> -->
      </h3>
      <!-- <p>{{ member.content | markdownify }}</p> -->
      
      <div class="links">
      
        {%- if member.googlescholar -%}
          <a href="{{ member.googlescholar }}" target="_blank">
            <i class="ai ai-google-scholar"></i>
          </a>
        {%- endif -%}
        
        {%- if member.researchgate -%}
          <a href="{{ member.researchgate }}" target="_blank">
            <i class="ai ai-researchgate"></i>
          </a>
        {%- endif -%}
      
        {%- if member.github -%}
          <a href="{{ member.github }}" target="_blank">
            <i class="fab fa-github"></i> 
          </a>
        {%- endif -%}
        
        {%- if member.twitter -%}
          <a href="{{ member.twitter }}" target="_blank">
            <i class="fab fa-twitter"></i>
          </a>
        {%- endif -%}
        
        
      </div>
      
    </div> 
  </div>
  {% endfor %}
</div>