# Welcome to my Space
这里是我的个人博客，平时可能会在上面发一些无关紧要的东西，可能有学习，可能是一些无聊の日常
## About Me 关于我
我是一个目前在加拿大UBC就读数学本科的鼠鼠，对数据和编程有点兴趣（但不多），这个博客网站目前只是兴趣使然，我会放一些简历，学习类的东西在上面，但是更多的还是一些生活向的事情吧
## Categories

- [Life / 日常](life.html)
- [Notes / 学习笔记](notes.html)
- [Games / 游戏](games.html)
- [Web Novels / 网文小说](novels.html)
- [About Me / 关于我](about.html)
  
## Latest Blog

{% assign latest_post = site.posts.first %}

{% if latest_post %}
### [{{ latest_post.title }}]({{ latest_post.url | relative_url }})

{{ latest_post.date | date: "%Y-%m-%d" }}

Category: {{ latest_post.categories | join: ", " }}

{{ latest_post.excerpt }}

[Read more]({{ latest_post.url | relative_url }})
{% else %}
No blog posts yet.
{% endif %}


## Recent Plan

我准备先把这个网站搭起来，然后慢慢加入文章、图片和项目记录
