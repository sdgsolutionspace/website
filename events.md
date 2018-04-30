---
layout: page
title: events
lang: en
ref: events
permalink: /events/
---

**Current Time (Geneva):** {{site.time | date: '%Y.%m.%d, %H:%M' }}

Please note that until the end of June 2018, the SDG Solution Space is available for booking on Mondays and Wednesdays full days, and on Tuesdays, Thursdays and Fridays from 6PM.

If you are interested in organizing an event at the SDG Solution Space, please fill-in this [form](https://docs.google.com/forms/d/e/1FAIpQLScQVAmSmWTn9zzS5PFLq-tqiIK6JpdDYKAx_dD3zHlU-6Ec5g/viewform?usp=sf_link).
Please understand that filling the form brings no guarantee the SDG Solution Space will be available for your event, even in case of prior contact.
We will answer you on a best-effort basis, please be patient.

## Ongoing events

{% for p in site.events %}
  {% if p.layout == page.title and p.starts < site.time and p.ends > site.time %}
<p>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }} - {{ p.ends | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' | slice: 11, 16 | append: ' : ' }}
	{% if {{p.url_address | size }} != 0  %}
<a href="{{p.url_address}}">{{p.title | truncatewords: 6 }}</a></p>
	{% else %}
{{p.title | truncatewords: 6 }}</p>
	{% endif %}
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}


## Upcoming events

{% for p in site.events %}
  {% if p.layout == page.title and p.starts > site.time %}
<p>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }} - {{ p.ends | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' | slice: 11, 16 | append: ' : ' }}
	{% if {{p.url_address | size }} != 0  %}
<a href="{{p.url_address}}">{{p.title | truncatewords: 6 }}</a></p>
	{% else %}
{{p.title | truncatewords: 6 }}</p>
	{% endif %}
      {% if post.excerpt %}
          {{ post.excerpt }}
      {% endif %}
    {% endif %}
{% endfor %}


## Past events

{% for p in site.events %}
  {% if p.layout == page.title and p.ends < site.time %}
<p>{{ p.starts | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' }} - {{ p.ends | remove: "+0100" | remove: "+0200" | replace_first: ':00', '' | slice: 11, 16 | append: ' : ' }}
	{% if {{p.url_address | size }} != 0  %}
<a href="{{p.url_address}}">{{p.title | truncatewords: 6 }}</a></p>
	{% else %}
{{p.title | truncatewords: 6 }}</p>
	{% endif %}
	{%if p.description and p.description != blank %}{{p.description}}
	{% endif %}
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}
