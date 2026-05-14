---
layout: default
title: Blog
---

# Blog / 所有文章

这里会显示我发布过的所有博客。你可以根据分类筛选文章。

<div class="filter-buttons">
  <button onclick="filterPosts('all')">All</button>
  <button onclick="filterPosts('life')">Life / 日常</button>
  <button onclick="filterPosts('notes')">Notes / 学习笔记</button>
  <button onclick="filterPosts('projects')">Projects / 项目记录</button>
  <button onclick="filterPosts('games')">Games / 游戏</button>
  <button onclick="filterPosts('novels')">Web Novels / 网文小说</button>
  <button onclick="filterPosts('random')">Random Thoughts / 随想</button>
</div>

<br>

<div id="post-list">

{% for post in site.posts %}
<div class="post-item" data-category="{{ post.categories | join: ' ' }}">
  <h2>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </h2>

  <p>
    <strong>Date:</strong> {{ post.date | date: "%Y-%m-%d" }}
  </p>

  <p>
    <strong>Category:</strong> {{ post.categories | join: ", " }}
  </p>

  <p>
    {{ post.excerpt }}
  </p>

  <hr>
</div>
{% endfor %}

</div>

<script>
function filterPosts(category) {
  const posts = document.querySelectorAll('.post-item');

  posts.forEach(post => {
    const categories = post.getAttribute('data-category');

    if (category === 'all' || categories.includes(category)) {
      post.style.display = 'block';
    } else {
      post.style.display = 'none';
    }
  });
}
</script>
