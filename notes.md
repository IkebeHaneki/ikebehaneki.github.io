---
layout: default
title: Notes
---

# Notes / 学习笔记
这里会放一些学习笔记

## Posts in Notes

{% assign notes_posts = site.posts | where_exp: "post", "post.categories contains 'notes'" %}

{% if notes_posts.size > 0 %}
{% for post in notes_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}
{% else %}
No posts in this category yet.
{% endif %}
