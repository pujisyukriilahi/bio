---
layout: default
title: "Insight"
description: "Kumpulan pemikiran, pengalaman, kerangka kerja, dan pembelajaran Puji Syukri Ilahi tentang pemasaran, strategi, analitik, market intelligence, pertumbuhan bisnis, pembelajaran, dan AI."
permalink: /insights/
---
<div class="wrap" style="padding:80px 0;">
  <div class="eyebrow">Pusat Pengetahuan</div>
  <h1>Insight</h1>
  <p class="lead">Kumpulan pemikiran, pengalaman, kerangka kerja, dan pembelajaran dari pekerjaan nyata di bidang pemasaran, strategi, analitik, market intelligence, pertumbuhan bisnis, pembelajaran, dan AI.</p>
  <div class="list" style="margin-top:48px;">
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% for post in posts %}
    <article>
      <div class="eyebrow">{{ post.categories | join: ' • ' }}</div>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <div class="meta">{{ post.date | date: "%d %B %Y" }}</div>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 220 }}</p>
      <a href="{{ post.url | relative_url }}" class="btn">Baca Artikel</a>
    </article>
  {% endfor %}
  {% if site.posts.size == 0 %}<p class="empty">Belum ada artikel. Insight akan diterbitkan secara rutin.</p>{% endif %}
  </div>
</div>
