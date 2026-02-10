<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Tu Local de Ropa | Moda urbana</title>
  <meta name="description" content="Local de ropa: nueva temporada, básicos y ofertas. Comprá online o visitanos." />
  <style>
    :root{
      --bg:#0b0c10;
      --card:#12141c;
      --muted:#9aa3b2;
      --text:#eef1f7;
      --brand:#7c5cff;
      --brand2:#2ee7a7;
      --border:rgba(255,255,255,.10);
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
      --max: 1100px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", "Helvetica Neue";
      background:
        radial-gradient(900px 450px at 20% -10%, rgba(124,92,255,.25), transparent 60%),
        radial-gradient(900px 450px at 80% -10%, rgba(46,231,167,.18), transparent 60%),
        var(--bg);
      color:var(--text);
      line-height:1.5;
    }
    a{color:inherit; text-decoration:none}
    img{max-width:100%; display:block}
    .container{width:min(var(--max), calc(100% - 32px)); margin:0 auto}
    .pill{display:inline-flex; align-items:center; gap:8px; padding:8px 12px; border:1px solid var(--border); border-radius:999px; color:var(--muted); font-size:12px; background:rgba(255,255,255,.03)}
    .btn{
      display:inline-flex; align-items:center; justify-content:center; gap:10px;
      padding:12px 16px; border-radius:12px; border:1px solid var(--border);
      background:rgba(255,255,255,.04); color:var(--text); font-weight:600;
      transition: transform .15s ease, background .15s ease, border-color .15s ease;
      cursor:pointer;
    }
    .btn:hover{transform: translateY(-1px); background:rgba(255,255,255,.06); border-color:rgba(255,255,255,.18)}
    .btn.primary{
      background: linear-gradient(135deg, var(--brand), #b57bff);
      border-color: transparent;
      color:#0b0c10;
    }
    .btn.primary:hover{filter: brightness(1.05)}
    .btn.ghost{background:transparent}
    header{
      position:sticky; top:0; z-index:20;
      backdrop-filter: blur(10px);
      background: rgba(11,12,16,.55);
      border-bottom:1px solid rgba(255,255,255,.06);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
    }
    .brand{
      display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.2px
    }
    .logo{
      width:38px; height:38px; border-radius:12px;
      background: conic-gradient(from 210deg, var(--brand), var(--brand2), #ff4fd8, var(--brand));
      box-shadow: var(--shadow);
    }
    nav ul{
      list-style:none; margin:0; padding:0;
      display:flex; gap:18px; align-items:center;
    }
    nav a{color:var(--muted); font-weight:600; font-size:14px}
    nav a:hover{color:var(--text)}
    .nav-actions{display:flex; gap:10px; align-items:center}
    .menu-btn{display:none}
    .hero{
      padding:56px 0 26px;
    }
    .hero-grid{
      display:grid; gap:22px;
      grid-template-columns: 1.1fr .9fr;
      align-items:stretch;
    }
    .hero-card{
      border:1px solid var(--border);
      background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border-radius: var(--radius);
      padding:26px;
      box-shadow: var(--shadow);
      position:relative;
      overflow:hidden;
    }
    .hero-card::after{
      content:"";
      position:absolute; inset:-2px;
      background:
        radial-gradient(500px 200px at 20% 10%, rgba(124,92,255,.35), transparent 60%),
        radial-gradient(500px 200px at 80% 30%, rgba(46,231,167,.20), transparent 60%);
      pointer-events:none;
      opacity:.9;
      mix-blend-mode: screen;
    }
    .hero-card > *{position:relative; z-index:1}
    h1{margin:10px 0 10px; font-size:42px; line-height:1.08}
    .subtitle{color:var(--muted); font-size:16px; max-width:56ch}
    .hero-actions{display:flex; gap:12px; flex-wrap:wrap; margin-top:16px}
    .hero-stats{display:flex; gap:16px; margin-top:18px; flex-wrap:wrap}
    .stat{
      border:1px solid var(--border);
      background:rgba(255,255,255,.03);
      border-radius:14px;
      padding:12px 14px;
      min-width:150px;
    }
    .stat b{display:block; font-size:16px}
    .stat span{color:var(--muted); font-size:12px}
    .showcase{
      border:1px solid var(--border);
      border-radius: var(--radius);
      background: rgba(255,255,255,.03);
      box-shadow: var(--shadow);
      overflow:hidden;
      display:flex;
      flex-direction:column;
    }
    .showcase-top{
      padding:18px 18px 10px;
      display:flex; align-items:center; justify-content:space-between; gap:10px;
    }
    .chips{display:flex; gap:8px; flex-wrap:wrap}
    .chip{
      font-size:12px; color:var(--muted);
      border:1px solid var(--border);
      background:rgba(255,255,255,.03);
      padding:7px 10px;
      border-radius:999px;
    }
    .grid-img{
      flex:1;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
      padding:0 18px 18px;
    }
    .ph{
      border-radius:16px;
      border:1px solid var(--border);
      background:
        radial-gradient(240px 120px at 30% 20%, rgba(124,92,255,.35), transparent 60%),
        radial-gradient(240px 120px at 70% 40%, rgba(46,231,167,.22), transparent 60%),
        rgba(255,255,255,.02);
      min-height:150px;
      position:relative;
      overflow:hidden;
    }
    .ph:before{
      content:"";
      position:absolute; inset:0;
      background: linear-gradient(120deg, rgba(255,255,255,.06), transparent 40%, rgba(255,255,255,.05));
      transform: translateX(-40%);
      animation: shimmer 3.2s ease-in-out infinite;
      opacity:.55;
    }
    @keyframes shimmer{
      0%,100%{transform:translateX(-60%)}
      50%{transform:translateX(30%)}
    }

    section{padding:26px 0}
    .section-head{
      display:flex; align-items:end; justify-content:space-between; gap:16px;
      margin-bottom:14px;
    }
    .section-head h2{margin:0; font-size:22px}
    .section-head p{margin:0; color:var(--muted); max-width:65ch}
    .cards{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:14px;
    }
    .card{
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      border-radius: 18px;
      padding:14px;
      box-shadow: 0 8px 22px rgba(0,0,0,.25);
      transition: transform .15s ease, border-color .15s ease, background .15s ease;
    }
    .card:hover{transform: translateY(-2px); border-color:rgba(255,255,255,.18); background: rgba(255,255,255,.05)}
    .card .thumb{border-radius:16px; height:130px; margin-bottom:12px; border:1px solid var(--border); background: rgba(255,255,255,.02)}
    .card h3{margin:0 0 6px; font-size:15px}
    .card p{margin:0; color:var(--muted); font-size:13px}
    .price{margin-top:10px; display:flex; align-items:center; justify-content:space-between; gap:10px}
    .price b{font-size:15px}
    .tag{
      font-size:11px; color:#0b0c10;
      background: linear-gradient(135deg, var(--brand2), #a6ffdd);
      padding:6px 9px; border-radius:999px; font-weight:800;
    }

    .two-col{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:14px;
    }
    .panel{
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius);
      padding:18px;
      box-shadow: var(--shadow);
    }
    .panel h3{margin:0 0 8px}
    .panel ul{margin:10px 0 0; padding-left:18px; color:var(--muted)}
    .form{
      display:grid; gap:10px;
    }
    input, textarea, select{
      width:100%;
      padding:12px 12px;
      border-radius:12px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.25);
      color: var(--text);
      outline:none;
    }
    textarea{min-height:110px; resize:vertical}
    input:focus, textarea:focus, select:focus{border-color: rgba(124,92,255,.7); box-shadow: 0 0 0 3px rgba(124,92,255,.18)}
    footer{
      padding:26px 0 34px;
      color:var(--muted);
      border-top:1px solid rgba(255,255,255,.06);
      margin-top:26px;
    }
    .footer-grid{
      display:flex; gap:16px; justify-content:space-between; flex-wrap:wrap;
    }
    .small{font-size:12px; color:var(--muted)}
    .notice{
      margin-top:10px;
      border:1px dashed rgba(255,255,255,.16);
      border-radius:14px;
      padding:10px 12px;
      background: rgba(255,255,255,.02);
    }

    /* Responsive */
    @media (max-width: 980px){
      .hero-grid{grid-template-columns:1fr}
      .cards{grid-template-columns: repeat(2, 1fr)}
      h1{font-size:36px}
    }
    @media (max-width: 720px){
      nav ul{display:none}
      .menu-btn{display:inline-flex}
      .cards{grid-template-columns: 1fr}
      .two-col{grid-template-columns: 1fr}
      h1{font-size:32px}
    }
  </style>
</head>
<body>

<header>
  <div class="container nav">
    <a class="brand" href="#inicio" aria-label="Ir al inicio">
      <span class="logo" aria-hidden="true"></span>
      <span>Tu Local</span>
    </a>

    <nav aria-label="Navegación principal">
      <ul id="menu">
        <li><a href="#categorias">Categorías</a></li>
        <li><a href="#destacados">Destacados</a></li>
        <li><a href="#nosotros">Nosotros</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>

    <div class="nav-actions">
      <a class="btn ghost" href="#contacto" title="WhatsApp / Contacto">📩 Consultar</a>
      <button class="btn menu-btn" id="toggleMenu" aria-label="Abrir/cerrar menú">☰</button>
    </div>
  </div>
</header>

<main id="inicio">
  <div class="container hero">
    <div class="hero-grid">
      <div class="hero-card">
        <span class="pill">✨ Nueva temporada · Envíos en Montevideo</span>
        <h1>Moda que se siente bien, se ve mejor.</h1>
        <p class="subtitle">
          Remeras, jeans, camperas y básicos para todos los días. Comprá por Instagram/WhatsApp o pasá por el local.
        </p>

        <div class="hero-actions">
          <a class="btn primary" href="#destacados">Ver destacados</a>
          <a class="btn" href="#categorias">Explorar categorías</a>
        </div>

        <div class="hero-stats">
          <div class="stat">
            <b>+120</b>
            <span>prendas seleccionadas</span>
          </div>
          <div class="stat">
            <b>24–48h</b>
            <span>entregas en zona urbana</span>
          </div>
          <div class="stat">
            <b>Cambios</b>
            <span>hasta 7 días</span>
          </div>
        </div>

        <div class="notice small">
          Tip: reemplazá “Tu Local” por tu marca y agregá tus links reales de Instagram/WhatsApp abajo.
        </div>
      </div>

      <aside class="showcase" aria-label="Vista previa de productos">
        <div class="showcase-top">
          <div>
            <div class="pill">🧥 Colección urbana</div>
          </div>
          <div class="chips" aria-label="Filtros">
            <span class="chip">Jeans</span>
            <span class="chip">Buzos</span>
            <span class="chip">Camperas</span>
          </div>
        </div>
        <div class="grid-img">
          <div class="ph" title="Foto producto 1 (placeholder)"></div>
          <div class="ph" title="Foto producto 2 (placeholder)"></div>
          <div class="ph" title="Foto producto 3 (placeholder)"></div>
          <div class="ph" title="Foto producto 4 (placeholder)"></div>
        </div>
      </aside>
    </div>
  </div>

  <section id="categorias">
    <div class="container">
      <div class="section-head">
        <div>
          <h2>Categorías</h2>
          <p>Elegí rápido lo que buscás. Después podés linkear cada categoría a tu catálogo o a Instagram.</p>
        </div>
      </div>

      <div class="cards">
        <a class="card" href="#contacto">
          <div class="thumb"></div>
          <h3>Jeans & Pantalones</h3>
          <p>Skinny, recto, cargo. Talles variados.</p>
        </a>
        <a class="card" href="#contacto">
          <div class="thumb"></div>
          <h3>Remeras & Tops</h3>
          <p>Básicos, estampadas y oversize.</p>
        </a>
        <a class="card" href="#contacto">
          <div class="thumb"></div>
          <h3>Buzos & Camperas</h3>
          <p>Frío resuelto con estilo.</p>
        </a>
        <a class="card" href="#contacto">
          <div class="thumb"></div>
          <h3>Accesorios</h3>
          <p>Gorras, cinturones, lentes y más.</p>
        </a>
      </div>
    </div>
  </section>

  <section id="destacados">
    <div class="container">
      <div class="section-head">
        <div>
          <h2>Destacados</h2>
          <p>Acá podés mostrar tus best-sellers. Los precios son ejemplo.</p>
        </div>
        <a class="btn" href="#contacto">Pedir por WhatsApp</a>
      </div>

      <div class="cards">
        <div class="card">
          <div class="thumb"></div>
          <h3>Jean recto premium</h3>
          <p>Denim resistente · Talles 36–46</p>
          <div class="price">
            <b>$ 2.490</b>
            <span class="tag">TOP</span>
          </div>
        </div>
        <div class="card">
          <div class="thumb"></div>
          <h3>Remera oversize</h3>
          <p>Algodón · Colores neutros</p>
          <div class="price">
            <b>$ 990</b>
            <span class="tag">NEW</span>
          </div>
        </div>
        <div class="card">
          <div class="thumb"></div>
          <h3>Buzo canguro</h3>
          <p>Interior frizado · Unisex</p>
          <div class="price">
            <b>$ 1.890</b>
            <span class="tag">🔥</span>
          </div>
        </div>
        <div class="card">
          <div class="thumb"></div>
          <h3>Campera urbana</h3>
          <p>Rompevientos · Liviana</p>
          <div class="price">
            <b>$ 3.490</b>
            <span class="tag">SALE</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="nosotros">
    <div class="container">
      <div class="two-col">
        <div class="panel">
          <h3>Sobre el local</h3>
          <p style="color:var(--muted); margin:0">
            Somos un local de ropa enfocado en moda urbana y básicos que combinan fácil.
            Seleccionamos prendas por calidad, calce y durabilidad.
          </p>
          <ul>
            <li>Atención personalizada</li>
            <li>Envíos y retiros coordinados</li>
            <li>Cambios dentro de 7 días</li>
          </ul>
        </div>

        <div class="panel">
          <h3>Horarios y ubicación</h3>
          <p class="small" style="margin:0 0 10px">
            Editá esta sección con tu dirección real.
          </p>
          <p style="margin:0; color:var(--muted)">
            📍 Dirección: <b style="color:var(--text)">Tu calle 1234, Montevideo</b><br/>
            🕒 Lunes a Sábado: <b style="color:var(--text)">10:00–19:00</b><br/>
            📦 Envíos: <b style="color:var(--text)">Montevideo y zona metropolitana</b>
          </p>
          <div class="notice small">
            Podés incrustar Google Maps acá (iframe) si querés.
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="contacto">
    <div class="container">
      <div class="section-head">
        <div>
          <h2>Contacto</h2>
          <p>Dejá tu consulta o linkeá directo a WhatsApp/Instagram.</p>
        </div>
      </div>

      <div class="two-col">
        <div class="panel">
          <h3>Escribinos</h3>
          <form class="form" onsubmit="return sendMessage(event)">
            <input id="name" type="text" placeholder="Tu nombre" required />
            <select id="topic" required>
              <option value="" selected disabled>Motivo</option>
              <option>Consulta de talles</option>
              <option>Disponibilidad</option>
              <option>Envíos</option>
              <option>Cambios</option>
            </select>
            <textarea id="msg" placeholder="Tu mensaje..." required></textarea>
            <button class="btn primary" type="submit">Enviar (simulado)</button>
            <p class="small" style="margin:0">*Este demo no envía a un servidor: abre tu app de email o WhatsApp si lo configurás.</p>
          </form>
        </div>

        <div class="panel">
          <h3>Links rápidos</h3>
          <p class="small" style="margin-top:0">Reemplazá los links por los tuyos.</p>

          <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px">
            <a class="btn" href="https://instagram.com/" target="_blank" rel="noreferrer">📷 Instagram</a>
            <a class="btn" href="https://wa.me/59800000000" target="_blank" rel="noreferrer">💬 WhatsApp</a>
            <a class="btn" href="mailto:tuemail@dominio.com">✉️ Email</a>
          </div>

          <div class="notice">
            <div class="small"><b>Tip pro:</b> si querés ventas online posta, se puede conectar esto a:</div>
            <ul class="small" style="margin:8px 0 0; padding-left:18px">
              <li>Un catálogo (Google Sheets / Airtable)</li>
              <li>Mercado Pago / transferencia</li>
              <li>Shopify / Tiendanube / WooCommerce</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container footer-grid">
    <div>
      <div class="brand" style="margin-bottom:8px">
        <span class="logo" aria-hidden="true"></span>
        <span>Tu Local</span>
      </div>
      <div class="small">© <span id="year"></span> · Moda urbana · Montevideo</div>
    </div>
    <div class="small">
      Hecho con HTML + CSS (un solo archivo).<br/>
      Listo para subir a hosting.
    </div>
  </div>
</footer>

<script>
  // Año automático
  document.getElementById('year').textContent = new Date().getFullYear();

  // Menú móvil
  const toggle = document.getElementById('toggleMenu');
  const menu = document.getElementById('menu');
  toggle?.addEventListener('click', () => {
    const isOpen = menu.style.display === 'flex';
    menu.style.display = isOpen ? 'none' : 'flex';
    menu.style.flexDirection = 'column';
    menu.style.position = 'absolute';
    menu.style.right = '16px';
    menu.style.top = '60px';
    menu.style.padding = '12px';
    menu.style.background = 'rgba(11,12,16,.95)';
    menu.style.border = '1px solid rgba(255,255,255,.10)';
    menu.style.borderRadius = '14px';
    menu.style.gap = '10px';
  });

  // Envío "simulado" del formulario (podés cambiarlo a WhatsApp o Email real)
  function sendMessage(e){
    e.preventDefault();
    const name = document.getElementById('name').value.trim();
    const topic = document.getElementById('topic').value;
    const msg = document.getElementById('msg').value.trim();

    alert(`Gracias, ${name}.\n\nMotivo: ${topic}\nMensaje: ${msg}\n\n(Esto es un demo. Si querés, lo conectamos a WhatsApp o a un backend.)`);
    e.target.reset();
    return false;
  }
</script>

</body>
</html>