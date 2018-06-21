---
layout: page
title: SDG Fablab
lang: en
ref: fablab
permalink: /fablab/
---



<br>
<img src="/pages/fablab/sdgfablab.jpg" alt=""  width="15%">
<br>

# **SDG Fablab**

#### **You wish to save the world and this requires that you build a prototype?**

The **SDG Fablab** located at the heart of the International Organizations neighborhood in Geneva is the right place for you !

The SDG Fablab is located within the [SDG Solution Space](https://sdgsolutionspace.org), on the [Campus Biotech](https://http://campusbiotech.ch/){:target="_blank"} premises, and welcomes people and projects that are directly concerned with the practical implementation of the [United Nations Sustainable Development Goals (SDG).](https://www.un.org/sustainabledevelopment/sustainable-development-goals/){:target="_blank"}

Not only you have access to cutting-edge equipment (CNC Milling Machine, Laser Cutter, 3D printer, 3D scanner, Electronics & Soldering Gear), but you will have a chance to interact with a vivid community of [UNIGE](https://unige.ch){:target="_blank"} [Master Students](www.unige.ch/sciences-societe/formations/masters/innovation-human-development-and-sustainability/){:target="_blank"}, [Summer School Students](http://www.gt-initiative.org/en/summer-school.html){:target="_blank"}. In addition, you may bump into representatives and collaborators of the United Nations and International Organizations, who hand out regularly at the [SDG Solution Space](https://sdgsolutionspace.org).

<br>
#### **You want to build a prototype, but you don't know how to use a 3D printer or a Laser Cutter ?**

As part of the the [Geneva-Tsinghua Initiative](https://gt-initiative.org){:target="_blank"}, the **SDG Fablab** has an education mandate. Provided that
1. you are motivated, self-reliant,
2. you wish to pursue the achievement of a project/prototype with positive and scalable positive impact related to the SDGs,
3. you are willing to share publicly your learning experience and in turn help others on their learning path,

we are happy to help you. For further information, [please get in touch with us](mailto:fablab@sdgsolutionspace.org){:target="_blank"}.

<br>
#### **SDG Fablab is part of a large network of fablabs**

Check out our page on [fablab.io](https://www.fablabs.io/labs/sdgsolutionspace){:target="_blank"}.

<br>

---

# **Recent Makes**

{% for item in site.posts %}

{% for cat in item.categories %}
{% if cat == "fablab" %}<p><h4><a href="{{item.url}}">{{ item.title}}</a> | {{ item.date | date: "%b %-d, %Y" }}</h4></p>
{{ item.excerpt }}
{% endif %}
<!--- <h4><a href="{{item.url}}">{{ item.title}}</a></h4> -->

{% endfor %}
{% endfor %}
