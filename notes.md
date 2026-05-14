---
layout: default
title: Notes
---

# Notes / 学习笔记

这里会放一些学习笔记。

可能包括：

- Mathematics
- Statistics
- Linear Programming
- Data Science
- Programming

## Posts in Notes

{% assign notes_posts = site.posts | where_exp: "post", "post.categories contains 'notes'" %}

{% if notes_posts.size > 0 %}
{% for post in notes_posts %}
<div class="post-card">
  <div class="post-card-title">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </div>

  <div class="post-card-meta">
    {{ post.date | date: "%Y-%m-%d" }}
  </div>

  <p>
    {{ post.excerpt }}
  </p>

  <a class="read-more" href="{{ post.url | relative_url }}">Read more</a>
</div>
{% endfor %}
{% else %}
No posts in this category yet.
{% endif %}
