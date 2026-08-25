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

  <div style="margin-top:32px; display:flex; flex-wrap:wrap; gap:10px;">
    <button class="insight-filter active" data-filter="all" type="button">All</button>
    {% assign categories = site.posts | map: 'categories' | flatten | uniq | sort %}
    {% for category in categories %}
      <button class="insight-filter" data-filter="{{ category | slugify }}" type="button">{{ category }}</button>
    {% endfor %}
  </div>

  <div class="list" style="margin-top:40px;" id="insights-list">
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% for post in posts %}
    <article class="insight-card" data-categories="{{ post.categories | join: ' ' | slugify }}">
      <div class="eyebrow">{{ post.categories | join: ' • ' }}</div>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <div class="meta">{{ post.date | date: "%d %B %Y" }}</div>
      <p>{{ post.description | default: post.excerpt | strip_html | truncate: 220 }}</p>
      <a href="{{ post.url | relative_url }}" class="btn">Read Article</a>
    </article>
  {% endfor %}
  {% if site.posts.size == 0 %}<p class="empty">No articles yet. New insights will be published regularly.</p>{% endif %}
  </div>

  <p id="insights-empty" class="empty" style="display:none; margin-top:32px;">Tidak ada artikel pada kategori ini.</p>
</div>

<style>
  .insight-filter{border:1px solid #dbe3ea;background:#fff;color:#475569;padding:10px 16px;border-radius:999px;font:inherit;font-weight:700;cursor:pointer;transition:.2s ease}
  .insight-filter:hover{transform:translateY(-1px)}
  .insight-filter.active{background:#0f172a;color:#fff;border-color:#0f172a}
  .insight-card.is-hidden{display:none}
</style>

<script>
(function(){
  const buttons = document.querySelectorAll('.insight-filter');
  const cards = document.querySelectorAll('.insight-card');
  const empty = document.getElementById('insights-empty');

  function applyFilter(filter){
    let visible = 0;
    cards.forEach(card => {
      const categories = card.dataset.categories || '';
      const show = filter === 'all' || categories.split(' ').includes(filter);
      card.classList.toggle('is-hidden', !show);
      if(show) visible++;
    });
    empty.style.display = visible ? 'none' : 'block';
    buttons.forEach(btn => btn.classList.toggle('active', btn.dataset.filter === filter));
  }

  buttons.forEach(btn => btn.addEventListener('click', () => applyFilter(btn.dataset.filter)));
})();
</script>
