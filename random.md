---
layout: default
title: Random Thoughts
---

# Random Thoughts / 随想

这里会放一些比较随意的想法
可能是一些短句、突然想到的事情、生活里的小观察，或者没有固定主题的记录。

## Random Posts

{% assign random_posts = site.posts | where_exp: "post", "post.categories contains 'random'" %}

{% if random_posts.size > 0 %}
{% for post in random_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}
{% else %}
No random posts yet.
{% endif %}
