---
layout: home
author_profile: true
---

## 📰 Ultime News
{% for articolo in site.news limit:3 %}
- [{{ articolo.title }}]({{ articolo.url }})  
  *{{ articolo.excerpt }}*
{% endfor %}

## 🎮 Ultime Recensioni
{% for articolo in site.recensioni limit:3 %}
- [{{ articolo.title }}]({{ articolo.url }})  
  *{{ articolo.excerpt }}*
{% endfor %}

## 📘 Ultime Guide
{% for articolo in site.guide limit:3 %}
- [{{ articolo.title }}]({{ articolo.url }})  
  *{{ articolo.excerpt }}*
{% endfor %}
