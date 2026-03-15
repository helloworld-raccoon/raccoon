---
layout: default
title: Blog
permalink: /blog/
---

<section class="content-section">
  <div class="section-heading">
    <p class="eyebrow">Archive</p>
    <h1>전체 게시글</h1>
    <p>공부하며 기록한 학습 정리, 문제 해결, 프로젝트 회고를 모아둔 공간입니다.</p>
  </div>

  <div class="blog-list">
    {% for post in site.posts %}
      <article class="panel blog-list-item">
        <p class="project-label">{{ post.category_label | default: "Tech Note" }}</p>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="post-meta">{{ post.date | date: "%Y.%m.%d" }}</p>
        <p>{{ post.excerpt | strip_html | strip_newlines | truncate: 180 }}</p>
      </article>
    {% endfor %}
  </div>
</section>

