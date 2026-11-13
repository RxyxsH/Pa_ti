<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Para ti, te amo ❤️</title>
<style>
:root{--pink:#ed789f;--deep:#c84c78;--paper:#fffaf7;--ink:#8f435e}
*{box-sizing:border-box}
body{margin:0;min-height:100vh;overflow:hidden;background:#f8a0c0;color:var(--ink);font-family:Georgia,serif}
#bg{position:fixed;inset:0;overflow:hidden;z-index:-1;background:radial-gradient(circle at 20% 20%,#ffb9d2,#f57eae 48%,#e94e91)}
#bg:before{content:"";position:absolute;inset:-50%;background:radial-gradient(circle,#fff8 0 1px,transparent 2px);background-size:34px 34px;opacity:.45;animation:drift 35s linear infinite}
@keyframes drift{to{transform:translate(100px,80px)}}
.heart-bg{position:absolute;color:#fff8;animation:floatUp linear infinite;text-shadow:0 0 15px #fff8;user-select:none}
@keyframes floatUp{from{transform:translateY(110vh) rotate(0deg) scale(.7);opacity:0}15%{opacity:.8}to{transform:translateY(-15vh) rotate(35deg) scale(1.25);opacity:0}}
.spark{position:absolute;width:5px;height:5px;border-radius:50%;background:#fff;box-shadow:0 0 14px 5px #fff9;animation:twinkle 2s infinite alternate}
@keyframes twinkle{to{opacity:.2;transform:scale(.4)}}
.brand{position:fixed;top:22px;left:0;right:0;text-align:center;color:white;font:12px Arial,sans-serif;letter-spacing:2px;text-shadow:0 1px 8px #a52d63}
main{height:100svh;display:grid;place-items:center;padding:65px 15px 20px}
.panel{width:min(620px,94vw);min-height:min(440px,72vh);background:var(--paper);border-radius:24px;box-shadow:0 18px 55px #8c245544;position:relative;overflow:hidden;text-align:center;padding:32px 20px;display:flex;flex-direction:column;align-items:center;justify-content:center}
.panel:before,.panel:after{content:"";position:absolute;width:90px;height:90px;border:1px solid #f2c5d2;border-radius:50%;opacity:.4}
.panel:before{top:-55px;left:-40px}.panel:after{bottom:-55px;right:-40px}
h1{font-size:clamp(30px,6vw,48px);font-style:italic;font-weight:normal;color:#c77991;margin:0 0 12px;text-shadow:0 2px 2px #f5dbe3}
.sub{font-size:11px;letter-spacing:3px;color:#b8798b;margin:0 0 20px}
.fingerprint{width:116px;height:116px;border:1.5px solid #e99ab1;border-radius:50%;display:grid;place-items:center;margin:12px auto 10px;color:#db6f91;cursor:pointer;position:relative;background:radial-gradient(circle,#fff,#fff7fa);box-shadow:0 0 0 7px #f9e8ed,0 0 28px #efb6c8;transition:.3s}
.fingerprint svg{width:65px;height:65px;fill:none;stroke:currentColor;stroke-width:2;stroke-linecap:round}
.fingerprint:after{content:"";position:absolute;inset:-8px;border:2px solid transparent;border-top-color:#e56e98;border-radius:50%;animation:spin 2.5s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
.fingerprint.unlocked{color:#5caa83;border-color:#8bc6a5;box-shadow:0 0 30px #8bc6a5}
.hint{font-size:12px;color:#bd8799;font-style:italic;margin:10px 0 0}
.hidden{display:none!important}
button{border:0;border-radius:30px;padding:12px 23px;background:linear-gradient(100deg,#e987a5,#d85e89);color:white;letter-spacing:1px;font-size:11px;cursor:pointer;box-shadow:0 6px 18px #d65e8938;transition:.2s}
button:hover{transform:translateY(-2px);filter:brightness(1.05)}
#anniversary{animation:fadeIn .8s ease both}
@keyframes fadeIn{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
.date{font:10px Arial,sans-serif;letter-spacing:3px;color:#b47c8b;margin-top:-5px}
.envelope{width:190px;height:125px;margin:30px auto 18px;position:relative;cursor:pointer;filter:drop-shadow(0 8px 10px #bd718655);transition:transform .25s}
.envelope:hover{transform:translateY(-4px)}
.env-body{position:absolute;inset:0;background:linear-gradient(145deg,#fbe1e7,#f3c5d1);border:1px solid #efc1ce;border-radius:5px;overflow:hidden}
.env-left,.env-right,.env-bottom{position:absolute;width:0;height:0;border-style:solid}
.env-left{left:0;top:0;border-width:62px 95px 62px 0;border-color:transparent #f7d5de transparent transparent}
.env-right{right:0;top:0;border-width:62px 0 62px 95px;border-color:transparent transparent transparent #f9e0e6}
.env-bottom{bottom:0;left:0;border-width:0 95px 78px;border-color:transparent transparent #f4cbd6}
.env-flap{position:absolute;top:0;left:0;border-left:95px solid transparent;border-right:95px solid transparent;border-top:75px solid #f8dbe2;transform-origin:top;transition:transform .65s;z-index:2}
.seal{position:absolute;z-index:3;left:50%;top:51%;transform:translate(-50%,-50%);font-size:25px;color:#d96c8d;text-shadow:0 2px 5px white}
.envelope.opened .env-flap{transform:rotateX(180deg);z-index:0}
.envelope.opened{transform:translateY(12px) scale(.92);opacity:.4}
.click-note{font:12px Arial,sans-serif;color:#b77d8d}
.letter-modal{position:fixed;inset:0;background:#43132888;backdrop-filter:blur(4px);display:grid;place-items:center;padding:15px;z-index:5;animation:fadeIn .4s}
.letter{position:relative;width:min(420px,94vw);max-height:85vh;overflow:auto;background:#fffdfb;padding:30px 28px 25px;box-shadow:0 15px 50px #4e173744;border:1px solid #f0d9dc;text-align:left}
.letter:before{content:"";position:absolute;inset:9px;border:1px solid #f4e2e4;pointer-events:none}
.letter h2{text-align:center;font-style:italic;color:#b85e7d;font-size:27px;margin:5px 0 20px}
.letter p{font-size:14px;line-height:1.8;color:#795563;white-space:pre-line}
.signature{text-align:right!important;font-style:italic;color:#b85e7d!important;margin-top:22px}
.close{position:absolute;right:15px;top:12px;background:transparent;color:#b66b83;box-shadow:none;padding:4px 8px;font-size:20px;z-index:2}
.footer{font:10px Arial,sans-serif;color:#c08a9b;margin-top:15px;letter-spacing:1px}
@media(max-height:620px){.panel{min-height:0;padding:18px}.envelope{margin:14px auto 10px}.letter{padding:22px}.letter p{font-size:13px;line-height:1.6}}
</style>
</head>
<body>
<div id="bg"></div><div class="brand">Rxyxs_H</div>
<main>
<section class="panel">
 <div id="unlock">
  <h1>Para ti, Te Amo</h1>
  <p class="sub">UNA SORPRESA HECHA CON AMOR</p>
  <div class="fingerprint" id="fingerprint" role="button" tabindex="0" aria-label="Desbloquear con huella">
   <svg viewBox="0 0 64 64" aria-hidden="true">
    <path d="M13 28c0-11 8-19 19-19s19 8 19 19M18 31c0-8 6-14 14-14s14 6 14 14c0 10-2 18-6 25M24 32c0-5 3-8 8-8s8 3 8 8c0 9-1 15-4 21M30 34c0-2 1-3 2-3s2 1 2 3c0 7-1 12-3 16M8 32c0 10 2 18 6 24M56 32c0 7-1 13-3 18M19 42c1 5 2 8 4 11"/>
   </svg>
  </div>
  <p class="hint" id="hint">Coloca tu huella para descubrir la sorpresa...</p>
 </div>
 <div id="anniversary" class="hidden">
  <h1>Feliz Primer mes ♥</h1>
  <div class="date">UN DÍA ESPECIAL PARA NOSOTROS</div>
  <div class="envelope" id="envelope" role="button" tabindex="0" aria-label="Abrir carta">
   <div class="env-body"></div><div class="env-left"></div><div class="env-right"></div><div class="env-bottom"></div><div class="env-flap"></div><div class="seal">♥</div>
  </div>
  <p class="click-note">Toca el sobre para abrir tu carta</p>
  <div class="footer">HECHO CON TODO MI CARIÑO ♥</div>
 </div>
</section>
</main>
<div class="letter-modal hidden" id="letterModal">
 <article class="letter">
  <button class="close" id="close" aria-label="Cerrar">×</button>
  <h2>Mi Amorcito</h2>
  <p id="letterText">No sé cómo explicar lo mucho que significas para mí. Desde que llegaste a mi vida, incluso los momentos más sencillos tienen algo especial.

Gracias por tu cariño, por tu forma de ser y por cada sonrisa que me regalas. Me encanta seguir compartiendo momentos contigo y descubrir, poco a poco, todo lo bonito que podemos construir.

Hoy celebramos nuestra historia, nuestros recuerdos y todo lo que todavía nos falta vivir. Quiero seguir eligiéndote y cuidando esto tan bonito que tenemos.

Feliz Primer Mes, Mi Amorcito ❤️ Muaa xdd </p>
  <p class="signature">Siempre tuyo ♥</p>
 </article>
</div>
<script>
const bg=document.getElementById('bg');
for(let i=0;i<34;i++){
 const h=document.createElement('span');h.className='heart-bg';h.textContent=['♡','♥','❤'][i%3];
 h.style.left=Math.random()*100+'%';h.style.fontSize=(12+Math.random()*28)+'px';
 h.style.animationDuration=(9+Math.random()*14)+'s';h.style.animationDelay=(-Math.random()*20)+'s';bg.appendChild(h);
}
for(let i=0;i<30;i++){
 const s=document.createElement('i');s.className='spark';s.style.left=Math.random()*100+'%';s.style.top=Math.random()*100+'%';s.style.animationDelay=Math.random()*3+'s';bg.appendChild(s);
}
const fingerprint=document.getElementById('fingerprint');
function unlock(){
 fingerprint.classList.add('unlocked');
 document.getElementById('hint').textContent='¡Huella reconocida! Preparando tu sorpresa...';
 fingerprint.querySelector('svg').style.opacity='.35';
 setTimeout(()=>{
  document.getElementById('unlock').classList.add('hidden');
  document.getElementById('anniversary').classList.remove('hidden');
 },850);
}
fingerprint.addEventListener('click',unlock);
fingerprint.addEventListener('keydown',e=>{if(e.key==='Enter'||e.key===' '){e.preventDefault();unlock();}});
const envelope=document.getElementById('envelope');
function openLetter(){
 envelope.classList.add('opened');
 setTimeout(()=>document.getElementById('letterModal').classList.remove('hidden'),400);
}
envelope.addEventListener('click',openLetter);
envelope.addEventListener('keydown',e=>{if(e.key==='Enter'||e.key===' '){e.preventDefault();openLetter();}});
function closeLetter(){document.getElementById('letterModal').classList.add('hidden');envelope.classList.remove('opened');}
document.getElementById('close').addEventListener('click',closeLetter);
document.getElementById('letterModal').addEventListener('click',e=>{if(e.target.id==='letterModal')closeLetter();});
</script>
</body>
</html>
