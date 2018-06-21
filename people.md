---
layout: default
title: people
lang: en
ref: people
permalink: /people/
---

## People

### **Master of Innovation, Human Development and Sustainability**

{% for item in site.people %}
<!--- <h4><a href="{{item.url}}">{{ item.title}}</a></h4> -->
{% for cat in item.categories %}
{% if cat == "students" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>{% endif %}
{% endfor %}
{% endfor %}


<br>
### **High School Students**

{% for item in site.people %}
<!--- <h4></h4> -->
{% for cat in item.categories %}
{% if cat == "highschoolers" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>{% endif %}
{% endfor %}
{% endfor %}


<br>
### **Teachers**

{% for item in site.people %}
<!--- <h4></h4> -->
{% for cat in item.categories %}
{% if cat == "teachers" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>{% endif %}
{% endfor %}
{% endfor %}

<br>
### **Fablab**

{% for item in site.people %}
<!--- <h4><a href="{{item.url}}">{{ item.title}}</a></h4> -->
{% for cat in item.categories %}
{% if cat == "fablab" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a></h4></p>{% endif %}
{% endfor %}
{% endfor %}
