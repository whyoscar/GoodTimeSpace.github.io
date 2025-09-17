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
