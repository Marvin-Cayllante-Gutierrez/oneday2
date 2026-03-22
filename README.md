[virus-amor.html](https://github.com/user-attachments/files/26163070/virus-amor.html)
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Virus de Amor 😈❤️ - Piano Sonando</title>
  <style>
    body { margin:0; padding:0; background:#000; overflow:hidden; font-family:Arial,sans-serif; color:white; text-align:center; }
    .contenedor { position:relative; display:block; max-width:100%; margin:10px auto; border:6px solid #ff00ff; box-shadow:0 0 50px #ff00ff; }
    .contenedor img { width:100%; display:block; }

    .zona-gato-sol { position:absolute; top:12%; left:52%; width:28%; height:31%; cursor:pointer; z-index:10; }
    .zona-flor { position:absolute; top:53%; left:59%; width:32%; height:39%; cursor:pointer; z-index:10; }
    
    /* NUEVA ZONA: Casa con dos gatos en la colina (calibrada en la parte verde izquierda) */
    .zona-casa { 
      position:absolute; 
      top:60%; 
      left:12%; 
      width:22%; 
      height:26%; 
      cursor:pointer; 
      z-index:10; 
      display:flex; 
      flex-direction:column; 
      align-items:center; 
      justify-content:center; 
      font-size:48px; 
      line-height:1.05; 
      text-align:center; 
      color:#fff; 
      text-shadow:3px 3px 8px #000, 0 0 15px #ff0; 
    }

    .abeja { position:absolute; font-size:54px; z-index:15; cursor:pointer; animation:volar linear infinite; filter:drop-shadow(0 0 12px #ff0); }
    .abeja1 { top:8%; left:12%; animation-duration:8.5s; }
    .abeja2 { top:27%; left:73%; animation-duration:6.5s; animation-delay:1s; }
    .abeja3 { top:66%; left:19%; animation-duration:10.5s; animation-delay:2.5s; }
    @keyframes volar { 0%{transform:translate(0,0)rotate(0deg)} 50%{transform:translate(300px,-140px)rotate(-25deg)} 100%{transform:translate(0,0)rotate(0deg)} }

    .burbuja { position:absolute; background:rgba(255,255,255,0.95); color:#000; padding:18px 25px; border-radius:30px; font-size:1.35em; font-weight:bold; box-shadow:0 8px 20px rgba(0,0,0,0.7); max-width:320px; z-index:20; animation:aparecer 0.3s, desaparecer 4.5s forwards; pointer-events:none; text-align:center; white-space:pre-wrap; }
    .burbuja.especial { background:#ff69b4; color:white; font-size:1.6em; }
    @keyframes aparecer { from{opacity:0;transform:scale(0.7)} to{opacity:1;transform:scale(1)} }
    @keyframes desaparecer { to{opacity:0;transform:translateY(-40px)} }

    #btnMusica { position:fixed; top:8px; left:50%; transform:translateX(-50%); background:#ff1493; color:white; padding:15px 30px; font-size:1.5em; border:none; border-radius:50px; box-shadow:0 0 20px #ff00ff; z-index:100; cursor:pointer; width:90%; max-width:340px; }
  </style>
</head>
<body>

  <button id="btnMusica" onclick="iniciarMusica()">❤️ Toca aquí para que suene el piano romántico 🎹😍</button>

  <div class="contenedor">
    <img src="meme.jpg" alt="Gato Sol y Gato Flor">
    <div class="zona-gato-sol" onclick="tocarGatoSol(event)"></div>
    <div class="zona-flor" onclick="tocarFlor(event)"></div>
    
    <!-- NUEVA CASA CON GATOS EN LA COLINA -->
    <div class="zona-casa" onclick="tocarCasa(event)">
      🏡<br>
      <span style="font-size:0.65em;">🐈 🐈‍⬛</span>
    </div>
    
    <div class="abeja abeja1" onclick="tocarAbeja(this)">🐝</div>
    <div class="abeja abeja2" onclick="tocarAbeja(this)">🐝</div>
    <div class="abeja abeja3" onclick="tocarAbeja(this)">🐝</div>
  </div>

  <audio id="piano" loop preload="auto">
    <source src="https://files.catbox.moe/tglb30.mp3" type="audio/mpeg">
    <source src="https://cdn.pixabay.com/audio/2024/08/20/audio_85353d689c.mp3" type="audio/mpeg">
  </audio>

  <script>
    let audio = document.getElementById('piano');

    function iniciarMusica() {
      audio.volume = 0.62;
      audio.play().then(() => {
        document.getElementById('btnMusica').innerHTML = "🎵 ¡Música activada forever! ❤️ Sigue tocando 😈";
        document.getElementById('btnMusica').style.background = "#00ff7f";
        setTimeout(()=>{ document.getElementById('btnMusica').style.display = "none"; }, 2800);
      }).catch(() => { alert("✅ ¡Tocado! La música ya está lista ❤️"); });
    }

    window.onload = () => { audio.volume = 0.62; audio.play().catch(()=>{}); };

    const frases = [
      "lirios para mi delirio🫠😜!",
      "no lo sabes\nPero este archivo\ntiene virus 🗣️🔥👀",
      "Este archivo me da acceso a tu\nCORAZON 🌹\n(Y a tu dispositivo👻👻)",
      "MI AMOR ES IGUAL QUE π🔥\n¡Nunca termina!",
      "🐈‍⬛❤️🐈  Tú y yo forever",
      "🐈‍⬛🌹🐈  Gatos enamorados",
      "🐦 ¡Vuelo directo a tu corazón!",
      "Ay! ayyyyy! 😍💥",
      "Para mí eres tan especial ❤️",
      "Sabes cuánto te amo?\n¡Más que infinito! ♾️",
      "👀👻 Tiene virus... ¡de amor!",
      "Te veo mientras duermes <⁠(⁠￣⁠︶⁠￣⁠)⁠> 😘",
      "(⁠≧⁠▽⁠≦⁠) ¡Eres mi sonrisa favorita!",
      "⊂⁠(⁠◉⁠‿⁠◉⁠)⁠つ ¡Ven aquí que te abrazo fuerte!",
      "¡Eres mi virus favorito! 🦠❤️"
    ];

    function crearBurbuja(txt, x, y, esp=false) {
      const b = document.createElement('div');
      b.className = 'burbuja' + (esp?' especial':'');
      b.innerHTML = txt;
      b.style.left = (x-130)+'px';
      b.style.top = (y-100)+'px';
      document.body.appendChild(b);
      setTimeout(()=>b.remove(),5200);
    }

    function tocarGatoSol(e){ e.stopImmediatePropagation(); crearBurbuja('quisiera ser sol para verte todos los días❤️', e.clientX, e.clientY, true); }
    function tocarFlor(e){ e.stopImmediatePropagation(); crearBurbuja('te amo Liz ❤️<br><span style="font-size:0.85em;">(el gato flor te lo dice)</span>', e.clientX, e.clientY, true); }

    // NUEVA FUNCIÓN: Casa + gatos en la colina
    function tocarCasa(e){ 
      e.stopImmediatePropagation(); 
      crearBurbuja('¡MIAU MIAU! 🏡<br>🐈 y 🐈‍⬛ tosh dosh ❤️<br>¡Voziozi!', e.clientX, e.clientY, true); 
      playMeow();
    }

    function playMeow() {
      const ctx = new (window.AudioContext || window.webkitAudioContext)();
      const osc = ctx.createOscillator();
      osc.type = 'sine';
      const gain = ctx.createGain();
      const filter = ctx.createBiquadFilter();
      filter.type = 'lowpass';
      filter.frequency.value = 1800;

      osc.frequency.setValueAtTime(920, ctx.currentTime);
      osc.frequency.linearRampToValueAtTime(380, ctx.currentTime + 0.75);

      gain.gain.setValueAtTime(0.38, ctx.currentTime);
      gain.gain.linearRampToValueAtTime(0.02, ctx.currentTime + 1.25);

      osc.connect(filter);
      filter.connect(gain);
      gain.connect(ctx.destination);

      osc.start();
      setTimeout(() => { osc.stop(); }, 1400);
    }

    function tocarAbeja(el){ 
      el.style.transform = 'scale(2) rotate(40deg)'; setTimeout(()=>{el.style.transform='';},300);
      crearBurbuja('🐝 BZZZZZ! ❤️\n¡Me tocaste!', el.getBoundingClientRect().left + 30, el.getBoundingClientRect().top - 20, true);
      const a = new (window.AudioContext||window.webkitAudioContext)();
      const o = a.createOscillator(); o.type='sawtooth'; o.frequency.value=110;
      const g = a.createGain(); g.gain.value=0.4; o.connect(g); g.connect(a.destination); o.start();
      setTimeout(()=>{g.gain.linearRampToValueAtTime(0,a.currentTime+0.8); o.stop(a.currentTime+1);},50);
    }

    // Toque random (ahora excluye también la casa)
    document.addEventListener('click', e => {
      if(e.target.id === 'btnMusica') return;
      if(!e.target.classList.contains('abeja') && 
         !e.target.classList.contains('zona-gato-sol') && 
         !e.target.classList.contains('zona-flor') &&
         !e.target.classList.contains('zona-casa')){
        const random = frases[Math.floor(Math.random() * frases.length)];
        crearBurbuja(random, e.clientX, e.clientY);
      }
    });

    // Soporte móvil
    document.addEventListener('touchstart', ()=>{ if(audio.paused) audio.play(); });
  </script>

  <p style="margin-top:15px; color:#ff69b4; font-size:1em;">
    
  </p>
</body>
</html>![WhatsApp Image 2026-03-21 at 8 09 10 PM](https://github.com/user-attachments/assets/d670b172-aca1-450f-9551-02074cf5ee5b)
