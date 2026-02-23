---

layout: archive
title: "Talks and Presentations"
permalink: /talks/
author_profile: true
--------------------

{% include base_path %}

My conference presentations and invited talks cover topics including artificial intelligence for healthcare, microwave sensing for biomedical applications, and software engineering.

---

## 🎤 Conference Presentations

{% assign conf = site.talks | where: "type", "conference" | sort: "date" | reverse %}

{% for post in conf %}
**{{ post.title }}**
{{ post.venue }} — {{ post.location }}
*{{ post.date | date: "%B %-d, %Y" }}*

{{ post.excerpt | default: post.content | markdownify }}

---

{% endfor %}

---

## 🎓 Invited Talks and Guest Lectures

{% assign invited = site.talks | where: "type", "invited" | sort: "date" | reverse %}

{% for post in invited %}
**{{ post.title }}**
{{ post.venue }} — {{ post.location }}
*{{ post.date | date: "%B %-d, %Y" }}*

{{ post.excerpt | default: post.content | markdownify }}

---

{% endfor %}
