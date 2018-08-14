---
title: Publications
permalink: /pages/pub/
---

<div>
{% assign sorted = site.categories.publication | sort: 'date' | reverse %}
{% for post in sorted %}
  {% if post.work-type == 'Paper' %}
    <h2>{{ post.title }} ({{ post.ref-year }})</h2>
    <p>
    {{ post.ref-authors }}. 
    <em>{{ post.ref-journal}}</em>,
    {% if post.ref-volume %} {{ post.ref-volume }}{% endif %}
    {% if post.ref-number %}({{ post.ref-number }}){% endif %}{% if post.ref-pages %}, {{ post.ref-pages }}{% endif %}.  
    {% if post.ref-doi %}
      <a href="http://dx.doi.org/{{ post.ref-doi }}">
        doi: {{ post.ref-doi }}
      </a>
    {% endif %}
    </p>
  {% endif %}
{% endfor %}
</div>
