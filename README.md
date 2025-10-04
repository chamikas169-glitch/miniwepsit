<!DOCTYPE html>
<html lang="si">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mini Website — උදාහරණය</title>
  <style>
    /* ====== Reset / Base ====== */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html,body { height: 100%; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; color:#f5f5f5; background: #0b0d12; }

    /* ====== Page layout ====== */
    header {
      background: linear-gradient(90deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
      backdrop-filter: blur(6px);
      padding: 18px 24px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      position:sticky;
      top:0;
      z-index:10;
      border-bottom: 1px solid rgba(255,255,255,0.03);
    }
    .brand { font-weight:700; letter-spacing:1px; color:#fff; }
    nav a { color:rgba(255,255,255,0.85); text-decoration:none; margin-left:18px; font-weight:600; font-size:14px; }
    nav a:hover { color:#a8ffea; }

    main { padding:32px; max-width:1200px; margin: 30px auto; }

    /* ====== Hero ====== */
    .hero {
      display:grid;
      grid-template-columns: 1fr 480px;
      gap:28px;
      align-items:center;
      margin-bottom:36px;
    }
    .hero .intro {
      padding:22px;
    }
    .intro h1 { font-size:2.2rem; margin-bottom:10px; color:#fff; }
    .intro p { color:rgba(255,255,255,0.8); line-height:1.6; }
    .cta {
      margin-top:18px;
      display:flex;
      gap:12px;
    }
    .btn {
      background:linear-gradient(90deg,#ff416c,#ff753b);
      padding:10px 16px;
      border-radius:10px;
      color:#fff;
      text-decoration:none;
      font-weight:700;
      box-shadow: 0 8px 24px rgba(255,99,97,0.12);
    }

    /* ====== Car card (neon style) ====== */
    .card {
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      padding:12px;
      border-radius:14px;
      position:relative;
      overflow:hidden;
      border: 1px solid rgba(255,255,255,0.04);
    }
    .car-photo {
      width:100%;
      height:320px;
      border-radius:10px;
      background:
        radial-gradient(600px 120px at 20% 20%, rgba(168,255,234,0.06), transparent 10%),
        linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.00));
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
    }
    .car-photo img {
      max-width:100%;
      max-height:100%;
      object-fit:cover;
      border-radius:8px;
      transform: translateY(6px);
      box-shadow: 0 18px 50px rgba(0,0,0,0.6);
    }
    /* neon underglow simulated */
    .neon-glow {
      position:absolute;
      left:50%;
      transform:translateX(-50%);
      bottom:18px;
      width:85%;
      height:24px;
      filter: blur(22px);
      opacity:0.95;
      pointer-events:none;
      border-radius:20px;
      background: linear-gradient(90deg,#00fff0,#0066ff,#ff00aa);
      mix-blend-mode:screen;
    }

    /* ====== Contact form ====== */
    .contact {
      margin-top:28px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:18px;
    }
    .contact form {
      grid-column: 1 / -1;
      background: rgba(255,255,255,0.02);
      padding:16px;
      border-radius:10px;
      border:1px solid rgba(255,255,255,0.03);
    }
    label { display:block; font-size:13px; margin-bottom:6px; color:rgba(255,255,255,0.9); }
    input, textarea {
      width:100%;
      padding:10px 12px;
      border-radius:8px;
      border:1px solid rgba(255,255,255,0.06);
      background: rgba(0,0,0,0.4);
      color:#fff;
      margin-bottom:12px;
      font-size:14px;
      resize:vertical;
    }
    .submit-btn {
      background:#00d3c8; color:#021212; padding:10px 14px; border-radius:8px; border:none; font-weight:700; cursor:pointer;
    }

    /* ====== Footer ====== */
    footer { margin-top:40px; text-align:center; color:rgba(255,255,255,0.6); font-size:14px; padding:20px 0; }

    /* ====== Responsive ====== */
    @media (max-width: 920px) {
      .hero { grid-template-columns: 1fr; }
      .car-photo { height:260px; }
      .contact { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <header>
    <div class="brand">MyMiniSite</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#car">Car</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main id="home">
    <section class="hero">
      <div class="intro">
        <h1>Hyper-real cinematic shot — demo</h1>
        <p>මෙය කුඩා දෘශ්‍යමය වෙබ් පිටුවකි. පහළින් ඔබට පිංතූරය, neon underglow ආශ්‍රිත style එක සහ contact form එකක් තියෙනවා. ඔබට කේතය හැඩගස්වා ගැනීමට හෝ වෙනස් කිරීමට නිදහස්.</p>

        <div class="cta">
          <a class="btn" href="#car">දැන් බලන්න</a>
          <a class="btn" href="#contact" style="background:linear-gradient(90deg,#6a85ff,#63ffe5)">හරහා සම්බන්ධ වන්න</a>
        </div>
      </div>

      <div class="card" id="car">
        <div class="car-photo">
          <!-- Placeholder: user can replace src with real generated image -->
          <img id="carImage" src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="Car demo image" />
          <div class="neon-glow" id="neonGlow"></div>
        </div>

        <div style="margin-top:12px; display:flex; justify-content:space-between; align-items:center;">
          <div>
            <strong>Modified Honda Civic Type R</strong>
            <div style="color:rgba(255,255,255,0.7); font-size:13px;">Night street, neon underglow — cinematic angle</div>
          </div>
          <div style="font-size:12px; color:rgba(255,255,255,0.6);">EOS R5 · 85mm · f/1.4</div>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <form id="contactForm">
        <label for="name">නම</label>
        <input id="name" type="text" placeholder="ඔබේ නම" required>

        <label for="email">ඊ-තැපැල්</label>
        <input id="email" type="email" placeholder="you@example.com" required>

        <label for="message">පනිවිඩය</label>
        <textarea id="message" placeholder="ඔබේ පනිවිඩය මෙහි ලිවිය හැක..." rows="6" required></textarea>

        <button type="submit" class="submit-btn">දැන් යවන්න</button>
      </form>
    </section>

    <footer>
      © 2025 MyMiniSite — සාදන ලද්දේ demo එකකි
    </footer>
  </main>

  <script>
    // ====== JavaScript: small interactions ======
    // 1) Contact form basic handling (no server) - show a friendly message
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      if (!name || !email || !message) {
        alert('කරුණාකර සියලු ක්ෂේත්‍ර පුරවා ඉදිරිපත් කරන්න.');
        return;
      }
      // Simple fake-submit feedback
      alert(`${name} — ඔබේ පණිවිඩය ලැබී තිබේ! (කාලීන demo)`);
      form.reset();
    });

    // 2) Neon glow color animation (purely UI)
    const neon = document.getElementById('neonGlow');
    let t = 0;
    function animateNeon() {
      t += 0.02;
      // create smooth hue shifting
      const r = Math.floor(128 + 127 * Math.sin(t));
      const g = Math.floor(128 + 127 * Math.sin(t + 2));
      const b = Math.floor(128 + 127 * Math.sin(t + 4));
      neon.style.background = `linear-gradient(90deg, rgba(${r},${g},${b},0.95), rgba(${255 - r},${255 - g},${255 - b},0.95))`;
      requestAnimationFrame(animateNeon);
    }
    animateNeon();

    // 3) Replace placeholder image with local generated image if user drags/drops one
    const carImg = document.getElementById('carImage');
    const card = document.querySelector('.car-photo');
    card.addEventListener('dragover', (e) => {
      e.preventDefault();
      card.style.outline = '2px dashed rgba(255,255,255,0.08)';
    });
    card.addEventListener('dragleave', () => {
      card.style.outline = 'none';
    });
    card.addEventListener('drop', (e) => {
      e.preventDefault();
      card.style.outline = 'none';
      const file = e.dataTransfer.files && e.dataTransfer.files[0];
      if (!file) return;
      if (!file.type.startsWith('image/')) {
        alert('කරුණාකර පින්තූරයක් බාගත කරන්න.');
        return;
      }
      const url = URL.createObjectURL(file);
      carImg.src = url;
    });

    // 4) Smooth scroll for anchors
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', (e)=>{
        e.preventDefault();
        const id = a.getAttribute('href').slice(1);
        const el = document.getElementById(id);
        if (el) el.scrollIntoView({behavior:'smooth', block:'start'});
      });
    });
  </script>
</body>
</html>
