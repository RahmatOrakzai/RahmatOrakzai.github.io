---

layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}

My teaching experience spans undergraduate and postgraduate education across software engineering, embedded systems, and computer science.

---

{% assign teaching_sorted = site.teaching | sort: "date" | reverse %}

{% for post in teaching_sorted %}

## {{ post.title }}

**{{ post.type }}**
{{ post.venue }}
{{ post.date | date: "%Y" }} — {{ post.location }}

{{ post.content }}

---

{% endfor %}
