---
title:
permalink: /pages/people/
---

<div style="display:table; vertical-align:top">
{% for author in site.data.people %}
  {% include multi-author-profile.html %}
{% endfor %}
</div>

## Alumni
<div style="display:table; vertical-align:top">
{% assign alumnibyrole = site.data.alumni | group_by:"role" %}
{% for role in alumnibyrole %}
  <section id="{{ role.name }}" class="taxonomy__section">
    <h2 class="archive__subtitle">{{ role.name }}</h2>
    <div>
      {% for alum in role.items %}
        <strong>{{ alum.name }}</strong>{% if alum.current %}, now at {{ alum.current }}{% endif %}<br>  
      {% endfor %}
    </div>
  </section>
{% endfor %}
</div>


