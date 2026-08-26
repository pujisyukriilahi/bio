---
layout: default
title: "Commercial Check"
description: "A quick self-assessment to understand the strengths and gaps of your commercial team across strategy, marketing, sales, customer management, analytics, and collaboration."
permalink: /commercial-check/
---

<div class="wrap commercial-check-page">
  <section class="assessment-hero" style="border-top:0;">
    <div class="eyebrow">Commercial Team Self-Assessment</div>
    <h1>Commercial Check</h1>
    <p class="lead">How strong is your commercial team?</p>
    <p>Assess your team's commercial maturity across strategy, lead generation, sales process, customer management, performance analytics, and cross-functional collaboration.</p>
    <div class="assessment-note"><strong>How it works:</strong> 30 statements · 1–5 scale · approximately 7–10 minutes.</div>
  </section>

  <form id="commercial-check-form" class="assessment-form" novalidate>
    <section style="border-top:0;padding-top:0;">
      <div class="section-head"><h2>Company Profile</h2><div class="meta">Optional context</div></div>
      <div class="form-grid">
        <label>Company Name<input type="text" name="company" placeholder="Company name"></label>
        <label>Your Role<input type="text" name="role" placeholder="Your role / position"></label>
        <label>Industry<select name="industry"><option value="">Select industry</option><option>FMCG / Consumer Goods</option><option>B2B Manufacturing / Distribution</option><option>B2B Services / Consulting</option><option>Retail / Distributor</option><option>Technology</option><option>Other</option></select></label>
        <label>Commercial Team Size<select name="team_size"><option value="">Select size</option><option>1–10</option><option>11–30</option><option>31–100</option><option>100+</option></select></label>
      </div>
    </section>

    <div id="question-container"></div>

    <section class="assessment-section" style="border-top:0;">
      <div class="section-head"><h2>Your Results</h2><div class="meta">Calculated automatically</div></div>
      <div id="result-placeholder" class="assessment-placeholder">Complete all 30 statements to see your Commercial Check result.</div>
      <div id="result-panel" class="result-panel" hidden>
        <div class="result-score-wrap">
          <div class="eyebrow">Overall Commercial Maturity</div>
          <div id="overall-score" class="overall-score">0.0 / 5</div>
          <div id="maturity-label" class="maturity-label">—</div>
          <p id="result-summary"></p>
        </div>
        <div class="dimension-results" id="dimension-results"></div>
        <div class="recommendation-card">
          <div class="eyebrow">Priority Areas</div>
          <h3>Where should your team focus first?</h3>
          <div id="priority-results"></div>
        </div>
        <div class="actions result-actions">
          <a class="btn primary" href="https://wa.me/628971021300?text=Hi%20Puji,%20saya%20sudah%20mengisi%20Commercial%20Check%20dan%20ingin%20membahas%20hasilnya." target="_blank" rel="noopener noreferrer">Discuss My Results via WhatsApp</a>
          <button class="btn" type="button" id="copy-result">Copy Result Summary</button>
        </div>
      </div>
    </section>

    <div class="assessment-footer-actions">
      <button class="btn primary" type="submit">Calculate My Result</button>
    </div>
  </form>
</div>

<style>
.commercial-check-page{padding:20px 0 80px}.assessment-hero{max-width:820px}.assessment-hero h1{font-size:clamp(3rem,7vw,5.8rem);line-height:.98;letter-spacing:-.045em;margin:14px 0}.assessment-note{margin-top:24px;padding:16px 18px;border:1px solid var(--line);background:#fff;border-radius:12px;max-width:650px}.assessment-form{padding-top:10px}.form-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}.form-grid label,.question-card label{display:grid;gap:8px;font-weight:700}.form-grid input,.form-grid select{width:100%;padding:12px 13px;border:1px solid var(--line);border-radius:8px;background:#fff;font:inherit;color:var(--ink)}.assessment-section{padding:68px 0}.question-group{padding:48px 0;border-top:1px solid var(--line)}.question-group:first-child{border-top:0}.question-group h2{font-size:2rem}.question-card{padding:22px 0;border-bottom:1px solid var(--line)}.question-card:last-child{border-bottom:0}.question-text{font-size:1.05rem;margin:0 0 15px;font-weight:700}.scale-options{display:grid;grid-template-columns:repeat(5,1fr);gap:8px}.scale-options label{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px;padding:12px 8px;border:1px solid var(--line);border-radius:10px;background:#fff;cursor:pointer;font-size:.85rem;font-weight:600;text-align:center}.scale-options input{accent-color:var(--ink)}.scale-options label:has(input:checked){background:var(--ink);color:#fff;border-color:var(--ink)}.result-panel{display:grid;gap:28px}.result-score-wrap{padding:28px;border:1px solid var(--line);background:#fff;border-radius:16px}.overall-score{font-size:clamp(3rem,6vw,5rem);font-weight:800;line-height:1;margin:10px 0}.maturity-label{display:inline-block;padding:7px 11px;border-radius:999px;border:1px solid var(--line);font-weight:800}.dimension-results{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}.dimension-card{padding:20px;border:1px solid var(--line);background:#fff;border-radius:14px}.dimension-header{display:flex;justify-content:space-between;gap:16px;align-items:baseline}.dimension-score{font-weight:800}.bar{height:8px;border-radius:999px;background:#e8e8e2;overflow:hidden;margin-top:14px}.bar span{display:block;height:100%;background:var(--ink)}.recommendation-card{padding:24px;border:1px solid var(--line);background:#fff;border-radius:16px}.priority-item{padding:15px 0;border-bottom:1px solid var(--line)}.priority-item:last-child{border-bottom:0}.priority-score{font-weight:800}.result-actions{margin-top:4px}.assessment-placeholder{padding:20px;border:1px dashed var(--line);border-radius:12px;color:var(--muted);background:#fff}.assessment-footer-actions{display:flex;justify-content:center;padding:30px 0 0}.error-message{color:#8a2d2d;font-size:.92rem;margin-top:8px}@media(max-width:800px){.form-grid,.dimension-results{grid-template-columns:1fr}.scale-options{grid-template-columns:repeat(5,1fr);gap:6px}.scale-options label{font-size:.75rem;padding:10px 4px}.commercial-check-page{padding-top:0}}@media(max-width:520px){.scale-options{grid-template-columns:1fr 1fr 1fr 1fr 1fr}.scale-options label{min-height:66px}.question-card{padding:18px 0}}
</style>

<script>
(function(){
  const dimensions = [
    {
      key:'strategy',
      title:'Commercial Strategy',
      description:'Target market, positioning, value proposition, and commercial direction.',
      questions:[
        'Our team has a clearly defined target customer.',
        'Our value proposition is clear and differentiated from competitors.',
        'Commercial priorities are directly linked to business goals.',
        'The team understands why customers choose or reject our offering.',
        'Commercial strategy is reviewed and updated as market conditions change.'
      ]
    },
    {
      key:'marketing',
      title:'Lead Generation & Marketing',
      description:'Demand generation, lead quality, channel effectiveness, and marketing-sales handoff.',
      questions:[
        'We have clear and measurable lead generation channels.',
        'Leads are classified based on quality or potential value.',
        'Marketing and sales use the same definition of a qualified lead.',
        'Marketing channel performance can be measured through inquiry or sales.',
        'The team regularly evaluates lead quality, not only lead volume.'
      ]
    },
    {
      key:'sales',
      title:'Sales Process',
      description:'Pipeline discipline, qualification, proposal quality, negotiation, and closing.',
      questions:[
        'Our sales pipeline has clearly defined stages and criteria.',
        'Every opportunity has a clear next step and owner.',
        'Sales uses a qualification process before opportunities enter the active pipeline.',
        'Proposals are built around customer needs and business problems.',
        'We conduct win/loss reviews to understand why opportunities are won or lost.'
      ]
    },
    {
      key:'customer',
      title:'Customer & CRM',
      description:'Customer data, follow-up, relationship management, retention, and feedback.',
      questions:[
        'Customer and prospect data is stored in a structured system.',
        'Sales has a clear and consistent follow-up process.',
        'Relevant customer interaction history is accessible to the right team members.',
        'We have a clear strategy to increase repeat business or retention.',
        'Customer feedback is used to improve products, services, or commercial processes.'
      ]
    },
    {
      key:'analytics',
      title:'Performance & Analytics',
      description:'KPI management, funnel measurement, reporting, and data-driven decisions.',
      questions:[
        'Our commercial team has clear and measurable KPIs.',
        'Pipeline and conversion rates are monitored regularly.',
        'Management can identify the biggest bottleneck in the commercial funnel.',
        'Marketing, sales, and revenue data can be analyzed together.',
        'Commercial decisions are based on data, not only intuition.'
      ]
    },
    {
      key:'people',
      title:'People & Collaboration',
      description:'Capability, leadership, coaching, teamwork, and cross-functional execution.',
      questions:[
        'The sales and marketing team has the capabilities required by the business.',
        'Managers conduct regular coaching with their team members.',
        'Sales, marketing, customer service, and operations have clear handover processes.',
        'Functions understand their role in the end-to-end customer journey.',
        'The team regularly reviews performance and agrees on improvement actions.'
      ]
    }
  ];

  const container = document.getElementById('question-container');
  const form = document.getElementById('commercial-check-form');
  const placeholder = document.getElementById('result-placeholder');
  const resultPanel = document.getElementById('result-panel');
  const overallScore = document.getElementById('overall-score');
  const maturityLabel = document.getElementById('maturity-label');
  const resultSummary = document.getElementById('result-summary');
  const dimensionResults = document.getElementById('dimension-results');
  const priorityResults = document.getElementById('priority-results');
  const copyResult = document.getElementById('copy-result');

  function renderQuestions(){
    dimensions.forEach(function(dim, di){
      const section=document.createElement('section');
      section.className='question-group';
      section.innerHTML='<div class="section-head"><div><h2>'+dim.title+'</h2><div class="meta">'+dim.description+'</div></div><div class="meta">5 questions</div></div>';
      dim.questions.forEach(function(q, qi){
        const name=dim.key+'-'+qi;
        const card=document.createElement('div');
        card.className='question-card';
        let options='';
        for(let score=1; score<=5; score++){
          options += '<label><input required type="radio" name="'+name+'" value="'+score+'"><span>'+score+'</span></label>';
        }
        card.innerHTML='<p class="question-text">'+(qi+1)+'. '+q+'</p><div class="scale-options">'+options+'</div>';
        section.appendChild(card);
      });
      container.appendChild(section);
    });
  }

  function maturity(avg){
    if(avg < 2) return ['Foundational','The team needs stronger commercial foundations, clearer processes, and basic capability development.'];
    if(avg < 3) return ['Emerging','There are initial practices in place, but consistency and standardization remain important priorities.'];
    if(avg < 4) return ['Developing','Core practices are developing. The next focus should be stronger execution, coaching, and integration.'];
    if(avg < 4.6) return ['Established','The team has consistent practices and can focus on optimization, advanced capabilities, and stronger data use.'];
    return ['Optimized','The team demonstrates a mature commercial system with a strong foundation for innovation, scale, and continuous improvement.'];
  }

  function calculate(){
    const scores=[];
    dimensions.forEach(function(dim){
      let total=0;
      dim.questions.forEach(function(_, qi){
        const selected=form.querySelector('input[name="'+dim.key+'-'+qi+'"]:checked');
        total += selected ? Number(selected.value) : 0;
      });
      scores.push({key:dim.key,title:dim.title,score:total/dim.questions.length});
    });
    const avg=scores.reduce((a,b)=>a+b.score,0)/scores.length;
    const level=maturity(avg);
    overallScore.textContent=avg.toFixed(1)+' / 5';
    maturityLabel.textContent=level[0];
    resultSummary.textContent=level[1];
    dimensionResults.innerHTML=scores.map(function(item){
      const pct=Math.round((item.score/5)*100);
      return '<div class="dimension-card"><div class="dimension-header"><strong>'+item.title+'</strong><span class="dimension-score">'+item.score.toFixed(1)+'/5</span></div><div class="bar"><span style="width:'+pct+'%"></span></div></div>';
    }).join('');

    const priorities=scores.slice().sort((a,b)=>a.score-b.score).slice(0,3);
    priorityResults.innerHTML=priorities.map(function(item,idx){
      const gap=(5-item.score).toFixed(1);
      return '<div class="priority-item"><div><strong>'+(idx+1)+'. '+item.title+'</strong></div><div class="meta">Current score: '+item.score.toFixed(1)+'/5 · Gap to 5: '+gap+'</div></div>';
    }).join('');

    placeholder.hidden=true;
    resultPanel.hidden=false;
    resultPanel.scrollIntoView({behavior:'smooth',block:'start'});

    return {overall:avg,level:level[0],scores:scores,priorities:priorities};
  }

  renderQuestions();
  form.addEventListener('submit', function(e){
    e.preventDefault();
    if(!form.checkValidity()){
      form.reportValidity();
      return;
    }
    window.__commercialResult=calculate();
  });

  copyResult.addEventListener('click', async function(){
    const r=window.__commercialResult;
    if(!r) return;
    let text='Commercial Check – Puji Syukri Ilahi\nOverall: '+r.overall.toFixed(1)+'/5\nMaturity: '+r.level+'\n\nDimension Scores:\n';
    r.scores.forEach(function(s){text += '- '+s.title+': '+s.score.toFixed(1)+'/5\n';});
    text += '\nPriority Areas:\n';
    r.priorities.forEach(function(s,i){text += (i+1)+'. '+s.title+' ('+s.score.toFixed(1)+'/5)\n';});
    try{
      await navigator.clipboard.writeText(text);
      copyResult.textContent='Copied!';
      setTimeout(()=>copyResult.textContent='Copy Result Summary',1800);
    }catch(err){
      alert(text);
    }
  });
})();
</script>
