---
layout: archive
title: "Teaching Assistance"
permalink: /teaching/
author_profile: true
---

{% include base_path %}
   You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u> 
{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}

