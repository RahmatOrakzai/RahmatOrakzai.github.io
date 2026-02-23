---

layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
--------------------

{% include base_path %}

My research focuses on **non-invasive biomedical sensing, artificial intelligence for healthcare, and intelligent monitoring systems**, with applications in neurodegenerative disease assessment, computational imaging, and human activity analysis.

You can also view my publications on
[Google Scholar](https://scholar.google.com.pk/citations?user=r3q7Re0AAAAJ)

---

## ⭐ Selected Publications

{% for post in site.publications reversed %}
{% if post.highlight == true %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## 🎓 Thesis

{% for post in site.publications reversed %}
{% if post.type == "thesis" %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## Journal Articles

{% for post in site.publications reversed %}
{% if post.type == "journal" %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## Conference Papers

{% for post in site.publications reversed %}
{% if post.type == "conference" %}
{% include archive-single.html %}
{% endif %}
{% endfor %}
