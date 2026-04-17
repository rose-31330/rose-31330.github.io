---
layout: page
title: Blog
permalink: /blog/
---

<div class="post-list">
  {% for post in site.posts %}
  <article class="post-preview">
    {% if post.image %}
    <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-thumbnail">
    {% endif %}
    <div class="post-preview-body">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
      <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">Read more &rarr;</a>
    </div>
  </article>
  {% else %}
  <p style="font-family:'Courier New',monospace;color:#666;font-size:0.88rem;">No posts yet — watch this space.</p>
  {% endfor %}
</div>
