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
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{{ post.excerpt }}

[Read more]({{ post.url | relative_url }})

---
{% endfor %}
{% else %}
No web novel posts yet.
{% endif %}
