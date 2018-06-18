---
layout: page
title: projects
lang: en
ref: projects
permalink: /projects/
---

## Projects at SDG Solution Space

{% for item in site.projects %}
<!--- <h4><a href="{{item.url}}">{{ item.title}}</a></h4> -->
<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>
{{ item.excerpt }}
{% endfor %}
