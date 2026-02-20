---

title: "Publications"
permalink: /publications/
author_profile: true
--------------------

{% include base_path %}

# Publications

My research focuses on **non-invasive biomedical sensing, artificial intelligence for healthcare, and intelligent monitoring systems**, with applications in neurodegenerative disease assessment and medical signal analysis.

You can also view my publications on
[Google Scholar](https://scholar.google.com/)

---

## ⭐ Selected Publications

{% for post in site.publications reversed %}
{% if post.highlight == true %}
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
