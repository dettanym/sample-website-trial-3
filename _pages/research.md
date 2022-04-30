---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<ol>
{% for post in site.research reversed %}
{% include common-formatting.html post=post %}
{%endfor%}

</ol>