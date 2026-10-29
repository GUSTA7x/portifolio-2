<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>MathClass Hub — Portfólio do Projeto</title>
<!--
  COMO USAR AS IMAGENS (duas opções)
  A) Clique em qualquer quadro cinza e escolha a foto no seu computador/celular.
     Ela fica salva neste navegador.
  B) Para uma versão definitiva, crie a pasta "imagens" ao lado deste arquivo e
     salve os arquivos com os nomes que aparecem nos quadros (ex.: imagens/tela-login.png).
     Se o arquivo existir, ele aparece sozinho.
-->
<style>
:root{--bg:#f6f4ee;--card:#fff;--ink:#16202e;--muted:#5b6575;--line:#e0dccf;--navy:#0f1b2d;--navy2:#1a2a42;--amber:#f2b134;--blue:#1f5fbf;--ph:#e8e4d6;--ok:#2e8b57}
@media (prefers-color-scheme:dark){:root{--bg:#0b1422;--card:#14233a;--ink:#f3efe4;--muted:#a9b6c9;--line:#27385a;--blue:#7fb0ff;--ph:#1d2f4c}}
*{box-sizing:border-box;margin:0}
body{font-family:Arial,Helvetica,sans-serif;background:var(--bg);color:var(--ink);line-height:1.55}
header{background:var(--navy);color:#f3efe4;position:sticky;top:0;z-index:5}
.bar{max-width:1100px;margin:auto;padding:12px 20px;display:flex;flex-wrap:wrap;gap:12px;align-items:center;justify-content:space-between}
.brand{font-weight:700;font-size:20px}.brand span{color:var(--amber)}
nav{display:flex;flex-wrap:wrap;gap:6px}
nav a{color:#c9d4e4;text-decoration:none;padding:8px 14px;border-radius:999px;font-size:15px}
nav a:hover{background:var(--navy2)}nav a.on{background:var(--amber);color:var(--navy);font-weight:700}
main{max-width:1100px;margin:auto;padding:32px 20px 64px}
section.tab{display:none}section.tab.on{display:block}
h1{font-size:clamp(34px,6vw,60px);line-height:1.1}h2{font-size:30px;margin:0 0 8px}h3{font-size:19px;margin-bottom:6px}
.lead{font-size:19px;color:var(--muted);max-width:720px;margin:12px 0 24px}
.hero{background:var(--navy);color:#f3efe4;border-radius:20px;padding:48px 32px;margin-bottom:32px}
.hero .lead{color:#c9d4e4}.tag{color:var(--amber);font-weight:700;letter-spacing:1px;font-size:13px}
.btn{display:inline-block;background:var(--amber);color:var(--navy);padding:12px 20px;border-radius:10px;font-weight:700;text-decoration:none;border:0;cursor:pointer;font-size:15px}
.btn.ghost{background:var(--card);color:var(--ink);border:1px solid var(--line)}
.btn.sm{padding:8px 14px;font-size:14px}
.grid{display:grid;gap:20px;grid-template-columns:repeat(auto-fit,minmax(240px,1fr))}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:22px}
.stat{font-size:52px;font-weight:700;color:var(--blue);line-height:1}
.src{font-size:13px;color:var(--muted);margin-top:10px}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin:10px 0 0}
.chip{background:var(--card);border:1px solid var(--line);padding:6px 12px;border-radius:999px;font-size:14px}
/* imagens */
.shot{position:relative;background:var(--ph);border:2px dashed var(--muted);border-radius:14px;aspect-ratio:16/10;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:12px;color:var(--muted);font-size:14px;overflow:hidden;cursor:pointer;transition:border-color .15s}
.shot:hover,.shot:focus-visible{border-color:var(--amber);outline:none}
.shot b{display:block;font-size:15px;color:var(--ink)}
.shot small{display:block;margin-top:4px}
.shot img{width:100%;height:100%;object-fit:cover;display:block}
.shot.has{border:0;padding:0}
.shot .tools{position:absolute;top:8px;right:8px;display:none;gap:6px}
.shot.has:hover .tools,.shot.has:focus-within .tools{display:flex}
.shot .tools button{background:rgba(15,27,45,.85);color:#fff;border:0;border-radius:8px;padding:5px 10px;font-size:13px;cursor:pointer}
@media (hover:none){.shot.has .tools{display:flex}}
.round{aspect-ratio:1/1;border-radius:50%;width:120px;margin:0 auto 12px}
.round .tools{top:auto;bottom:6px;right:auto;left:50%;transform:translateX(-50%)}
.sec{margin-top:40px}
/* campos editáveis */
.fill{background:#fff3b0;color:#3b3200;padding:1px 6px;border-radius:4px;display:inline-block;min-width:90px;cursor:text;outline:none}
.fill:focus{box-shadow:0 0 0 3px var(--amber)}
.fill.filled{background:transparent;color:inherit;padding:1px 0}
.fill.filled:hover{background:#fff3b0;color:#3b3200}
.hint{font-size:13px;color:var(--muted);margin-top:6px}
/* kanban */
.board{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));align-items:start}
.col{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:14px;min-height:140px}
.col h3{display:flex;justify-content:space-between}.col.over{outline:3px dashed var(--amber)}
.k{background:var(--bg);border:1px solid var(--line);border-radius:10px;padding:10px 12px;margin-top:10px;cursor:grab;font-size:15px}
.k .acts{display:flex;gap:6px;margin-top:8px}.k button{border:1px solid var(--line);background:var(--card);color:var(--ink);border-radius:6px;padding:2px 9px;cursor:pointer;font-size:14px}
.add{display:flex;gap:8px;margin:0 0 20px;flex-wrap:wrap}
.add input,.inp{flex:1;min-width:200px;padding:11px 14px;border-radius:10px;border:1px solid var(--line);background:var(--card);color:var(--ink);font-size:15px}
.bar2{height:10px;border-radius:99px;background:var(--line);overflow:hidden;margin:6px 0 4px}
.bar2 i{display:block;height:100%;background:var(--ok);width:0;transition:width .25s}
/* checklist */
ul.chk{list-style:none;padding:0}ul.chk li{padding:8px 0;border-bottom:1px solid var(--line);display:flex;gap:10px;align-items:center;justify-content:space-between}
ul.chk label{flex:1;cursor:pointer}ul.chk input[type=checkbox]{margin-right:10px;width:18px;height:18px;vertical-align:middle}
ul.chk li.done label{text-decoration:line-through;color:var(--muted)}
.x{border:0;background:none;color:var(--muted);cursor:pointer;font-size:16px;padding:4px 8px}
/* roteiro e cronômetro */
.timer{font-size:44px;font-weight:700;font-variant-numeric:tabular-nums;color:var(--blue)}
ol.steps{padding-left:22px}ol.steps li{padding:4px 8px;border-radius:8px;margin:2px 0}
ol.steps li.now{background:#fff3b0;color:#3b3200;font-weight:700}
/* faq */
details{border-bottom:1px solid var(--line);padding:9px 0}
summary{cursor:pointer;font-weight:700}
details p{margin-top:6px;color:var(--muted)}
#qr{display:flex;justify-content:center;padding:10px;background:#fff;border-radius:12px;min-height:160px;align-items:center;color:#555;font-size:13px;text-align:center}
#qr img,#qr canvas{max-width:100%;height:auto}
footer{text-align:center;color:var(--muted);font-size:14px;padding:24px}
footer button{background:none;border:0;color:var(--muted);text-decoration:underline;cursor:pointer;font-size:13px;margin-top:6px}
@media print{header,.add,.tools,footer button{display:none}section.tab{display:block!important;page-break-after:always}}
</style>
</head>
<body>
<header><div class="bar">
  <div class="brand">MathClass <span>Hub</span></div>
  <nav id="nav">
    <a href="#inicio">Início</a><a href="#problema">O problema</a><a href="#solucao">A solução</a>
    <a href="#kanban">Kanban</a><a href="#equipe">Equipe</a><a href="#feira">Feira de Ciências</a>
  </nav>
</div></header>

<main>
<!-- INÍCIO -->
<section class="tab" id="t-inicio">
  <div class="hero">
    <p class="tag">TRABALHO DE CONCLUSÃO DE CURSO · DESENVOLVIMENTO DE SISTEMAS</p>
    <h1>MathClass Hub</h1>
    <p class="lead">Um site educacional que centraliza tarefas e materiais de matemática para professores e alunos do Ensino Médio.</p>
    <a class="btn" href="#solucao">Ver o projeto</a>
  </div>
  <div class="grid">
    <div class="card"><h3>Escola</h3><p>Escola Estadual Culto à Ciência, Campinas-SP, 2026.</p></div>
    <div class="card"><h3>Orientação</h3><p>Orientador: Aparecido da Silva<br>Coorientador: Lucas Pontes</p></div>
    <div class="card"><h3>Tecnologias</h3>
      <div class="chips"><span class="chip">HTML</span><span class="chip">CSS</span><span class="chip">JavaScript</span><span class="chip">Firebase Authentication</span><span class="chip">Cloud Firestore</span><span class="chip">GitHub</span><span class="chip">VS Code</span></div></div>
  </div>
  <p class="hint" style="margin-top:16px">Dica: clique em qualquer quadro cinza para adicionar uma imagem.</p>
  <div class="sec grid">
    <figure class="shot" data-src="imagens/capa.png" data-label="Imagem de destaque do projeto"></figure>
    <figure class="shot" data-src="imagens/logo-projeto.png" data-label="Logo do MathClass Hub"></figure>
  </div>
</section>

<!-- PROBLEMA -->
<section class="tab" id="t-problema">
  <h2>O problema</h2>
  <p class="lead">A matemática é o ponto mais frágil da aprendizagem no Brasil, e na rotina da escola as atividades ficam espalhadas em cadernos, grupos de mensagens e anotações avulsas.</p>
  <div class="grid">
    <div class="card"><div class="stat">73%</div><p>dos estudantes brasileiros de 15 anos não alcançam o nível básico em matemática.</p><p class="src">Fonte: Pisa 2022 (OCDE / Inep)</p></div>
    <div class="card"><div class="stat">379 × 479</div><p>pontos: Brasil contra a média da OCDE em matemática.</p><p class="src">Fonte: Pisa 2022 (OCDE / Inep)</p></div>
    <div class="card"><div class="stat">27% × 69%</div><p>dos alunos no nível básico ou acima: Brasil contra a média da OCDE.</p><p class="src">Fonte: Pisa 2022 (OCDE / Inep)</p></div>
  </div>
  <div class="sec grid">
    <div class="card"><h3>Na rotina da escola</h3><p>O aluno perde prazos e o professor perde o controle do que já foi passado para cada série.</p></div>
    <figure class="shot" data-src="imagens/problema.jpg" data-label="Foto ilustrando o problema (cadernos, grupos de mensagens)"></figure>
  </div>
</section>

<!-- SOLUÇÃO -->
<section class="tab" id="t-solucao">
  <h2>A solução</h2>
  <p class="lead">Um único ambiente organizado por série e por frequência de entrega, com área exclusiva do professor.</p>
  <div class="grid">
    <div class="card"><h3>Portal do aluno</h3><p>Acesso por série (1ª, 2ª e 3ª), sem senha.</p></div>
    <div class="card"><h3>Portal do professor</h3><p>Login pelo Firebase Authentication para cadastrar, editar e excluir.</p></div>
    <div class="card"><h3>Gerenciador de tarefas</h3><p>Diária, semanal, mensal ou bimestral, com indicador de prazo.</p></div>
    <div class="card"><h3>Apoio ao estudo</h3><p>Fórmulas e dicas, vídeo-aulas e recados.</p></div>
  </div>
  <h2 class="sec">Telas do site</h2>
  <div class="grid">
    <figure class="shot" data-src="imagens/tela-login.png" data-label="Tela de login / escolha de portal"></figure>
    <figure class="shot" data-src="imagens/tela-aluno.png" data-label="Portal do aluno"></figure>
    <figure class="shot" data-src="imagens/tela-professor.png" data-label="Painel do professor"></figure>
    <figure class="shot" data-src="imagens/tela-tarefas.png" data-label="Quadro de tarefas"></figure>
    <figure class="shot" data-src="imagens/tela-videos.png" data-label="Vídeo-aulas"></figure>
    <figure class="shot" data-src="imagens/tela-dicas.png" data-label="Dicas e fórmulas"></figure>
  </div>
</section>

<!-- KANBAN -->
<section class="tab" id="t-kanban">
  <h2>Kanban do projeto</h2>
  <p class="lead">Como o grupo organizou o trabalho. Arraste os cartões entre as colunas ou use as setas. Clique duas vezes no texto para editar. Tudo fica salvo neste navegador.</p>
  <div class="card" style="margin-bottom:20px">
    <strong id="kpText">0% concluído</strong>
    <div class="bar2"><i id="kpBar"></i></div>
  </div>
  <div class="add"><input id="novo" placeholder="Nova tarefa do projeto..."><button class="btn" id="addBtn">Adicionar</button><button class="btn ghost" id="resetBtn">Restaurar exemplo</button></div>
  <div class="board" id="board"></div>
</section>

<!-- EQUIPE -->
<section class="tab" id="t-equipe">
  <h2>Equipe</h2>
  <p class="lead">Alunos do curso de Desenvolvimento de Sistemas da Escola Estadual Culto à Ciência. Clique na função para escrever a sua e na bolinha para colocar a foto.</p>
  <div class="grid">
    <div class="card" style="text-align:center"><figure class="shot round" data-src="imagens/danilo.jpg" data-label="Foto"></figure><h3>Danilo Hernandes Ferreira</h3><p><span class="fill" data-ph="função no projeto"></span></p></div>
    <div class="card" style="text-align:center"><figure class="shot round" data-src="imagens/felipe.jpg" data-label="Foto"></figure><h3>Felipe da Silva Alves</h3><p><span class="fill" data-ph="função no projeto"></span></p></div>
    <div class="card" style="text-align:center"><figure class="shot round" data-src="imagens/gustavo.jpg" data-label="Foto"></figure><h3>Gustavo dos Santos Guide</h3><p><span class="fill" data-ph="função no projeto"></span></p></div>
    <div class="card" style="text-align:center"><figure class="shot round" data-src="imagens/leonardo.jpg" data-label="Foto"></figure><h3>Leonardo Gonçalves Passini</h3><p><span class="fill" data-ph="função no projeto"></span></p></div>
  </div>
  <div class="sec grid">
    <div class="card"><h3>Orientador</h3><p>Aparecido da Silva</p></div>
    <div class="card"><h3>Coorientador</h3><p>Lucas Pontes</p></div>
  </div>
</section>

<!-- FEIRA -->
<section class="tab" id="t-feira">
  <h2>Feira de Ciências</h2>
  <p class="lead">Tudo o que o grupo precisa para apresentar o MathClass Hub na feira. Clique nos campos amarelos para preencher.</p>
  <div class="grid">
    <div class="card"><h3>Data e horário</h3><p><span class="fill" data-ph="dd/mm/aaaa, hh:mm"></span></p></div>
    <div class="card"><h3>Local</h3><p><span class="fill" data-ph="sala / estande"></span></p></div>
    <div class="card"><h3>Acesse o site</h3>
      <div id="qr">Cole o link do site abaixo e clique em Gerar.</div>
      <div class="add" style="margin:10px 0 0"><input class="inp" id="qrUrl" placeholder="https://seu-site.web.app" style="min-width:120px"><button class="btn sm" id="qrBtn">Gerar</button></div>
      <p class="hint">Dica: clique com o botão direito no QR code para salvar a imagem e imprimir.</p>
    </div>
  </div>
  <div class="sec grid">
    <div class="card"><h3>Roteiro de 2 minutos</h3>
      <div class="timer" id="tm">02:00</div>
      <div style="display:flex;gap:8px;margin:8px 0 12px;flex-wrap:wrap">
        <button class="btn sm" id="tmGo">Iniciar</button><button class="btn sm ghost" id="tmReset">Zerar</button>
      </div>
      <ol class="steps" id="steps"><li>O problema: 73% dos jovens sem o básico em matemática.</li><li>Na escola: tarefas espalhadas e prazos perdidos.</li><li>Demonstração: entrar como aluno e como professor.</li><li>Resultado: testes com professor e alunos.</li><li>Próximos passos: fórum e medalhas.</li></ol></div>
    <div class="card"><h3>Perguntas que podem aparecer</h3>
      <p class="hint" style="margin:0 0 8px">Clique na pergunta para ver a resposta sugerida.</p>
      <details><summary>Por que o aluno entra sem senha?</summary><p>Para ser rápido: o aluno só escolhe a série e vê as tarefas. Só o professor precisa de login, porque é ele quem cadastra, edita e exclui.</p></details>
      <details><summary>Onde ficam os dados?</summary><p>No Firebase: o login usa o Firebase Authentication e as tarefas ficam no Cloud Firestore.</p></details>
      <details><summary>Quem testou o site?</summary><p>O professor Lucas e dois grupos de alunos testaram o site durante o desenvolvimento.</p></details>
      <details><summary>Funciona no celular?</summary><p>Sim, o site é feito em HTML, CSS e JavaScript e roda no navegador. Confirme antes da feira e ajuste esta resposta se precisar.</p></details>
    </div>
  </div>
  <h2 class="sec">Estande e fotos</h2>
  <div class="grid">
    <figure class="shot" data-src="imagens/feira-banner.jpg" data-label="Banner / painel do estande"></figure>
    <figure class="shot" data-src="imagens/feira-demo.jpg" data-label="Foto da demonstração"></figure>
    <figure class="shot" data-src="imagens/feira-equipe.jpg" data-label="Foto da equipe na feira"></figure>
  </div>
  <h2 class="sec">Checklist do dia</h2>
  <div class="card">
    <strong id="ckText">0 de 0</strong>
    <div class="bar2"><i id="ckBar"></i></div>
    <ul class="chk" id="chk"></ul>
    <div class="add" style="margin:14px 0 0"><input id="ckNew" placeholder="Novo item do checklist..."><button class="btn sm" id="ckAdd">Adicionar</button></div>
  </div>
</section>
</main>
<footer>MathClass Hub · Escola Estadual Culto à Ciência · Campinas-SP · 2026<br><button id="wipe">Apagar tudo que foi salvo neste navegador</button></footer>

<input type="file" id="picker" accept="image/*" hidden>

<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<script>
// ===== armazenamento seguro =====
var P='mch-';
function ld(k,d){try{var v=localStorage.getItem(P+k);return v===null?d:JSON.parse(v)}catch(e){return d}}
function sv(k,v){try{localStorage.setItem(P+k,JSON.stringify(v));return true}catch(e){return false}}

// ===== abas (usa o #hash) =====
var TABS=['inicio','problema','solucao','kanban','equipe','feira'];
function show(){
  var h=(location.hash||'#inicio').slice(1);if(TABS.indexOf(h)<0)h='inicio';
  TABS.forEach(function(t){document.getElementById('t-'+t).classList.toggle('on',t===h)});
  document.querySelectorAll('#nav a').forEach(function(a){a.classList.toggle('on',a.getAttribute('href')==='#'+h)});
  window.scrollTo(0,0);
}
window.addEventListener('hashchange',show);show();

// ===== imagens: upload, arquivo da pasta ou quadro cinza =====
var picker=document.getElementById('picker'),current=null;
function shrink(file,cb){
  var r=new FileReader();
  r.onload=function(){var im=new Image();im.onload=function(){
    var m=1000,s=Math.min(1,m/Math.max(im.width,im.height));
    var c=document.createElement('canvas');c.width=Math.round(im.width*s);c.height=Math.round(im.height*s);
    c.getContext('2d').drawImage(im,0,0,c.width,c.height);cb(c.toDataURL('image/jpeg',.82))};
    im.onerror=function(){alert('Não consegui abrir essa imagem.')};im.src=r.result};
  r.readAsDataURL(file);
}
function initShot(f){
  var src=f.dataset.src,label=f.dataset.label||'Imagem',round=f.classList.contains('round');
  f.tabIndex=0;f.setAttribute('role','button');f.setAttribute('aria-label',label+' — clique para escolher uma imagem');
  function placeholder(){
    f.classList.remove('has');
    f.innerHTML='<b>'+label+'</b>'+(round?'':'<small>Clique para adicionar<br>ou use: '+src+'</small>');
  }
  function showImg(url,canRemove){
    var img=new Image();img.alt=label;
    img.onload=function(){f.innerHTML='';f.appendChild(img);f.classList.add('has');
      var t=document.createElement('div');t.className='tools';
      var b1=document.createElement('button');b1.textContent='Trocar';
      b1.onclick=function(e){e.stopPropagation();open()};
      t.appendChild(b1);
      if(canRemove){var b2=document.createElement('button');b2.textContent='Remover';
        b2.onclick=function(e){e.stopPropagation();try{localStorage.removeItem(P+'img-'+src)}catch(x){};load()};t.appendChild(b2)}
      f.appendChild(t)};
    img.onerror=function(){if(canRemove){try{localStorage.removeItem(P+'img-'+src)}catch(x){}}placeholder()};
    img.src=url;
  }
  function load(){var s=ld('img-'+src,null);placeholder();if(s)showImg(s,true);else showImg(src,false)}
  function open(){current={f:f,src:src,load:load};picker.value='';picker.click()}
  f.onclick=open;
  f.onkeydown=function(e){if(e.key==='Enter'||e.key===' '){e.preventDefault();open()}};
  f._load=load;load();
}
picker.onchange=function(){
  var file=picker.files[0];if(!file||!current)return;var c=current;
  shrink(file,function(url){
    if(!sv('img-'+c.src,url)){alert('A imagem não coube na memória do navegador. Tente uma foto menor ou salve na pasta "imagens".');return}
    c.load()});
};
document.querySelectorAll('.shot').forEach(initShot);

// ===== campos editáveis (amarelos) =====
var fills=ld('fill',{});
document.querySelectorAll('.fill').forEach(function(el,i){
  var ph=el.dataset.ph||'clique para editar';
  el.contentEditable='true';el.spellcheck=false;
  function paint(){var t=el.textContent.trim();if(!t){el.textContent=ph;el.classList.remove('filled')}else el.classList.add('filled')}
  if(fills[i])el.textContent=fills[i];else el.textContent=ph;
  if(fills[i])el.classList.add('filled');
  el.onfocus=function(){if(!el.classList.contains('filled')){el.textContent=''}};
  el.onblur=function(){var t=el.textContent.trim();if(t===ph)t='';fills[i]=t;sv('fill',fills);paint()};
  el.onkeydown=function(e){if(e.key==='Enter'){e.preventDefault();el.blur()}};
});

// ===== kanban =====
var COLS=[['todo','A fazer'],['doing','Em andamento'],['done','Concluído']];
var DEF=[
 {t:'Aplicar questionário aos alunos',c:'todo'},{t:'Fórum de dúvidas',c:'todo'},{t:'Medalhas e pontuações',c:'todo'},{t:'Notificações de prazo',c:'todo'},
 {t:'Finalizar o TCC escrito (ABNT)',c:'doing'},{t:'Preparar a apresentação',c:'doing'},{t:'Montar o estande da feira',c:'doing'},
 {t:'Definir funcionalidades e áreas (professor e aluno)',c:'done'},{t:'Estrutura das páginas em HTML',c:'done'},{t:'Interface em CSS',c:'done'},
 {t:'Lógica em JavaScript',c:'done'},{t:'Firebase: login e banco de dados',c:'done'},{t:'Testes com o professor Lucas e dois grupos de alunos',c:'done'}
];
function fresh(){return DEF.map(function(x){return{t:x.t,c:x.c}})}
var cards=ld('kanban',null);if(!cards)cards=fresh();
function saveK(){sv('kanban',cards)}
function progress(){
  var d=cards.filter(function(k){return k.c==='done'}).length,p=cards.length?Math.round(d/cards.length*100):0;
  document.getElementById('kpText').textContent=p+'% concluído ('+d+' de '+cards.length+' tarefas)';
  document.getElementById('kpBar').style.width=p+'%';
}
function render(){
  var b=document.getElementById('board');b.innerHTML='';
  COLS.forEach(function(col,ci){
    var d=document.createElement('div');d.className='col';
    var n=cards.filter(function(k){return k.c===col[0]}).length;
    d.innerHTML='<h3>'+col[1]+'<span>'+n+'</span></h3>';
    cards.forEach(function(k,i){
      if(k.c!==col[0])return;
      var e=document.createElement('div');e.className='k';e.draggable=true;
      var tx=document.createElement('div');tx.textContent=k.t;tx.title='Clique duas vezes para editar';
      tx.ondblclick=function(){var v=prompt('Editar tarefa:',k.t);if(v&&v.trim()){k.t=v.trim();saveK();render()}};
      e.appendChild(tx);
      var a=document.createElement('div');a.className='acts';
      [['←',-1],['→',1],['✕',0]].forEach(function(p){
        var bt=document.createElement('button');bt.textContent=p[0];
        bt.setAttribute('aria-label',p[0]==='✕'?'Excluir':p[0]==='←'?'Mover para a esquerda':'Mover para a direita');
        bt.onclick=function(){
          if(p[1]===0)cards.splice(i,1);else{var ni=ci+p[1];if(ni<0||ni>2)return;k.c=COLS[ni][0]}
          saveK();render()};
        a.appendChild(bt)});
      e.appendChild(a);
      e.ondragstart=function(ev){ev.dataTransfer.setData('text/plain',String(i))};
      d.appendChild(e)});
    d.ondragover=function(ev){ev.preventDefault();d.classList.add('over')};
    d.ondragleave=function(){d.classList.remove('over')};
    d.ondrop=function(ev){ev.preventDefault();d.classList.remove('over');
      var i=parseInt(ev.dataTransfer.getData('text/plain'),10);if(cards[i]){cards[i].c=col[0];saveK();render()}};
    b.appendChild(d)});
  progress();
}
function addK(){var i=document.getElementById('novo'),v=i.value.trim();if(!v)return;cards.push({t:v,c:'todo'});i.value='';saveK();render()}
document.getElementById('addBtn').onclick=addK;
document.getElementById('novo').onkeydown=function(e){if(e.key==='Enter')addK()};
document.getElementById('resetBtn').onclick=function(){if(confirm('Voltar o Kanban para o exemplo original?')){cards=fresh();saveK();render()}};
render();

// ===== checklist =====
var CKDEF=['Notebook carregado e site aberto','Internet testada (Firebase precisa de conexão)','Login do professor anotado','Banner e QR code impressos','Cada integrante sabe sua parte da fala'];
var ck=ld('check',null);if(!ck)ck=CKDEF.map(function(t){return{t:t,d:false}});
function renderCk(){
  var ul=document.getElementById('chk');ul.innerHTML='';
  ck.forEach(function(it,i){
    var li=document.createElement('li');if(it.d)li.className='done';
    var lb=document.createElement('label'),cb=document.createElement('input');cb.type='checkbox';cb.checked=it.d;
    cb.onchange=function(){it.d=cb.checked;sv('check',ck);renderCk()};
    lb.appendChild(cb);lb.appendChild(document.createTextNode(it.t));
    var x=document.createElement('button');x.className='x';x.textContent='✕';x.setAttribute('aria-label','Remover item');
    x.onclick=function(){ck.splice(i,1);sv('check',ck);renderCk()};
    li.appendChild(lb);li.appendChild(x);ul.appendChild(li)});
  var d=ck.filter(function(c){return c.d}).length;
  document.getElementById('ckText').textContent=d+' de '+ck.length+' feitos'+(ck.length&&d===ck.length?' — tudo pronto!':'');
  document.getElementById('ckBar').style.width=(ck.length?d/ck.length*100:0)+'%';
}
function addCk(){var i=document.getElementById('ckNew'),v=i.value.trim();if(!v)return;ck.push({t:v,d:false});i.value='';sv('check',ck);renderCk()}
document.getElementById('ckAdd').onclick=addCk;
document.getElementById('ckNew').onkeydown=function(e){if(e.key==='Enter')addCk()};
renderCk();

// ===== QR code =====
var qrUrl=document.getElementById('qrUrl');qrUrl.value=ld('qrurl','');
function makeQr(){
  var u=qrUrl.value.trim(),box=document.getElementById('qr');
  if(!u){box.textContent='Cole o link do site abaixo e clique em Gerar.';return}
  if(typeof QRCode==='undefined'){box.textContent='Não consegui carregar o gerador de QR code (precisa de internet).';return}
  box.innerHTML='';new QRCode(box,{text:u,width:160,height:160});sv('qrurl',u);
}
document.getElementById('qrBtn').onclick=makeQr;
qrUrl.onkeydown=function(e){if(e.key==='Enter')makeQr()};
if(qrUrl.value)window.addEventListener('load',makeQr);

// ===== cronômetro do roteiro (2 min, 5 etapas) =====
var TOTAL=120,left=TOTAL,iv=null,tmEl=document.getElementById('tm'),go=document.getElementById('tmGo');
var stepEls=document.querySelectorAll('#steps li');
function drawT(){
  var m=Math.floor(left/60),s=left%60;tmEl.textContent=(m<10?'0':'')+m+':'+(s<10?'0':'')+s;
  var idx=left===TOTAL&&!iv?-1:Math.min(4,Math.floor((TOTAL-left)/(TOTAL/5)));
  stepEls.forEach(function(li,i){li.classList.toggle('now',i===idx)});
  tmEl.style.color=left<=10&&iv?'#d33':'';
}
function stop(){clearInterval(iv);iv=null;go.textContent=left===0||left===TOTAL?'Iniciar':'Continuar'}
go.onclick=function(){
  if(iv){stop();drawT();return}
  if(left===0)left=TOTAL;
  go.textContent='Pausar';
  iv=setInterval(function(){left--;if(left<=0){left=0;stop()}drawT()},1000);drawT();
};
document.getElementById('tmReset').onclick=function(){stop();left=TOTAL;go.textContent='Iniciar';drawT()};
drawT();

// ===== apagar dados salvos =====
document.getElementById('wipe').onclick=function(){
  if(!confirm('Isso apaga fotos, textos, kanban e checklist salvos neste navegador. Continuar?'))return;
  try{Object.keys(localStorage).forEach(function(k){if(k.indexOf(P)===0)localStorage.removeItem(k)})}catch(e){}
  location.reload();
};
</script>
</body>
</html>
