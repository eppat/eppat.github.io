---
layout: home
title: Benvenuti su Il Mio Sito di Videogiochi
---

# 📰 News
{% for articolo in site.news %}
- [{{ articolo.title }}]({{ articolo.url }})
{% endfor %}

# 🎮 Recensioni
{% for articolo in site.recensioni %}
- [{{ articolo.title }}]({{ articolo.url }})
{% endfor %}

# 📘 Guide
{% for articolo in site.guide %}
- [{{ articolo.title }}]({{ articolo.url }})
{% endfor %}
