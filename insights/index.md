---
layout: default
title: "Insights"
description: "A collection of Puji Syukri Ilahi's perspectives, experiences, frameworks, and lessons on marketing, strategy, analytics, market intelligence, business growth, learning, and AI."
permalink: /insights/
---
<div class="wrap" style="padding:80px 0;">
  <div class="eyebrow">Knowledge Hub</div>
  <h1>Insights</h1>
  <p class="lead">A collection of perspectives, experiences, frameworks, and lessons from real-world work across marketing, strategy, analytics, market intelligence, business growth, corporate learning, and AI.</p>
  <div class="list" style="margin-top:48px;">
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% for post in posts %}
    <article>
      <div class="eyebrow">{{ post.categories | join: ' • ' }}</div>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <div class="meta">{{ post.date | date: "%d %B %Y" }}</div>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 220 }}</p>
      <a href="{{ post.url | relative_url }}" class="btn">Read Article</a>
    </article>
  {% endfor %}
  {% if site.posts.size == 0 %}<p class="empty">No articles yet. New insights will be published regularly.</p>{% endif %}
  </div>
</div>
