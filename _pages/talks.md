## Conference Presentations

{% assign conf = site.talks | where: "type", "conference" | sort: "date" | reverse %}
{% for post in conf %}
**{{ post.title }}**  
{{ post.venue }} — {{ post.location }}  
*{{ post.date | date: "%B %-d, %Y" }}*  
{{ post.excerpt | default: post.content | markdownify }}
---
{% endfor %}

## Invited Talks and Guest Lectures

{% assign invited = site.talks | where: "type", "invited" | sort: "date" | reverse %}
{% for post in invited %}
**{{ post.title }}**  
{{ post.venue }} — {{ post.location }}  
*{{ post.date | date: "%B %-d, %Y" }}*  
{{ post.excerpt | default: post.content | markdownify }}
---
{% endfor %}
