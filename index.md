<div class="hero">
  <p class="hero-kicker">Haneki's Personal Space ✦</p>

  <h1>Welcome to Haneki's Space</h1>

  <p class="hero-text">
    这里是一个记录日常、学习笔记、游戏、网文小说和一些突然想到的事情的小站。
  </p>

  <p class="hero-text">
    希望它能慢慢变成一个有生活痕迹、也有一点个人风格的地方。
  </p>
</div>

## Categories 分类

- [🌸 Blog / 所有文章](blog.html)
- [☁️ Life / 日常](life.html)
- [📘 Notes / 学习笔记](notes.html)
- [🎮 Games / 游戏](games.html)
- [📖 Web Novels / 网文小说](novels.html)
- [✨ Random Thoughts / 随想](random.html)
- [🫧 About Me / 关于我](about.html)
  
## Latest Blog 最新的

{% assign latest_post = site.posts.first %}

{% if latest_post %}
<div class="post-card">
  <div class="post-card-title">
    <a href="{{ latest_post.url | relative_url }}">{{ latest_post.title }}</a>
  </div>

  <div class="post-card-meta">
    {{ latest_post.date | date: "%Y-%m-%d" }}
    · Category: {{ latest_post.categories | join: ", " }}
  </div>

  <p>
    {{ latest_post.excerpt }}
  </p>

  <a class="read-more" href="{{ latest_post.url | relative_url }}">Read more</a>
</div>
{% else %}
No blog posts yet.
{% endif %}


## Recent Plan

我准备先把这个网站搭起来，然后慢慢加入文章、图片和项目记录
