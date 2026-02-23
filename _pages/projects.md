---

layout: archive
title: "Research Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

My research projects focus on artificial intelligence, computational imaging, and digital health technologies, with applications in neurodegenerative disease monitoring, assistive technologies, and intelligent sensing systems.

---

{% assign projects_sorted = site.projects | sort: "date" | reverse %}

{% for post in projects_sorted %}

## {{ post.title }}

{{ post.excerpt }}

{{ post.content }}

---

{% endfor %}
