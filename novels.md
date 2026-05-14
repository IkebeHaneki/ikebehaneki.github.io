---
layout: default
title: Web Novels
---

# Web Novels / 网文小说

这里会记录一些网文小说相关内容。

可能包括：

- 最近在看的小说
- 喜欢的角色
- 剧情感想
- 推荐和吐槽

## Posts in Web Novels

{% assign novel_posts = site.posts | where_exp: "post", "post.categories contains 'novels'" %}

{% if novel_posts.size > 0 %}
{% for post in novel_posts %}
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
No web novel posts yet.
{% endif %}
