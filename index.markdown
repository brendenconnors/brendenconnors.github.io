---
layout: home
---

Hello! Welcome to my website. I will be using this to share various things that I have done that I think are interesting or helpful to others!
This is a WIP, so bear with me while I things get filled out. 


{% for p in site.collections %}
{% if p.label != "posts" %}
   <h1>{{p.label | capitalize | replace: "_", " "}}</h1>
{% endif %}
<ul>
{% for page in site[p.label] %}
   <li><a href="{{site.url}}{{page.url}}">{{page.title}}</a></li>
{% endfor %}
</ul>
{% endfor %}

