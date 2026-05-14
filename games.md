---
layout: default
title: Games
---

# Games / 游戏

这里会记录一些游戏相关内容。

可能包括：

- 玩过的游戏
- 游戏体验
- 游戏截图
- 角色 / 剧情感想
- 一些随便的吐槽

## Posts in Games

{% assign game_posts = site.posts | where_exp: "post", "post.categories contains 'games'" %}

{% if game_posts.size > 0 %}
{% for post in game_posts %}
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
No game posts yet.
{% endif %}
