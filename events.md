---
layout: page
title: events
lang: en
ref: events
permalink: /events/
---

**Current Time (Geneva):** {{site.time | date: '%Y.%m.%d, %H:%M' }}

If you are interested in organizing an event at the SDG Solution Space, please fill-in this [form](https://docs.google.com/forms/d/e/1FAIpQLScQVAmSmWTn9zzS5PFLq-tqiIK6JpdDYKAx_dD3zHlU-6Ec5g/viewform?usp=sf_link).

We will answer you as soon as possible.

## ongoing

{% for p in site.events %}
  {% if p.layout == page.title and p.starts < site.time and p.ends > site.time %}
<p><h4>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }}</h4></p>
	{% if {{p.url_address | size }} != 0  %}
<p><a href="{{p.url_address}}">{{p.title}}</a></p>
	{% else %}
<p>{{p.title}}</p>
	{% endif %}
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}



## upcoming events

{% for p in site.events %}
  {% if p.layout == page.title and p.starts > site.time %}
<p><h4>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }}</h4></p>
	{% if {{p.url_address | size }} != 0  %}
<p><a href="{{p.url_address}}">{{p.title}}</a></p>
	{% else %}
<p>{{p.title}}</p>
	{% endif %}
      {% if post.excerpt %}
          {{ post.excerpt }}
      {% endif %}
    {% endif %}
{% endfor %}


## past events

{% for p in site.events %}
  {% if p.layout == page.title and p.ends < site.time %}
<p><h4>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }}</h4></p>
	{% if {{p.url_address | size }} != 0  %}
<p><a href="{{p.url_address}}">{{p.title}}</a></p>
	{% else %}
<p>{{p.title}}</p>
	{% endif %}
	{%if p.description and p.description != blank %}{{p.description}}
	{% endif %}
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}
