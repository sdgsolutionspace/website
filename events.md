---
layout: page
title: events
lang: en
ref: events
permalink: /events/
---

**Current Time (Geneva):** {{site.time}}

# ongoing

{% for p in site.pages %}
  {% if p.layout == page.title and p.starts < site.time and p.ends > site.time %}{{ p.title }}{% endif %}
{% endfor %}

# upcoming events

{% for p in site.pages %}
  {% if p.layout == page.title and p.starts > site.time %}{{ p.title }}{% endif %}
{% endfor %}


# past events

{% for p in site.pages %}
  {% if p.layout == page.title and p.ends < site.time %}{{ p.title }}{% endif %}
{% endfor %}
