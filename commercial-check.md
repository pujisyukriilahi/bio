---
layout: default
title: "Commercial Check"
description: "A quick self-assessment to understand the strengths and gaps of your commercial team across strategy, marketing, sales, customer management, analytics, AI, technology, and collaboration."
permalink: /commercial-check/
---

<div class="wrap commercial-check-page">
  <section class="assessment-hero" style="border-top:0;">
    <div class="eyebrow">Commercial Team Self-Assessment</div>
    <h1>Commercial Check</h1>
    <p class="lead">How strong is your commercial team?</p>
    <p>Assess your team's commercial maturity across strategy, lead generation, sales process, customer management, performance analytics, AI & technology adoption, and cross-functional collaboration.</p>
    <div class="assessment-note"><strong>How it works:</strong> 35 statements · 1–5 scale · approximately 8–10 minutes.</div>
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

    <div class="completion-status" id="completion-status" aria-live="polite">
      <strong id="completion-text">0 of 35 questions answered</strong>
      <div class="completion-bar"><span id="completion-bar-fill" style="width:0%"></span></div>
      <div class="completion-note" id="completion-note">Answer every statement to unlock your result.</div>
    </div>

    <div id="question-container"></div>

    <div class="assessment-footer-actions">
      <button class="btn primary" id="calculate-button" type="submit">Calculate My Result</button>
      <div class="form-submit-note" id="form-submit-note">Complete all questions before calculating.</div>
    </div>

    <section class="assessment-section results-section" style="border-top:0;">
      <div class="section-head"><h2>Your Results</h2><div class="meta">Calculated from your answers</div></div>
      <div id="result-placeholder" class="assessment-placeholder">Complete all 35 statements and calculate your result to see the diagnosis.</div>
      <div id="result-panel" class="result-panel" hidden>
        <div class="result-score-wrap">
          <div class="eyebrow">Overall Commercial Maturity</div>
          <div id="overall-score" class="overall-score">0.0 / 5</div>
          <div id="maturity-label" class="maturity-label">—</div>
          <p id="result-summary"></p>
        </div>

        <div>
          <div class="eyebrow">Commercial Diagnosis</div>
          <h3>How the dimensions connect</h3>
          <div id="diagnosis-results" class="diagnosis-stack"></div>
        </div>

        <div>
          <div class="eyebrow">Priority Areas</div>
          <h3>The three most important intervention areas</h3>
          <div id="priority-results"></div>
        </div>

        <div class="training-recommendation-card">
          <div class="eyebrow">Recommended Development</div>
          <h3>3 training recommendations for your commercial team</h3>
          <p id="training-intro"></p>
          <div id="training-recommendations"></div>
        </div>

        <div class="consultation-card">
          <div class="eyebrow">Next Step</div>
          <h3>Consult the result with MarkedTraining</h3>
          <p>Use this result as an initial diagnostic. The final training recommendation should be validated with business context, root cause, current priorities, and expected business impact.</p>
          <div class="actions result-actions">
            <a class="btn primary" id="whatsapp-result" href="https://wa.me/628971021300" target="_blank" rel="noopener noreferrer">Discuss with MarkedTraining via WhatsApp</a>
            <button class="btn" type="button" id="copy-result">Copy Result Summary</button>
          </div>
        </div>
      </div>
    </section>
  </form>
</div>

<style>
.commercial-check-page{padding:20px 0 80px}.assessment-hero{max-width:820px}.assessment-hero h1{font-size:clamp(3rem,7vw,5.8rem);line-height:.98;letter-spacing:-.045em;margin:14px 0}.assessment-note{margin-top:24px;padding:16px 18px;border:1px solid var(--line);background:#fff;border-radius:12px;max-width:650px}.assessment-form{padding-top:10px}.form-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}.form-grid label,.question-card label{display:grid;gap:8px;font-weight:700}.form-grid input,.form-grid select{width:100%;padding:12px 13px;border:1px solid var(--line);border-radius:8px;background:#fff;font:inherit;color:var(--ink)}.completion-status{position:sticky;top:73px;z-index:5;padding:14px 16px;margin:18px 0;background:rgba(247,247,244,.96);backdrop-filter:blur(10px);border:1px solid var(--line);border-radius:12px}.completion-status strong{display:block;font-size:.94rem}.completion-bar{height:7px;background:#e8e8e2;border-radius:999px;overflow:hidden;margin-top:9px}.completion-bar span{display:block;height:100%;background:var(--ink);transition:width .2s ease}.completion-note,.form-submit-note{margin-top:7px;color:var(--muted);font-size:.86rem}.question-group{padding:48px 0;border-top:1px solid var(--line)}.question-group:first-child{border-top:0}.question-group h2{font-size:2rem}.question-card{padding:22px 0;border-bottom:1px solid var(--line)}.question-card:last-child{border-bottom:0}.question-text{font-size:1.05rem;margin:0 0 15px;font-weight:700}.question-card.missing{padding:18px 14px;margin:0 -14px;border:1px solid #b34a4a;border-radius:12px}.question-card.missing .question-text{color:#7f1f1f}.missing-message{margin-top:8px;color:#8a2d2d;font-size:.88rem;font-weight:700}.scale-options{display:grid;grid-template-columns:repeat(5,1fr);gap:8px}.scale-options label{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px;padding:12px 8px;border:1px solid var(--line);border-radius:10px;background:#fff;cursor:pointer;font-size:.85rem;font-weight:600;text-align:center}.scale-options input{accent-color:var(--ink)}.scale-options label:has(input:checked){background:var(--ink);color:#fff;border-color:var(--ink)}.assessment-footer-actions{display:flex;flex-direction:column;align-items:center;gap:10px;padding:30px 0 0}.is-disabled{opacity:.55;cursor:not-allowed}.ai-callout{margin:0 0 8px;padding:14px 16px;border:1px solid var(--line);background:#fff;border-radius:10px;color:#444}.assessment-section{padding:68px 0}.assessment-placeholder{padding:20px;border:1px dashed var(--line);border-radius:12px;color:var(--muted);background:#fff}.result-panel{display:grid;gap:34px}.result-score-wrap,.training-recommendation-card,.consultation-card{padding:28px;border:1px solid var(--line);background:#fff;border-radius:16px}.overall-score{font-size:clamp(3rem,6vw,5rem);font-weight:800;line-height:1;margin:10px 0}.maturity-label{display:inline-block;padding:7px 11px;border-radius:999px;border:1px solid var(--line);font-weight:800}.diagnosis-stack{display:grid;gap:14px}.diagnosis-card{padding:22px;border:1px solid var(--line);background:#fff;border-radius:14px}.diagnosis-card h4{margin:0 0 8px;font-size:1.05rem}.diagnosis-card p{margin:7px 0}.diagnosis-links{color:var(--muted);font-size:.93rem}.dimension-results{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}.dimension-card{padding:20px;border:1px solid var(--line);background:#fff;border-radius:14px}.dimension-header{display:flex;justify-content:space-between;gap:16px;align-items:baseline}.dimension-score{font-weight:800}.bar{height:8px;border-radius:999px;background:#e8e8e2;overflow:hidden;margin-top:14px}.bar span{display:block;height:100%;background:var(--ink)}.priority-item,.training-item{padding:18px 0;border-bottom:1px solid var(--line)}.priority-item:last-child,.training-item:last-child{border-bottom:0}.training-item h4{margin:0 0 6px;font-size:1.08rem}.training-meta{font-size:.9rem;color:var(--muted);margin-bottom:8px}.training-reason{margin:0}.consultation-card{margin-top:2px}.result-actions{margin-top:16px}.training-badge{display:inline-block;border:1px solid var(--line);padding:5px 9px;border-radius:999px;font-size:.76rem;font-weight:800;margin-bottom:8px}.form-submit-note{min-height:20px;text-align:center}@media(max-width:800px){.form-grid,.dimension-results{grid-template-columns:1fr}.scale-options{grid-template-columns:repeat(5,1fr);gap:6px}.scale-options label{font-size:.75rem;padding:10px 4px}.commercial-check-page{padding-top:0}}@media(max-width:520px){.completion-status{top:62px}.scale-options{grid-template-columns:repeat(5,1fr)}.scale-options label{min-height:66px}.question-card{padding:18px 0}}
</style>

<script>
(function(){
  const dimensions = [
    {key:'strategy',title:'Commercial Strategy',questions:['Our team has a clearly defined target customer.','Our value proposition is clear and differentiated from competitors.','Commercial priorities are directly linked to business goals.','The team understands why customers choose or reject our offering.','Commercial strategy is reviewed and updated as market conditions change.']},
    {key:'marketing',title:'Lead Generation & Marketing',questions:['We have clear and measurable lead generation channels.','Leads are classified based on quality or potential value.','Marketing and sales use the same definition of a qualified lead.','Marketing channel performance can be measured through inquiry or sales.','The team regularly evaluates lead quality, not only lead volume.']},
    {key:'sales',title:'Sales Process',questions:['Our sales pipeline has clearly defined stages and criteria.','Every opportunity has a clear next step and owner.','Sales uses a qualification process before opportunities enter the active pipeline.','Proposals are built around customer needs and business problems.','We conduct win/loss reviews to understand why opportunities are won or lost.']},
    {key:'customer',title:'Customer & CRM',questions:['Customer and prospect data is stored in a structured system.','Sales has a clear and consistent follow-up process.','Relevant customer interaction history is accessible to the right team members.','We have a clear strategy to increase repeat business or retention.','Customer feedback is used to improve products, services, or commercial processes.']},
    {key:'analytics',title:'Performance & Analytics',questions:['Our commercial team has clear and measurable KPIs.','Pipeline and conversion rates are monitored regularly.','Management can identify the biggest bottleneck in the commercial funnel.','Marketing, sales, and revenue data can be analyzed together.','Commercial decisions are based on data, not only intuition.']},
    {key:'technology',title:'AI, Tools & Technology',callout:'Think about how consistently tools and AI are actually embedded in daily commercial work—not only whether the team has access to them.',questions:['Our team uses CRM or another structured system consistently to manage leads, opportunities, and pipeline.','Our commercial team uses dashboards or analytics tools to support decisions and performance reviews.','We use automation to reduce repetitive commercial or marketing tasks where appropriate.','AI tools are used consistently for relevant sales or marketing workflows such as research, content, analysis, prospecting, or productivity.','We have clear practices for data hygiene, tool adoption, and responsible use of AI in commercial work.']},
    {key:'people',title:'People & Collaboration',questions:['The sales and marketing team has the capabilities required by the business.','Managers conduct regular coaching with their team members.','Sales, marketing, customer service, and operations have clear handover processes.','Functions understand their role in the end-to-end customer journey.','The team regularly reviews performance and agrees on improvement actions.']}
  ];
  const TOTAL=35;
  const container=document.getElementById('question-container');
  const form=document.getElementById('commercial-check-form');
  const placeholder=document.getElementById('result-placeholder');
  const panel=document.getElementById('result-panel');
  const overallEl=document.getElementById('overall-score');
  const maturityEl=document.getElementById('maturity-label');
  const summaryEl=document.getElementById('result-summary');
  const dimensionsEl=document.getElementById('dimension-results');
  const diagnosisEl=document.getElementById('diagnosis-results');
  const priorityEl=document.getElementById('priority-results');
  const trainingEl=document.getElementById('training-recommendations');
  const trainingIntro=document.getElementById('training-intro');
  const copyBtn=document.getElementById('copy-result');
  const waBtn=document.getElementById('whatsapp-result');
  const completionText=document.getElementById('completion-text');
  const completionBar=document.getElementById('completion-bar-fill');
  const completionNote=document.getElementById('completion-note');
  const calcBtn=document.getElementById('calculate-button');
  const submitNote=document.getElementById('form-submit-note');

  function renderQuestions(){dimensions.forEach(function(dim){const section=document.createElement('section');section.className='question-group';let heading='<div class="section-head"><div><h2>'+dim.title+'</h2><div class="meta">5 questions</div></div></div>';if(dim.callout)heading+='<div class="ai-callout">'+dim.callout+'</div>';section.innerHTML=heading;dim.questions.forEach(function(q,qi){const name=dim.key+'-'+qi,card=document.createElement('div');card.className='question-card';let options='';for(let s=1;s<=5;s++)options+='<label><input required type="radio" name="'+name+'" value="'+s+'"><span>'+s+'</span></label>';card.innerHTML='<p class="question-text">'+(qi+1)+'. '+q+'</p><div class="scale-options">'+options+'</div>';section.appendChild(card);});container.appendChild(section);});}
  function updateProgress(){let answered=0;dimensions.forEach(function(dim){dim.questions.forEach(function(_,qi){if(form.querySelector('input[name="'+dim.key+'-'+qi+'"]:checked'))answered++;});});const pct=Math.round(answered/TOTAL*100);completionText.textContent=answered+' of '+TOTAL+' questions answered';completionBar.style.width=pct+'%';if(answered===TOTAL){completionNote.textContent='All questions answered. Your result is ready to calculate.';calcBtn.classList.remove('is-disabled');submitNote.textContent='';}else{completionNote.textContent='Answer all '+TOTAL+' statements to unlock your result.';calcBtn.classList.add('is-disabled');}}
  function maturity(avg){if(avg<2)return['Foundational','The team needs stronger commercial foundations, clearer processes, and basic capability development.'];if(avg<3)return['Emerging','There are initial practices in place, but consistency and standardization remain important priorities.'];if(avg<4)return['Developing','Core practices are developing. The next focus should be stronger execution, coaching, and integration.'];if(avg<4.6)return['Established','The team has consistent practices and can focus on optimization, advanced capabilities, and stronger data use.'];return['Optimized','The team demonstrates a mature commercial system with a strong foundation for innovation, scale, and continuous improvement.'];}
  const trainingMap={strategy:{name:'Commercial Strategy & Go-to-Market',format:'Workshop / working session',reason:'Strengthen target market, positioning, value proposition, and commercial priorities.'},marketing:{name:'Lead Generation & Performance Marketing',format:'Workshop + hands-on implementation',reason:'Improve lead quality, channel effectiveness, and marketing-to-sales handoff.'},sales:{name:'Consultative Selling, Discovery & Closing',format:'Workshop + roleplay + coaching',reason:'Strengthen qualification, discovery, proposal relevance, negotiation, and closing.'},customer:{name:'CRM, Customer Management & Retention',format:'Hands-on training + coaching',reason:'Improve CRM discipline, follow-up, customer visibility, retention, and customer feedback use.'},analytics:{name:'Commercial Analytics & Performance Dashboard',format:'Workshop + applied project',reason:'Connect KPI, pipeline, conversion, marketing, sales, and revenue data for better decisions.'},technology:{name:'AI for Commercial Productivity & Workflow',format:'AI workshop / bootcamp + use-case implementation',reason:'Embed AI, automation, CRM, analytics, and data discipline into daily commercial workflows.'},people:{name:'Sales Leadership, Coaching & Cross-Functional Alignment',format:'Leadership workshop + coaching',reason:'Improve manager coaching, accountability, handover, and collaboration across the customer journey.'}};
  const relationRules=[
    {keys:['marketing','sales'],title:'Lead-to-Sales Conversion Gap',text:'Marketing and Sales both shape the top-to-middle of the funnel. If lead generation is weak and sales process is also weak, increasing lead volume alone is unlikely to solve the commercial problem. The priority is to align lead quality, qualification, handoff, and conversion.',training:'sales'},
    {keys:['sales','customer'],title:'Conversion-to-Retention Gap',text:'A weak sales process combined with weak customer management suggests the commercial issue may continue after the deal is won. The team needs stronger qualification, follow-up, customer visibility, and repeat-business discipline.',training:'customer'},
    {keys:['analytics','technology'],title:'Data-to-Execution Gap',text:'Low analytics maturity combined with weak tools and AI adoption can make the team reactive: data exists but is not consistently translated into decisions or workflow improvement. Capability building should connect analytics with practical tool and AI usage.',training:'analytics'},
    {keys:['technology','people'],title:'Adoption & Capability Gap',text:'Tools do not create value by themselves. Weak technology adoption together with people and collaboration gaps indicates that the challenge may be workflow, capability, coaching, or adoption discipline—not simply lack of software.',training:'technology'},
    {keys:['strategy','marketing'],title:'Strategy-to-Demand Gap',text:'A weak commercial strategy combined with weak lead generation can indicate that the team is generating activity before the target customer, positioning, and demand priorities are sufficiently clear.',training:'strategy'},
    {keys:['strategy','sales'],title:'Strategy-to-Sales Gap',text:'When commercial strategy and sales execution are both weak, the team may struggle to translate market positioning into a consistent sales motion, qualification process, and proposal approach.',training:'sales'},
    {keys:['people','sales'],title:'Capability-to-Conversion Gap',text:'Weak people capability alongside a weak sales process suggests the issue is not only process design. The team may need structured selling skills, coaching, and a shared sales methodology.',training:'people'},
    {keys:['marketing','analytics'],title:'Demand-to-Measurement Gap',text:'Weak marketing and analytics together suggest the organization may be generating activity without a sufficiently clear view of channel quality, conversion, and contribution to revenue.',training:'analytics'}
  ];
  function findRelations(scores){const low=scores.slice().sort((a,b)=>a.score-b.score);const lowKeys=low.slice(0,4).map(s=>s.key);const matched=[];relationRules.forEach(function(rule){if(rule.keys.every(k=>lowKeys.includes(k)))matched.push(rule);});if(!matched.length){
      if(lowKeys.includes('sales'))matched.push({title:'Commercial Conversion Gap',text:'The assessment points to a combination of gaps affecting the ability to convert opportunities into revenue. Review qualification, discovery, proposal quality, negotiation, and the supporting customer or marketing processes before adding more activity.',training:'sales'});
      if(lowKeys.includes('technology'))matched.push({title:'Commercial Enablement Gap',text:'The team may have opportunities to improve how technology, AI, CRM, and analytics support daily commercial work. Focus on adoption in real workflows rather than tools in isolation.',training:'technology'});
      if(lowKeys.includes('marketing'))matched.push({title:'Demand Generation Gap',text:'The team may need stronger alignment between target customer, channel execution, lead quality, and conversion measurement.',training:'marketing'});
    }
    return matched.slice(0,3);
  }
  function calculate(){
    const scores=dimensions.map(function(dim){let total=0;dim.questions.forEach(function(_,qi){total+=Number(form.querySelector('input[name="'+dim.key+'-'+qi+'"]:checked').value);});return{key:dim.key,title:dim.title,score:total/5};});
    const avg=scores.reduce((a,b)=>a+b.score,0)/scores.length,level=maturity(avg),low=scores.slice().sort((a,b)=>a.score-b.score),priorities=low.slice(0,3),relations=findRelations(scores);
    overallEl.textContent=avg.toFixed(1)+' / 5';maturityEl.textContent=level[0];summaryEl.textContent=level[1];
    dimensionsEl.innerHTML=scores.map(function(s){return'<div class="dimension-card"><div class="dimension-header"><strong>'+s.title+'</strong><span class="dimension-score">'+s.score.toFixed(1)+'/5</span></div><div class="bar"><span style="width:'+Math.round(s.score/5*100)+'%"></span></div></div>';}).join('');
    priorityEl.innerHTML=priorities.map(function(s,i){return'<div class="priority-item"><strong>'+(i+1)+'. '+s.title+'</strong><div class="meta">Current score: '+s.score.toFixed(1)+'/5 · Gap to 5: '+(5-s.score).toFixed(1)+'</div></div>';}).join('');
    diagnosisEl.innerHTML=relations.map(function(r){return'<div class="diagnosis-card"><h4>'+r.title+'</h4><p>'+r.text+'</p><p class="diagnosis-links"><strong>Dimensions connected:</strong> '+r.keys.join(' + ')+'</p></div>';}).join('');
    const recKeys=[];relations.forEach(function(r){if(!recKeys.includes(r.training))recKeys.push(r.training);});low.forEach(function(s){if(recKeys.length<3&&!recKeys.includes(s.key))recKeys.push(s.key);});
    const recommendations=recKeys.slice(0,3).map(k=>trainingMap[k]);
    trainingIntro.textContent='The recommendations below are not based on one low score in isolation. They combine the lowest-scoring dimensions and the relationships between them, then translate the pattern into three development priorities. Validate the final intervention with MarkedTraining against the team’s business context and root cause.';
    trainingEl.innerHTML=recommendations.map(function(t,i){return'<div class="training-item"><span class="training-badge">Priority '+(i+1)+'</span><h4>'+t.name+'</h4><div class="training-meta">Suggested format: '+t.format+'</div><p class="training-reason">'+t.reason+'</p></div>';}).join('');
    const company=form.querySelector('[name="company"]').value.trim()||'our team',message='Hi MarkedTraining, I completed the Commercial Check for '+company+'. Overall score: '+avg.toFixed(1)+'/5 ('+level[0]+'). The assessment identified cross-dimensional priorities: '+priorities.map(p=>p.title).join(', ')+'. Recommended training: '+recommendations.map(t=>t.name).join('; ')+'. I would like to consult on the appropriate development plan.';
    waBtn.href='https://wa.me/628971021300?text='+encodeURIComponent(message);panel.hidden=false;placeholder.hidden=true;panel.scrollIntoView({behavior:'smooth',block:'start'});
    return{overall:avg,level:level[0],scores:scores,priorities:priorities,relations:relations,recommendations:recommendations};
  }
  function showMissing(){const missing=[];dimensions.forEach(function(dim){dim.questions.forEach(function(_,qi){const input=form.querySelector('input[name="'+dim.key+'-'+qi+'"]'),checked=form.querySelector('input[name="'+dim.key+'-'+qi+'"]:checked'),card=input.closest('.question-card');card.classList.toggle('missing',!checked);let msg=card.querySelector('.missing-message');if(!checked){missing.push(1);if(!msg){msg=document.createElement('div');msg.className='missing-message';msg.textContent='Please answer this question.';card.appendChild(msg);}}else if(msg)msg.remove();});});return missing;}
  renderQuestions();updateProgress();form.addEventListener('change',function(){updateProgress();showMissing();});form.addEventListener('submit',function(e){e.preventDefault();const missing=showMissing();if(missing.length){completionNote.textContent=missing.length+' question'+(missing.length===1?' is':'s are')+' still unanswered. Please complete the highlighted questions.';submitNote.textContent='Please complete all highlighted questions before calculating your result.';const first=form.querySelector('.question-card.missing');if(first)first.scrollIntoView({behavior:'smooth',block:'center'});return;}window.__commercialResult=calculate();});
  copyBtn.addEventListener('click',async function(){const r=window.__commercialResult;if(!r)return;let text='Commercial Check – Puji Syukri Ilahi\nOverall: '+r.overall.toFixed(1)+'/5\nMaturity: '+r.level+'\n\nCross-dimensional diagnosis:\n';r.relations.forEach(function(x){text+='- '+x.title+': '+x.text+'\n';});text+='\nRecommended Training:\n';r.recommendations.forEach(function(t,i){text+=(i+1)+'. '+t.name+' — '+t.reason+'\n';});text+='\nDiscuss with MarkedTraining: 08971021300';try{await navigator.clipboard.writeText(text);copyBtn.textContent='Copied!';setTimeout(()=>copyBtn.textContent='Copy Result Summary',1800);}catch(err){alert(text);}});
})();
</script>
