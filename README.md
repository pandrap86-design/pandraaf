<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Website Sederhana — Landra</title>
  <meta name="description" content="Contoh single-page website: hero, fitur, portofolio, dan kontak." />
  <style>
    :root{
      --bg:#0f1724; /* dark navy */
      --card:#0b1220;
      --accent:#06b6d4; /* cyan */
      --muted:#94a3b8;
      --glass: rgba(255,255,255,0.04);
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background:linear-gradient(180deg,var(--bg),#071022 60%);
      color:#e6eef6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    .container{max-width:980px;margin:0 auto;padding:32px}

    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px}
    nav a:hover{color:var(--accent)}

    .hero{display:grid;grid-template-columns:1fr 360px;gap:28px;align-items:center;margin-bottom:36px}
    .hero-card{background:linear-gradient(180deg,rgba(255,255,255,0.02),var(--glass));padding:28px;border-radius:14px;box-shadow:0 6px 18px rgba(2,6,23,0.6)}
    h1{font-size:clamp(26px,4vw,40px);margin:0 0 12px}
    p.lead{color:var(--muted);margin:0 0 18px}
    .cta{display:inline-block;padding:10px 16px;border-radius:10px;background:var(--accent);color:#032027;text-decoration:none;font-weight:600}

    .features{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px;margin-bottom:36px}
    .feature{background:var(--card);padding:18px;border-radius:12px}
    .feature h3{margin:0 0 8px}
    .muted{color:var(--muted)}

    .portfolio{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
    .project{background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);padding:12px;border-radius:10px}

    footer{margin-top:40px;color:var(--muted);font-size:13px;text-align:center}

    /* contact form */
    form{display:grid;gap:10px}
    input,textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);background:transparent;color:inherit}
    button[type=submit]{padding:10px 12px;border-radius:8px;border:0;background:var(--accent);font-weight:700}

    /* responsive */
    @media (max-width:860px){
      .hero{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">L</div>
        <div>
          <div style="font-weight:700">Landra</div>
          <div style="font-size:12px;color:var(--muted)">Contoh website sederhana</div>
        </div>
      </div>
      <nav>
        <a href="#features">Fitur</a>
        <a href="#portfolio">Portofolio</a>
        <a href="#contact">Kontak</a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-card">
        <h1>Halo! Saya bantu buatkan website HTML sederhana.</h1>
        <p class="lead">Template ini sudah termasuk: responsive layout, kartu fitur, portofolio, dan formulir kontak (tidak ada backend). Mudah dikustomisasi.</p>
        <a class="cta" id="downloadBtn">Download HTML</a>
        <div style="margin-top:16px;color:var(--muted);font-size:13px">Atau: salin, sunting, dan unggah ke hosting statis seperti Netlify, Vercel, GitHub Pages.</div>
      </div>

      <aside>
        <div class="hero-card">
          <h3>Status</h3>
          <p class="muted">Template siap dipakai. Klik tombol untuk mengunduh file HTML yang sama dengan halaman ini.</p>
          <hr style="border:none;border-top:1px solid rgba(255,255,255,0.04);margin:12px 0">
          <strong>Demo interaksi</strong>
          <ul style="margin:8px 0 0 18px;color:var(--muted)">
            <li>Notifikasi saat kirim pesan</li>
            <li>Unduh HTML sebagai file</li>
          </ul>
        </div>
      </aside>
    </section>

    <section id="features" class="features">
      <div class="feature">
        <h3>Responsive</h3>
        <p class="muted">Tampilan menyesuaikan layar mobile, tablet, dan desktop.</p>
      </div>
      <div class="feature">
        <h3>Mudah disunting</h3>
        <p class="muted">Semua CSS dan JS ada dalam satu file untuk kemudahan.</p>
      </div>
      <div class="feature">
        <h3>Form Kontak (Front-end)</h3>
        <p class="muted">Form mengirim data ke konsol dan menampilkan notifikasi. Hubungkan ke backend sesuai kebutuhan.</p>
      </div>
    </section>

    <section id="portfolio" class="portfolio">
      <div class="project">
        <strong>Project A</strong>
        <div class="muted">Deskripsi singkat project A.</div>
      </div>
      <div class="project">
        <strong>Project B</strong>
        <div class="muted">Deskripsi singkat project B.</div>
      </div>
      <div class="project">
        <strong>Project C</strong>
        <div class="muted">Deskripsi singkat project C.</div>
      </div>
    </section>

    <section id="contact" style="margin-top:28px">
      <div class="hero-card">
        <h3>Kontak</h3>
        <form id="contactForm">
          <input type="text" name="name" placeholder="Nama" required />
          <input type="email" name="email" placeholder="Email" required />
          <textarea name="message" rows="4" placeholder="Pesan" required></textarea>
          <button type="submit">Kirim</button>
        </form>
        <div id="notice" style="margin-top:10px;color:var(--muted)"></div>
      </div>
    </section>

    <footer>
      © <span id="year"></span> Landra • Dibuat dengan ChatGPT
    </footer>
  </div>

  <script>
    // Small JS: download page as .html, handle contact form
    document.getElementById('year').textContent = new Date().getFullYear();

    // Download the full HTML source of this page
    document.getElementById('downloadBtn').addEventListener('click', function(){
      // Build a complete HTML string by serializing the document
      const doctype = '<!doctype html>\n';
      const html = document.documentElement.outerHTML;
      const blob = new Blob([doctype + html], {type: 'text/html'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download = 'website.html';
      document.body.appendChild(a); a.click(); a.remove();
      URL.revokeObjectURL(url);
    });

    // Contact form (front-end demo only)
    const form = document.getElementById('contactForm');
    const notice = document.getElementById('notice');
    form.addEventListener('submit', function(e){
      e.preventDefault();
      const data = new FormData(form);
      const obj = Object.fromEntries(data.entries());
      console.log('Contact form submitted:', obj);
      notice.textContent = 'Terima kasih! Pesan Anda telah dicatat (demo).';
      form.reset();
      // Example: show temporary green background to indicate success
      const original = form.style.boxShadow;
      form.style.boxShadow = '0 4px 20px rgba(6,182,212,0.12)';
      setTimeout(()=> form.style.boxShadow = original, 1400);
    });

    // Small accessibility: focus styles for keyboard users
    document.addEventListener('keydown', function(e){
      if(e.key === 'Tab') document.body.classList.add('user-is-tabbing');
    });
  </script>
</body>
</html>
