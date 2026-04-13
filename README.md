<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Maison Café</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Segoe UI', Arial, sans-serif; background: #fff; color: #1a1a1a; }

    /* NAV */
    nav { display: flex; justify-content: space-between; align-items: center; padding: 1.2rem 2.5rem; border-bottom: 1px solid #eee; }
    .nav-logo { font-size: 20px; font-weight: 600; letter-spacing: 3px; }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a { text-decoration: none; font-size: 13px; color: #555; letter-spacing: 0.5px; }
    .nav-links a:hover { color: #1a1a1a; }

    /* HERO */
    .hero { padding: 6rem 2.5rem 5rem; text-align: center; border-bottom: 1px solid #eee; }
    .hero-tag { font-size: 11px; letter-spacing: 4px; color: #999; margin-bottom: 1rem; }
    .hero h1 { font-size: 48px; font-weight: 500; line-height: 1.2; margin-bottom: 1.2rem; }
    .hero p { font-size: 15px; color: #666; max-width: 420px; margin: 0 auto 2.5rem; line-height: 1.8; }
    .hero-btns { display: flex; gap: 12px; justify-content: center; }
    .btn-primary { padding: 12px 32px; background: #1a1a1a; color: #fff; border: none; border-radius: 8px; font-size: 13px; cursor: pointer; letter-spacing: 0.5px; }
    .btn-primary:hover { background: #333; }
    .btn-outline { padding: 12px 32px; background: transparent; color: #1a1a1a; border: 1px solid #ccc; border-radius: 8px; font-size: 13px; cursor: pointer; letter-spacing: 0.5px; }
    .btn-outline:hover { background: #f5f5f5; }

    /* SECTIONS */
    .section { padding: 4rem 2.5rem; border-bottom: 1px solid #eee; }
    .section-label { font-size: 11px; letter-spacing: 3px; color: #aaa; margin-bottom: 2rem; }

    /* MENU GRID */
    .menu-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); border: 1px solid #eee; border-radius: 12px; overflow: hidden; gap: 1px; background: #eee; }
    .menu-item { padding: 1.5rem; background: #fff; }
    .menu-item-name { font-size: 15px; font-weight: 500; margin-bottom: 5px; }
    .menu-item-desc { font-size: 12px; color: #888; line-height: 1.6; margin-bottom: 10px; }
    .menu-item-price { font-size: 14px; font-weight: 600; }

    /* ABOUT */
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
    .about-text h2 { font-size: 28px; font-weight: 500; line-height: 1.35; margin-bottom: 1rem; }
    .about-text p { font-size: 14px; color: #666; line-height: 1.9; }
    .about-img { height: 260px; background: #f5f5f5; border-radius: 12px; display: flex; align-items: center; justify-content: center; color: #bbb; font-size: 12px; letter-spacing: 2px; border: 1px solid #eee; }

    /* HOURS */
    .hours-table { width: 100%; max-width: 400px; border-collapse: collapse; }
    .hours-table tr { border-bottom: 1px solid #eee; }
    .hours-table td { padding: 10px 0; font-size: 14px; }
    .hours-table td:first-child { color: #888; }
    .hours-table td:last-child { text-align: right; font-weight: 500; }

    /* RESERVATIONS */
    .form-row { display: flex; gap: 12px; flex-wrap: wrap; }
    .form-row input { flex: 1; min-width: 140px; padding: 10px 14px; font-size: 13px; border: 1px solid #ddd; border-radius: 8px; outline: none; color: #1a1a1a; background: #fff; }
    .form-row input:focus { border-color: #999; }

    /* FOOTER */
    footer { padding: 1.5rem 2.5rem; display: flex; justify-content: space-between; align-items: center; }
    .footer-copy { font-size: 12px; color: #aaa; }
    .footer-links { display: flex; gap: 1.5rem; }
    .footer-links a { font-size: 12px; color: #aaa; text-decoration: none; }
    .footer-links a:hover { color: #555; }

    /* CONTACT INFO */
    .contact-block { margin-top: 2rem; }
    .contact-label { font-size: 11px; letter-spacing: 2px; color: #aaa; margin-bottom: 6px; }
    .contact-val { font-size: 14px; color: #1a1a1a; line-height: 1.8; }

    @media (max-width: 600px) {
      .about-grid { grid-template-columns: 1fr; gap: 2rem; }
      .nav-links { display: none; }
      .hero h1 { font-size: 32px; }
    }
  </style>
</head>
<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="nav-logo">MAISON</div>
    <ul class="nav-links">
      <li><a href="#menu">Menu</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#hours">Hours</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <p class="hero-tag">EST. 2018 &middot; CAFÉ & BISTRO</p>
    <h1>Simple food,<br>thoughtfully made.</h1>
    <p>A neighbourhood café serving seasonal dishes, specialty coffee, and fresh pastries every morning.</p>
    <div class="hero-btns">
      <button class="btn-primary" onclick="document.getElementById('reserve').scrollIntoView({behavior:'smooth'})">Reserve a table</button>
      <button class="btn-outline" onclick="document.getElementById('menu').scrollIntoView({behavior:'smooth'})">View menu</button>
    </div>
  </section>

  <!-- MENU -->
  <section class="section" id="menu">
    <p class="section-label">MENU HIGHLIGHTS</p>
    <div class="menu-grid">
      <div class="menu-item">
        <div class="menu-item-name">Avocado Toast</div>
        <div class="menu-item-desc">Sourdough, smashed avo, poached egg, chilli flakes</div>
        <div class="menu-item-price">₹320</div>
      </div>
      <div class="menu-item">
        <div class="menu-item-name">Shakshuka</div>
        <div class="menu-item-desc">Spiced tomato, baked eggs, feta, toasted bread</div>
        <div class="menu-item-price">₹290</div>
      </div>
      <div class="menu-item">
        <div class="menu-item-name">Cold Brew Latte</div>
        <div class="menu-item-desc">18-hour cold brew, oat milk, vanilla</div>
        <div class="menu-item-price">₹180</div>
      </div>
      <div class="menu-item">
        <div class="menu-item-name">Almond Croissant</div>
        <div class="menu-item-desc">Buttery laminated dough, frangipane, toasted almonds</div>
        <div class="menu-item-price">₹140</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="section" id="about">
    <div class="about-grid">
      <div class="about-text">
        <h2>A quiet corner for<br>good food & coffee.</h2>
        <p>Maison started as a passion project by two friends who believed that great food doesn't need to be complicated. We source locally, cook simply, and serve with warmth. Whether you're grabbing a quick coffee or settling in for brunch, you're always welcome here.</p>
      </div>
      <div class="about-img">CAFÉ PHOTO</div>
    </div>
  </section>

  <!-- HOURS & LOCATION -->
  <section class="section" id="hours">
    <p class="section-label">HOURS & LOCATION</p>
    <div style="display: flex; gap: 4rem; flex-wrap: wrap;">
      <div>
        <table class="hours-table">
          <tr><td>Monday – Friday</td><td>8:00 am – 7:00 pm</td></tr>
          <tr><td>Saturday</td><td>9:00 am – 6:00 pm</td></tr>
          <tr><td>Sunday</td><td>10:00 am – 4:00 pm</td></tr>
        </table>
      </div>
      <div id="contact">
        <div class="contact-label">ADDRESS</div>
        <div class="contact-val">12, FC Road, Shivajinagar<br>Pune, Maharashtra 411005</div>
        <div class="contact-block">
          <div class="contact-label">PHONE</div>
          <div class="contact-val">+91 98765 43210</div>
        </div>
        <div class="contact-block">
          <div class="contact-label">EMAIL</div>
          <div class="contact-val">hello@maisoncafe.in</div>
        </div>
      </div>
    </div>
  </section>

  <!-- RESERVATIONS -->
  <section class="section" id="reserve">
    <p class="section-label">RESERVATIONS</p>
    <p style="font-size: 14px; color: #666; margin-bottom: 1.5rem; line-height: 1.7;">Walk-ins welcome. For groups of 4 or more, we recommend booking ahead.</p>
    <div class="form-row">
      <input type="text" placeholder="Your name" />
      <input type="text" placeholder="Date (DD/MM/YYYY)" />
      <input type="text" placeholder="Time (e.g. 7:00 pm)" />
      <input type="number" placeholder="Guests" style="max-width: 100px;" />
      <button class="btn-primary">Book now</button>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-copy">©️ 2026 Maison Café. All rights reserved.</div>
    <div class="footer-links">
      <a href="#">Instagram</a>
      <a href="#">Facebook</a>
      <a href="#">Google Maps</a>
    </div>
  </footer>

</body>
</html>
