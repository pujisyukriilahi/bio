---
layout: default
title: "Strategic Marketing, Market Intelligence & Business Growth"
description: "Puji Syukri Ilahi — Strategic Marketing, Market Intelligence, and Business Development professional with over 6 years of experience."
---

<div class="wrap">
<section class="hero" style="border-top:0;">
<div>
<div class="eyebrow">Research • Strategy • Commercial • Learning</div>
<h1>Turning Business Insights Into Business Growth.</h1>
<p class="lead">Strategic Marketing, Market Intelligence, and Business Development professional focused on turning customer, market, and commercial insights into practical business decisions.</p>
<div class="chips"><span class="chip">Marketing Strategy</span><span class="chip">Market Intelligence</span><span class="chip">Business Growth</span><span class="chip">Marketing Analytics</span><span class="chip">Corporate Learning</span></div>
<div class="actions"><a class="btn primary" href="#work">View Portfolio</a><a class="btn" href="{{ '/insights/' | relative_url }}">Read Insights</a></div>
</div>
</section>

<section id="about"><div class="section-head"><h2>About Me</h2><div class="meta">ITB alumnus • Indonesia</div></div>
<p>Puji Syukri Ilahi is a Strategic Marketing, Market Intelligence, and Business Development professional with over 6 years of experience in marketing consulting, market research, corporate learning, performance marketing, product development, and business growth. Experienced in conducting end-to-end market research, analyzing customer, competitor, product, and marketing data, and translating insights into actionable business recommendations.</p>
<p>Skilled in developing marketing strategies, supporting business growth initiatives, and collaborating with cross-functional teams to improve marketing performance, customer acquisition, and commercial decision-making.</p></section>

<section id="work"><div class="section-head"><div><h2>Selected Portfolio</h2><div class="meta">Latest selected projects</div></div></div><div class="grid">
<article class="card"><div class="eyebrow">Market Intelligence • 2024–2025</div><h3>PT Finnet Indonesia</h3><p><strong>Market Intelligence — Finpay Remittance</strong></p><p>Managed Competitor, Customer, and Product Intelligence research for Finpay Remittance, including benchmarking, customer analysis, value proposition development, and strategic recommendations.</p></article>
<article class="card"><div class="eyebrow">New Product Development • 2024–2025</div><h3>PT Finnet Indonesia</h3><p><strong>New Product Development — Payroll Solution & Earned Wage Access</strong></p><p>Analyzed opportunities for Payroll Solutions and Earned Wage Access (EWA), with recommendations for product development, positioning, and partnerships.</p></article>
<article class="card"><div class="eyebrow">Marketing & Sales Strategy • 2026</div><h3>PT Finnet Indonesia</h3><p><strong>Marketing & Sales Playbook Multifinance</strong></p><p>Contributed to Brand Perception Survey, Market Size & Market Share analysis, and development of a Marketing & Sales Playbook for the Multifinance segment.</p></article>
<article class="card"><div class="eyebrow">Customer & Vendor Research • 2026</div><h3>PT Pertamina International Shipping</h3><p><strong>Customer & Vendor Satisfaction Research</strong></p><p>Supported fieldwork, data validation, CSI and NPS analysis, and recommendations for improvement.</p></article>
</div><div style="margin-top:28px;"><a class="btn" href="{{ '/portfolio/' | relative_url }}">View all portfolio →</a></div></section>

<section id="experience"><div class="section-head"><div><h2>Professional Experience</h2><div class="meta">Selected roles</div></div></div><div class="timeline">
<div class="role"><div class="role-top"><div><h3>Beta Belajar</h3><div class="meta"><strong>Co-Founder & Marketing Director</strong></div></div><div class="meta">October 2019 – September 2023</div></div><p>Led marketing, business growth, product development, sales strategy, and business expansion for an education and tutoring company.</p><a class="btn" href="{{ '/experience/beta-belajar/' | relative_url }}">Read more →</a></div>
<div class="role"><div class="role-top"><div><h3>Proxsis Group</h3><div class="meta"><strong>Commercial Training Leader & Market Research Consultant</strong></div></div><div class="meta">September 2023 – Present</div></div><p>Led commercial training and corporate learning solutions across marketing, sales, business development, and AI, while supporting market research and consulting projects for corporate clients.</p><a class="btn" href="{{ '/experience/proxsis-group/' | relative_url }}">Read more →</a></div>
</div></section>

<section id="education"><div class="section-head"><h2>Education</h2><div class="meta">Academic background</div></div>
<div class="role"><div class="role-top"><div><h3>INSTITUT TEKNOLOGI BANDUNG (ITB)</h3><div class="meta"><strong>Bachelor of Science in Physics</strong></div></div><div class="meta">August 2015 – October 2019</div></div><ul><li>Developed strong foundations in analytical thinking, quantitative analysis, research, and problem solving through Physics education and research experience.</li><li><strong>Teaching Assistant</strong>, Basic & Advanced Physics Laboratories, ITB (2018–2019), supporting laboratory learning and practical activities.</li><li><strong>Speaker</strong>, 7th International Conference on Advanced Materials Science and Technology (ICAMST 2019), demonstrating research communication and presentation skills.</li></ul></div></section>

<section id="insights"><div class="section-head"><div><h2>Popular Insights</h2><div class="meta">Most visited articles</div></div><a class="meta" href="{{ '/insights/' | relative_url }}">View all →</a></div><div class="list" id="popular-insights"><p class="empty">Loading popular insights…</p></div>
<script>
document.addEventListener('DOMContentLoaded', function () {
  const container = document.getElementById('popular-insights');
  const posts = [{% for post in site.posts %}{title: {{ post.title | jsonify }}, url: {{ post.url | relative_url | jsonify }}, date: {{ post.date | date: '%d %B %Y' | jsonify }}, category: {{ post.categories | join: ' • ' | jsonify }}, description: {{ post.description | default: post.excerpt | strip_html | truncate: 180 | jsonify }} }{% unless forloop.last %},{% endunless %}{% endfor %}];
  const base = 'https://pujisyukriilahi.goatcounter.com/counter/';
  Promise.all(posts.map(function (post) {
    return fetch(base + encodeURIComponent(post.url) + '.json')
      .then(function (response) { return response.ok ? response.json() : {count: '0'}; })
      .then(function (data) { post.views = parseInt(String(data.count).replace(/[^0-9]/g, ''), 10) || 0; return post; })
      .catch(function () { post.views = 0; return post; });
  })).then(function (results) {
    results.sort(function (a, b) { return b.views - a.views; });
    const top = results.slice(0, 2);
    if (!top.length) { container.innerHTML = '<p class="empty">Insights will appear here as new Markdown articles are published.</p>'; return; }
    container.innerHTML = top.map(function (post) {
      return '<article><div class="eyebrow">' + post.category + '</div><h2><a href="' + post.url + '">' + post.title + '</a></h2><div class="meta">' + post.date + ' · ' + post.views.toLocaleString('id-ID') + ' visits</div><p>' + post.description + '</p></article>';
    }).join('');
  });
});
</script>
</section>

<section id="contact"><div class="section-head"><h2>Let's Connect</h2><div class="meta">Open to selected opportunities & collaborations</div></div><p>For hiring, consulting, corporate learning, research, or professional collaboration, connect with me through LinkedIn or WhatsApp.</p><div class="actions"><a class="btn primary" href="https://www.linkedin.com/in/pujisyukriilahi/" target="_blank" rel="noreferrer">LinkedIn</a><a class="btn" href="https://wa.me/628971021300" target="_blank" rel="noreferrer">WhatsApp</a></div></section>
</div>
