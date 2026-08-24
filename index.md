---
layout: default
title: "Strategi Pemasaran, Intelijen Pasar & Pertumbuhan Bisnis"
description: "Puji Syukri Ilahi — profesional strategi pemasaran, intelijen pasar, pertumbuhan bisnis, analitik, dan pembelajaran korporat yang berfokus mengubah insight bisnis menjadi pertumbuhan yang terukur."
---

<div class="wrap">
<section class="hero" style="border-top:0;">
<div>
<div class="eyebrow">Riset • Strategi • Komersial • Pembelajaran</div>
<h1>Mengubah Insight Bisnis Menjadi Pertumbuhan Bisnis.</h1>
<p class="lead">Profesional di bidang strategi pemasaran, intelijen pasar, pertumbuhan bisnis, analitik, dan pembelajaran korporat yang berfokus mengubah insight pelanggan, pasar, dan komersial menjadi keputusan yang dapat ditindaklanjuti.</p>
<div class="chips"><span class="chip">Strategi Pemasaran</span><span class="chip">Intelijen Pasar</span><span class="chip">Pertumbuhan Bisnis</span><span class="chip">Analitik Pemasaran</span><span class="chip">Pembelajaran Korporat</span></div>
<div class="actions"><a class="btn primary" href="#work">Lihat Portofolio</a><a class="btn" href="{{ '/insights/' | relative_url }}">Baca Insight</a></div>
</div>
<aside class="hero-card"><div class="eyebrow">Dampak Terpilih</div><div class="metric"><span>Pengalaman</span><strong>6+ tahun</strong></div><div class="metric"><span>Pendapatan didukung</span><strong>Rp1,2 M+</strong></div><div class="metric"><span>Pertumbuhan pendapatan pelatihan</span><strong>100%+</strong></div><div class="metric"><span>MER gabungan</span><strong>36×</strong></div></aside>
</section>

<section id="about"><div class="section-head"><h2>Tentang Saya</h2><div class="meta">Alumnus ITB • Indonesia</div></div>
<p>Puji Syukri Ilahi adalah profesional di bidang strategi pemasaran, intelijen pasar, dan pengembangan bisnis dengan pengalaman lebih dari 6 tahun di konsultasi pemasaran, riset pasar, pembelajaran korporat, pemasaran berbasis kinerja, pengembangan produk, dan pertumbuhan bisnis.</p>
<p>Fokus pekerjaannya mencakup riset, pemahaman pelanggan dan kompetitor, evaluasi kinerja pemasaran, strategi komersial, serta menerjemahkan data dan bukti menjadi rekomendasi yang dapat ditindaklanjuti.</p></section>

<section id="work"><div class="section-head"><h2>Portofolio Pilihan</h2><div class="meta">Bukti pekerjaan</div></div><div class="grid">
<article class="card"><div class="eyebrow">Bisnis Pendidikan</div><h3>Beta Belajar</h3><p>Memimpin pemasaran, penjualan, pengembangan produk, dan strategi pertumbuhan. Mengelola Meta Ads serta analitik terintegrasi antara pemasaran dan penjualan.</p><p><strong>Dampak:</strong> mendukung pendapatan kumulatif Rp1,2 M+, MER gabungan 36×, serta peningkatan konversi dari lead menjadi pelanggan dari 20% menjadi 37%.</p></article>
<article class="card"><div class="eyebrow">Pembelajaran Korporat</div><h3>Proxsis Mark</h3><p>Memimpin solusi pelatihan dan konsultasi komersial di bidang pemasaran, penjualan, merek, pemasaran digital, CRM, pengembangan bisnis, negosiasi, dan AI.</p><p><strong>Dampak:</strong> berkontribusi pada pertumbuhan pendapatan tahunan dari Rp1,93 M menjadi Rp2,49 M (+29%) pada 2025.</p></article>
<article class="card"><div class="eyebrow">Intelijen Pasar</div><h3>PT Finnet Indonesia</h3><p>Mengerjakan riset kompetitor, pelanggan, dan intelijen produk untuk peluang produk baru serta menerjemahkan bukti menjadi rekomendasi produk dan komersial.</p></article>
<article class="card"><div class="eyebrow">Kewirausahaan</div><h3>Tutorin</h3><p>Membangun bisnis pendidikan dengan fokus pada produk, pemasaran, pengalaman belajar, dan nilai pelanggan untuk program bimbingan belajar sekolah hingga perguruan tinggi.</p></article>
</div></section>

<section id="experience"><div class="section-head"><h2>Pengalaman</h2><div class="meta">Peran profesional pilihan</div></div><div class="timeline">
<div class="role"><div class="role-top"><div><h3>Proxsis Group</h3><div class="meta">Pemimpin Pelatihan Bisnis & Konsultan Riset Pemasaran</div></div><div class="meta">Sep 2023 – Sekarang</div></div><ul><li>Memimpin solusi pembelajaran korporat dan konsultasi serta menerjemahkan kebutuhan bisnis menjadi rangkaian pembelajaran, lokakarya, simulasi, pembinaan, dan penilaian.</li><li>Menyusun proposal komersial, metodologi, rekomendasi strategis, serta mengoordinasikan pelaksanaan lintas fungsi.</li></ul></div>
<div class="role"><div class="role-top"><div><h3>Beta Belajar</h3><div class="meta">Pendiri Bersama & Direktur Pemasaran</div></div><div class="meta">Okt 2019 – Sep 2023</div></div><ul><li>Memimpin pemasaran, penjualan, pengembangan produk, penentuan posisi, akuisisi pelanggan, dan ekspansi.</li><li>Membangun CRM, pengelolaan prospek, analitik, sistem tindak lanjut, dan alur kerja layanan pelanggan.</li></ul></div>
<div class="role"><div class="role-top"><div><h3>Adsmind</h3><div class="meta">Pendiri — Analitik Pemasaran & Kreator Pengetahuan AI</div></div><div class="meta">2026 – Sekarang</div></div><ul><li>Mengembangkan konten berbasis riset, kerangka kerja, dan materi edukasi tentang strategi pemasaran, wawasan pelanggan, analitik kampanye, funnel, pengembangan produk, dan AI dalam pemasaran.</li></ul></div>
</div></section>

<section id="insights"><div class="section-head"><h2>Insight Terbaru</h2><a class="meta" href="{{ '/insights/' | relative_url }}">Lihat semua →</a></div>
<div class="list">{% assign posts = site.posts | sort: 'date' | reverse %}{% for post in posts limit:4 %}<article><div class="eyebrow">{{ post.categories | join: ' • ' }}</div><h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2><div class="meta">{{ post.date | date: "%d %B %Y" }}</div><p>{{ post.description | default: post.excerpt | strip_html | truncate: 180 }}</p></article>{% endfor %}{% if site.posts.size == 0 %}<p class="empty">Insight akan segera hadir. Website ini sudah siap untuk publikasi artikel Markdown secara rutin.</p>{% endif %}</div></section>

<section id="contact"><div class="section-head"><h2>Mari Terhubung</h2><div class="meta">Terbuka untuk peluang & kolaborasi terpilih</div></div><p>Untuk kebutuhan rekrutmen, konsultasi, pembelajaran korporat, riset, atau kolaborasi profesional, silakan terhubung melalui LinkedIn atau email.</p><div class="actions"><a class="btn primary" href="https://www.linkedin.com/in/pujisyukriilahi/" target="_blank" rel="noreferrer">LinkedIn</a><a class="btn" href="mailto:pujisyukriilahi.psi@gmail.com">Email</a></div></section>
</div>
