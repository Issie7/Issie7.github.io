---
layout: default
title: 主页
---

# 欢迎来到我的博客

这里会分享我在 **DevOps** 和 **网络安全** 领域的研究与实践。  

<div class="post-list">
  <h2>我的文章</h2>
  {% if site.posts.size > 0 %}  <!-- 先判断是否有文章 -->
    <ul>
      {% for post in site.posts %}  <!-- 循环所有文章 -->
        <li>
          <!-- 文章发布日期 -->
          <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
          <!-- 文章标题（链接到文章详情页） -->
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
          <!-- 可选：显示文章摘要 -->
          {% if post.excerpt %}
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <!-- 没有文章时显示的提示 -->
    <p>暂无文章，敬请期待！</p>
  {% endif %}
</div>

敬请期待更多内容 🚀
