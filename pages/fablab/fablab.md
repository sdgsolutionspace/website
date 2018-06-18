---
layout: page
title: SDG Fablab
lang: en
ref: fablab
permalink: /fablab/
---

# SDG Fablab

Description of the fablab to be added here.

### Recent Makes

{% for item in site.posts %}

{% for cat in item.categories %}
{% if cat == "fablab" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>
{{ item.excerpt }}
<br>
{% endif %}
<!--- <h4><a href="{{item.url}}">{{ item.title}}</a></h4> -->

{% endfor %}
{% endfor %}
