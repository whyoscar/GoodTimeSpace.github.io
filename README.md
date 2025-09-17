# GoodTimeSpace.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Casa Wabi — Mushroom Pavilion (recreation)</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="logo" href="#">OMA — Projects</a>
      <nav class="nav">
        <a href="#">Projects</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section class="hero">
    <img src="assets/hero.jpg" alt="Mushroom Pavilion hero" class="hero-image" />
    <div class="hero-overlay">
      <div class="container">
        <h1 class="project-title">Casa Wabi — Mushroom Pavilion</h1>
        <p class="meta">OMA • Puerto Escondido • 2025</p>
      </div>
    </div>
  </section>

  <!-- Main content -->
  <main class="container main">
    <article class="project">
      <div class="project-body">
        <p>
          The Mushroom Pavilion is a self-supporting ellipsoid pavilion conceived as an incubator for fungi
          and a place for community exchange. Its stepped interior creates shelfing for terra-cotta pots and
          frames a central gathering space beneath an oculus.
        </p>

        <h2>Concept & program</h2>
        <p>
          The pavilion arranges fruiting, incubation and storage around a central amphitheatre-like space,
          providing both visibility of the cultivation process and an intimate place for communal activity.
        </p>

        <dl class="project-credits">
          <div>
            <dt>Architect</dt><dd>OMA</dd>
          </div>
          <div>
            <dt>Location</dt><dd>Puerto Escondido, Mexico</dd>
          </div>
          <div>
            <dt>Year</dt><dd>2025</dd>
          </div>
        </dl>
      </div>

      <!-- Gallery -->
      <section class="gallery" aria-label="Project images">
        <button class="gallery-filter" id="open-all">Open first image</button>
        <div class="grid">
          <figure tabindex="0">
            <img src="assets/img1.jpg" alt="Exterior view" data-index="0" />
          </figure>
          <figure tabindex="0">
            <img src="assets/img2.jpg" alt="Interior stepped seating" data-index="1" />
          </figure>
          <figure tabindex="0">
            <img src="assets/img3.jpg" alt="Model" data-index="2" />
          </figure>
          <figure tabindex="0">
            <img src="assets/img4.jpg" alt="Detail" data-index="3" />
          </figure>
        </div>
      </section>
    </article>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>© 2025 — Recreated layout for demonstration</p>
    </div>
  </footer>

  <!-- Lightbox UI -->
  <div id="lightbox" class="lightbox" aria-hidden="true" role="dialog" aria-label="Image viewer">
    <button id="lb-close" class="lb-close" aria-label="Close">×</button>
    <button id="lb-prev" class="lb-nav" aria-label="Previous image">‹</button>
    <div class="lb-content">
      <img id="lb-image" src="" alt="" />
      <p id="lb-caption" class="lb-caption"></p>
    </div>
    <button id="lb-next" class="lb-nav" aria-label="Next image">›</button>
  </div>

  <script src="script.js"></script>
</body>
</html>

/* Simple reset */
* { box-sizing: border-box; }
html,body { height:100%; margin:0; font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; color:#111; background:#fff; }
.container { max-width:1100px; margin:0 auto; padding:0 20px; }

/* Header */
.site-header { position:sticky; top:0; background:rgba(255,255,255,0.85); backdrop-filter: blur(6px); border-bottom:1px solid rgba(0,0,0,0.04); z-index:20; }
.header-inner { display:flex; align-items:center; justify-content:space-between; padding:14px 0; }
.logo { font-weight:700; text-decoration:none; color:#111; }
.nav a { margin-left:18px; text-decoration:none; color:#333; font-size:0.95rem; }

/* Hero */
.hero { position:relative; height:60vh; min-height:420px; display:block; overflow:hidden; }
.hero-image { width:100%; height:100%; object-fit:cover; display:block; filter:contrast(0.95) saturate(0.9); transform:scale(1.03); }
.hero-overlay { position:absolute; left:0; right:0; top:0; bottom:0; display:flex; align-items:flex-end; }
.hero-overlay .container { padding-bottom:36px; color:#fff; text-shadow:0 6px 20px rgba(0,0,0,0.35); }
.project-title { font-size:clamp(1.6rem, 3.6vw, 3.2rem); margin:0 0 6px; letter-spacing: -0.02em; }
.meta { margin:0; opacity:0.95; }

/* Main */
.main { padding:48px 0; }
.project-body p { line-height:1.6; margin:0 0 1rem; color:#222; font-size:1rem; }
.project-body h2 { margin-top:1.2rem; font-size:1.15rem; }
.project-credits { display:grid; grid-template-columns:repeat(auto-fit,minmax(140px,1fr)); gap:12px; margin-top:18px; }
.project-credits dt { font-weight:600; font-size:0.85rem; color:#555; }
.project-credits dd { margin:2px 0 12px; color:#111; }

/* Gallery */
.gallery { margin-top:28px; }
.gallery .grid { display:grid; grid-template-columns: repeat(3, 1fr); gap:12px; }
.gallery figure { margin:0; overflow:hidden; background:#f3f3f3; cursor:pointer; border-radius:6px; }
.gallery img { width:100%; height:230px; object-fit:cover; display:block; transition:transform .35s ease; }
.gallery figure:focus img,
.gallery figure:hover img { transform:scale(1.04); }

/* Buttons */
button { font:inherit; }
.gallery-filter { margin-bottom:12px; padding:8px 12px; border:1px solid #ddd; background:#fff; border-radius:6px; }

/* Lightbox */
.lightbox { position:fixed; inset:0; display:flex; align-items:center; justify-content:center; background:rgba(0,0,0,0.85); opacity:0; pointer-events:none; transition:opacity .25s ease; z-index:60; }
.lightbox[aria-hidden="false"] { opacity:1; pointer-events:auto; }
.lb-content { max-width:92vw; max-height:84vh; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:8px; }
.lb-content img { max-width:100%; max-height:78vh; border-radius:6px; box-shadow:0 20px 60px rgba(0,0,0,0.6); }
.lb-close { position: absolute; right:22px; top:18px; background:transparent; border:0; color:#fff; font-size:28px; cursor:pointer; }
.lb-nav { position:absolute; top:50%; transform:translateY(-50%); background:transparent; border:0; color:#fff; font-size:36px; padding:12px; cursor:pointer; }
#lb-prev { left:10px; }
#lb-next { right:10px; }
.lb-caption { color:#ddd; font-size:0.95rem; margin:0; text-align:center; max-width:80vw; }

/* Footer */
.site-footer { border-top:1px solid #eee; padding:18px 0; text-align:center; color:#666; font-size:0.9rem; }

/* Responsive */
@media (max-width:920px){
  .gallery .grid { grid-template-columns: repeat(2, 1fr); }
  .hero { height:48vh; min-height:320px; }
}
@media (max-width:560px){
  .nav { display:none; }
  .gallery .grid { grid-template-columns: 1fr; }
  .hero { height:42vh; min-height:240px; }
  .gallery img { height:200px; }
}

// Simple lightbox for the gallery
(() => {
  const images = Array.from(document.querySelectorAll('.gallery img'));
  const lightbox = document.getElementById('lightbox');
  const lbImage = document.getElementById('lb-image');
  const lbCaption = document.getElementById('lb-caption');
  const lbClose = document.getElementById('lb-close');
  const lbNext = document.getElementById('lb-next');
  const lbPrev = document.getElementById('lb-prev');
  const openAllBtn = document.getElementById('open-all');

  let current = 0;

  function open(index) {
    const el = images[index];
    if (!el) return;
    current = index;
    lbImage.src = el.src;
    lbImage.alt = el.alt || '';
    lbCaption.textContent = el.alt || '';
    lightbox.setAttribute('aria-hidden', 'false');
    document.body.style.overflow = 'hidden';
    // focus for keyboard users
    lbClose.focus();
  }

  function close() {
    lightbox.setAttribute('aria-hidden', 'true');
    document.body.style.overflow = '';
  }

  function next() { open((current + 1) % images.length); }
  function prev() { open((current - 1 + images.length) % images.length); }

  images.forEach((img, i) => {
    img.addEventListener('click', () => open(i));
    // keyboard accessible: Enter/Space on figure container
    img.parentElement.addEventListener('keydown', (e) => {
      if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); open(i); }
    });
  });

  lbClose.addEventListener('click', close);
  lbNext.addEventListener('click', next);
  lbPrev.addEventListener('click', prev);

  // keyboard controls
  document.addEventListener('keydown', (e) => {
    if (lightbox.getAttribute('aria-hidden') === 'false') {
      if (e.key === 'Escape') close();
      if (e.key === 'ArrowRight') next();
      if (e.key === 'ArrowLeft') prev();
    }
  });

  openAllBtn.addEventListener('click', () => open(0));
})();
