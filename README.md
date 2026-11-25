
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#21152f">
<title>Movie Night — Just Us</title>
<style>
:root{--ink:#251a30;--muted:#766d7e;--plum:#392448;--pink:#f1c6d9;--rose:#b85d85;--paper:#fffafd;--line:#eee4ec}
*{box-sizing:border-box}body{margin:0;background:linear-gradient(145deg,#f8edf4,#f7f4fa 55%,#fcefe9);font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,sans-serif;color:var(--ink);min-height:100vh}
.wrap{max-width:760px;margin:0 auto;padding:22px 16px 50px}.hero{background:linear-gradient(135deg,#21152f,#4b3157);color:white;border-radius:26px;padding:25px;position:relative;overflow:hidden;box-shadow:0 16px 40px #39244824}
.hero:after{content:"✦";position:absolute;font-size:170px;right:12px;top:-52px;color:#ffffff12}.eyebrow{font-size:11px;letter-spacing:2.4px;font-weight:800;color:#f1c6d9}.hero h1{font-family:Georgia,serif;font-weight:500;font-size:clamp(34px,8vw,52px);line-height:1.03;margin:14px 0 10px}.hero p{color:#e9dce9;max-width:430px;line-height:1.55;margin:0}.hero .tag{display:inline-block;margin-top:20px;border:1px solid #ffffff38;border-radius:99px;padding:7px 12px;font-size:12px;color:#f8eaf2}
.progress{display:flex;gap:6px;margin:18px 3px}.progress span{height:5px;border-radius:9px;background:#e8dce7;flex:1}.progress span.active{background:#a85b83}
.panel{background:#fff;border:1px solid #f0e6ee;border-radius:22px;padding:clamp(18px,4vw,28px);margin-top:14px;box-shadow:0 12px 35px #3924480b}.step{display:none}.step.active{display:block}.step h2{font:500 28px Georgia,serif;margin:0 0 7px}.hint{color:var(--muted);font-size:14px;line-height:1.5;margin:0 0 22px}
label.field{display:block;font-size:11px;letter-spacing:1.2px;font-weight:800;color:#796d7c;margin:18px 0 9px}
input[type=date],input[type=text],textarea,select{width:100%;border:1px solid var(--line);border-radius:12px;padding:13px 14px;font:inherit;color:var(--ink);background:#fff;outline:none}textarea{resize:vertical;min-height:90px}input:focus,textarea:focus,select:focus{border-color:#bd7d9d;box-shadow:0 0 0 3px #f8e8f0}
.choices{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:9px}.choice{position:relative}.choice input{position:absolute;opacity:0;pointer-events:none}.choice label{display:flex;align-items:center;gap:9px;border:1px solid var(--line);border-radius:13px;padding:13px 12px;min-height:52px;cursor:pointer;font-size:14px;background:#fff;transition:.15s}.choice input:checked+label{border-color:#b56a8d;background:#fff4f8;box-shadow:inset 0 0 0 1px #b56a8d}.choice label span{font-size:19px}.choice.wide{grid-column:1/-1}
.nav{display:flex;justify-content:space-between;gap:10px;margin-top:24px}.btn{border:0;border-radius:12px;padding:13px 19px;font-weight:750;font-size:14px;cursor:pointer}.primary{background:#392448;color:white}.secondary{background:#f5edf3;color:#59435b}.btn:disabled{opacity:.4;cursor:not-allowed}.note{font-size:12px;color:#827787;line-height:1.5;margin-top:16px}
.summary{background:#fbf6fa;border:1px solid #f0e5ed;border-radius:16px;padding:18px}.summary h3{font:500 25px Georgia,serif;margin:0 0 14px}.row{display:flex;gap:12px;padding:10px 0;border-bottom:1px solid #eee5ec;font-size:14px}.row:last-child{border:0}.row b{width:112px;flex-shrink:0;color:#77677a}.row span{line-height:1.45}.success{display:none;background:#eff8f1;color:#27643a;padding:12px;border-radius:10px;margin-top:12px;font-size:13px}
footer{text-align:center;color:#897f8b;font-size:12px;padding:22px 8px}
@media(max-width:440px){.choices{grid-template-columns:1fr}.choice.wide{grid-column:auto}.hero{padding:22px}.row b{width:94px}}
</style>
</head>
<body>
<main class="wrap">
<header class="hero">
  <div class="eyebrow">A LITTLE DATE PLANNER</div>
  <h1>Movie night.<br>Just us. ♥</h1>
  <p>One movie, your favourite snacks, and an evening planned together. Tell me what would make it lovely for you.</p>
  <div class="tag">✦ Your comfort. Your choices. Our evening.</div>
</header>
<div class="progress" aria-label="Progress"><span class="active"></span><span></span><span></span><span></span><span></span><span></span></div>
<section class="panel">
<form id="dateForm">
<div class="step active">
<h2>First, when works for you?</h2><p class="hint">Pick a date and a time that feels right. We can always adjust.</p>
<label class="field" for="date">DATE</label><input id="date" type="date" required>
<label class="field">PREFERRED TIME</label><div class="choices">
<div class="choice"><input type="radio" name="time" id="t1" value="5:00 PM"><label for="t1">🌇 5:00 PM</label></div>
<div class="choice"><input type="radio" name="time" id="t2" value="7:00 PM" checked><label for="t2">🍿 7:00 PM</label></div>
<div class="choice"><input type="radio" name="time" id="t3" value="8:00 PM"><label for="t3">🌙 8:00 PM</label></div>
<div class="choice"><input type="radio" name="time" id="t4" value="Let's decide together"><label for="t4">💬 Let's decide</label></div></div>
</div>
<div class="step">
<h2>Where should we meet?</h2><p class="hint">Choose somewhere you would feel comfortable. No pressure — we decide together.</p>
<div class="choices">
<div class="choice wide"><input type="radio" name="venue" id="v1" value="My place"><label for="v1"><span>🏠</span> My place — cosy home setup</label></div>
<div class="choice wide"><input type="radio" name="venue" id="v2" value="Your place"><label for="v2"><span>🏡</span> Your place</label></div>
<div class="choice wide"><input type="radio" name="venue" id="v3" value="Cinema"><label for="v3"><span>🎥</span> Cinema</label></div>
<div class="choice wide"><input type="radio" name="venue" id="v4" value="A restaurant or lounge"><label for="v4"><span>✨</span> Restaurant or lounge</label></div>
<div class="choice wide"><input type="radio" name="venue" id="v5" value="Let's decide together" checked><label for="v5"><span>🤝</span> Let's decide together</label></div>
</div>
<label class="field" for="venueOther">ANOTHER VENUE IDEA? (OPTIONAL)</label><input id="venueOther" type="text" placeholder="Add a place or neighbourhood">
</div>
<div class="step">
<h2>What are we watching?</h2><p class="hint">Pick the mood. You can name a specific movie too.</p>
<div class="choices">
<div class="choice"><input type="radio" name="genre" id="g1" value="Romance" checked><label for="g1"><span>❤️</span> Romance</label></div>
<div class="choice"><input type="radio" name="genre" id="g2" value="Comedy"><label for="g2"><span>😂</span> Comedy</label></div>
<div class="choice"><input type="radio" name="genre" id="g3" value="Thriller / Mystery"><label for="g3"><span>🔍</span> Thriller</label></div>
<div class="choice"><input type="radio" name="genre" id="g4" value="Horror"><label for="g4"><span>👻</span> Horror</label></div>
<div class="choice"><input type="radio" name="genre" id="g5" value="Action"><label for="g5"><span>🔥</span> Action</label></div>
<div class="choice"><input type="radio" name="genre" id="g6" value="Surprise me"><label for="g6"><span>🎲</span> Surprise me</label></div>
</div>
<label class="field" for="movie">SPECIFIC MOVIE (OPTIONAL)</label><input id="movie" type="text" placeholder="A movie you've been wanting to watch">
</div>
<div class="step">
<h2>Snacks are important. 🍿</h2><p class="hint">Choose anything you would enjoy. Select as many as you like.</p>
<div class="choices">
<div class="choice"><input type="checkbox" name="snack" id="s1" value="Popcorn" checked><label for="s1"><span>🍿</span> Popcorn</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s2" value="Chocolate"><label for="s2"><span>🍫</span> Chocolate</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s3" value="Crisps"><label for="s3"><span>🥔</span> Crisps</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s4" value="Pizza"><label for="s4"><span>🍕</span> Pizza</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s5" value="Biscuits"><label for="s5"><span>🍪</span> Biscuits</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s6" value="Ice cream"><label for="s6"><span>🍨</span> Ice cream</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s7" value="Sausages"><label for="s7"><span>🌭</span> Sausages</label></div>
<div class="choice"><input type="checkbox" name="snack" id="s8" value="Sweets"><label for="s8"><span>🍬</span> Sweets</label></div>
</div>
<label class="field" for="otherSnacks">ANY OTHER SNACKS?</label><input id="otherSnacks" type="text" placeholder="Tell me what you're craving">
<label class="field">WHAT WOULD YOU LIKE TO DRINK?</label><div class="choices">
<div class="choice"><input type="radio" name="drink" id="d1" value="Juice" checked><label for="d1">🧃 Juice</label></div>
<div class="choice"><input type="radio" name="drink" id="d2" value="Soda"><label for="d2">🥤 Soda</label></div>
<div class="choice"><input type="radio" name="drink" id="d3" value="Water"><label for="d3">💧 Water</label></div>
<div class="choice"><input type="radio" name="drink" id="d4" value="Milkshake"><label for="d4">🥛 Milkshake</label></div>
<div class="choice"><input type="radio" name="drink" id="d5" value="Surprise me"><label for="d5">🎁 Surprise me</label></div>
</div>
</div>
<div class="step">
<h2>Make it your kind of evening.</h2><p class="hint">What atmosphere would make you happiest?</p>
<div class="choices">
<div class="choice wide"><input type="radio" name="vibe" id="b1" value="Cosy and relaxed" checked><label for="b1"><span>🛋️</span> Cosy and relaxed</label></div>
<div class="choice wide"><input type="radio" name="vibe" id="b2" value="Fun and playful"><label for="b2"><span>😂</span> Fun and playful</label></div>
<div class="choice wide"><input type="radio" name="vibe" id="b3" value="Romantic"><label for="b3"><span>❤️</span> Romantic</label></div>
<div class="choice wide"><input type="radio" name="vibe" id="b4" value="Simple and spontaneous"><label for="b4"><span>✨</span> Simple and spontaneous</label></div>
</div>
<label class="field" for="requests">WHAT ELSE WOULD YOU LIKE?</label><textarea id="requests" placeholder="Anything you'd love me to prepare? Anything you would prefer we avoid? Your comfort matters."></textarea>
</div>
<div class="step">
<h2>Our movie night plan. ♥</h2><p class="hint">Here's what you've picked. Review it, then send your choices back to me.</p>
<div class="summary" id="summary"></div>
<p class="note">This is a suggested plan, not a booking. We'll confirm the details together.</p>
<button class="btn primary" type="button" id="shareBtn" style="width:100%;margin-top:14px">Share my choices ↗</button>
<button class="btn secondary" type="button" id="copyBtn" style="width:100%;margin-top:9px">Copy my date plan</button>
<div class="success" id="success">Copied! You can now paste your date plan into a message.</div>
</div>
<div class="nav"><button class="btn secondary" type="button" id="back" disabled>← Back</button><button class="btn primary" type="button" id="next">Continue →</button></div>
</form>
</section>
<footer>Made with a little thought and a lot of ❤️</footer>
</main>
<script>
const steps=[...document.querySelectorAll('.step')], bars=[...document.querySelectorAll('.progress span')],back=document.getElementById('back'),next=document.getElementById('next');let current=0;
function val(name){return document.querySelector(`[name="${name}"]:checked`)?.value||'Not selected'}
function selected(name){return [...document.querySelectorAll(`[name="${name}"]:checked`)].map(x=>x.value)}
function data(){let snacks=selected('snack');let extra=document.getElementById('otherSnacks').value.trim();if(extra)snacks.push(extra);let venue=val('venue');let other=document.getElementById('venueOther').value.trim();if(other)venue+=' — '+other;return {date:document.getElementById('date').value||'To be decided',time:val('time'),venue,genre:val('genre'),movie:document.getElementById('movie').value.trim()||'To be decided',snacks:snacks.join(', ')||'To be decided',drink:val('drink'),vibe:val('vibe'),requests:document.getElementById('requests').value.trim()||'None added'}}
function message(d){return `🎬 OUR MOVIE NIGHT DATE ❤️\nDate: ${d.date}\nTime: ${d.time}\nVenue: ${d.venue}\nGenre: ${d.genre}\nMovie: ${d.movie}\nSnacks: ${d.snacks}\nDrink: ${d.drink}\nVibe: ${d.vibe}\nOther wishes: ${d.requests}\n\nLet's confirm the plan together!`}
function renderSummary(){let d=data();let rows=[['Date',d.date],['Time',d.time],['Venue',d.venue],['Movie mood',d.genre],['Movie title',d.movie],['Snacks',d.snacks],['Drink',d.drink],['Atmosphere',d.vibe],['Special requests',d.requests]];document.getElementById('summary').innerHTML='<h3>A little evening to look forward to</h3>'+rows.map(([a,b])=>`<div class="row"><b>${a}</b><span>${escapeHtml(b)}</span></div>`).join('')}
function escapeHtml(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
function show(){steps.forEach((s,i)=>s.classList.toggle('active',i===current));bars.forEach((b,i)=>b.classList.toggle('active',i<=current));back.disabled=current===0;next.style.display=current===steps.length-1?'none':'inline-block';if(current===steps.length-1)renderSummary();window.scrollTo({top:0,behavior:'smooth'})}
next.addEventListener('click',()=>{if(current===0&&!document.getElementById('date').value){document.getElementById('date').focus();return}if(current<steps.length-1){current++;show()}});
back.addEventListener('click',()=>{if(current>0){current--;show()}});
async function copyPlan(){try{await navigator.clipboard.writeText(message(data()));document.getElementById('success').style.display='block'}catch(e){alert(message(data()))}}
document.getElementById('copyBtn').addEventListener('click',copyPlan);
document.getElementById('shareBtn').addEventListener('click',async()=>{let text=message(data());if(navigator.share){try{await navigator.share({title:'Our Movie Night Date',text})}catch(e){}}else{await copyPlan()}});
const today=new Date();today.setMinutes(today.getMinutes()-today.getTimezoneOffset());document.getElementById('date').min=today.toISOString().slice(0,10);
</script>
</body></html>
