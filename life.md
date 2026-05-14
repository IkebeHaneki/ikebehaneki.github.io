---
layout: default
title: Life
---
# Life / 日常

这里会记录一些日常生活。

可能包括校园生活、温哥华日常、旅行、吃到的东西、心情随笔，或者一些没有什么主题的碎碎念。

## Posts in Life

{% assign life_posts = site.posts | where_exp: "post", "post.categories contains 'life'" %}

{% if life_posts.size > 0 %}
{% for post in life_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}
{% else %}
No posts in this category yet.
{% endif %}
