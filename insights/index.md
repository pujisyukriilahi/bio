---
layout: default
title: "Insights"
description: "Insights from Puji Syukri Ilahi on marketing, strategy, analytics, market intelligence, business growth, learning, and AI."
permalink: /insights/
---
<div class="wrap" style="padding:80px 0;">
  <div class="eyebrow">Knowledge hub</div>
  <h1>Insights</h1>
  <p class="lead">Ideas, experiments, frameworks, and lessons from marketing, strategy, analytics, market intelligence, business growth, learning, and AI.</p>
  <div class="list" style="margin-top:48px;">
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% for post in posts %}
    <article>
      <div class="eyebrow">{{ post.categories | join: ' • ' }}</div>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <div class="meta">{{ post.date | date: "%d %B %Y" }}</div>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 220 }}</p>
    </article>
  {% endfor %}
  {% if site.posts.size == 0 %}<p class="empty">No articles yet.</p>{% endif %}
  </div>
</div>
