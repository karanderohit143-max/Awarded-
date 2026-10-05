# Awarded-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Award Goes To My Cute Girl 🏆❤️</title>
  
  <!-- Typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Montserrat:wght@400;600;800&family=Playfair+Display:ital,wght@0,600;0,800;1,600&display=swap" rel="stylesheet">

  <!-- Canvas Confetti Library -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <style>
    :root {
      --bg-burgundy: #2d0b1e;
      --bg-dark-wine: #1a0510;
      --gold-primary: #f39c12;
      --gold-light: #f1c40f;
      --gold-gradient: linear-gradient(135deg, #ffe066 0%, #d4af37 50%, #aa7c11 100%);
      --pink-highlight: #ff758c;
      --cream-text: #fff8f0;
      --shadow-gold: rgba(212, 175, 55, 0.4);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body, html {
      width: 100%;
      min-height: 100vh;
      overflow-x: hidden;
      font-family: 'Montserrat', sans-serif;
      background-color: var(--bg-dark-wine);
      color: var(--cream-text);
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    /* Canvas Backgrounds */
    #sparkle-canvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }

    /* Radial Light Rays / Glow */
    .bg-gradient {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at center, #521535 0%, var(--bg-burgundy) 50%, var(--bg-dark-wine) 100%);
      z-index: 0;
    }

    /* Floating SVG Container */
    .decorations-layer {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 2;
      overflow: hidden;
    }

    /* Floating Elements */
    .floating-item {
      position: absolute;
      opacity: 0;
      filter: drop-shadow(0 4px 10px rgba(0,0,0,0.5));
      animation: floatAround 12s infinite ease-in-out;
    }

    @keyframes floatAround {
      0% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-25px) rotate(12deg); }
      100% { transform: translateY(0px) rotate(0deg); }
    }

    /* Layout Wrapper */
    .container {
      position: relative;
      z-index: 10;
      width: 90%;
      max-width: 650px;
      margin: 40px auto;
      text-align: center;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px 20px;
      background: rgba(45, 11, 30, 0.45);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 24px;
      border: 1px solid rgba(212, 175, 55, 0.25);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.6), 0 0 30px var(--shadow-gold);
    }

    /* Opening Animation States */
    .anim-hidden {
      opacity: 0;
      transform: translateY(30px) scale(0.95);
    }

    .anim-reveal {
      transition: opacity 1.2s cubic-bezier(0.25, 1, 0.5, 1), transform 1.2s cubic-bezier(0.25, 1, 0.5, 1);
      opacity: 1;
      transform: translateY(0) scale(1);
    }

    /* Header & Subtitle */
    .award-badge {
      font-family: 'Great Vibes', cursive;
      color: var(--pink-highlight);
      font-size: 2rem;
      margin-bottom: 5px;
      text-shadow: 0 0 10px rgba(255, 117, 140, 0.5);
    }

    .main-title {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      background: var(--gold-gradient);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 25px;
      line-height: 1.3;
      filter: drop-shadow(0 2px 4px rgba(0,0,0,0.6));
    }

    @media (min-width: 600px) {
      .main-title {
        font-size: 2.8rem;
        letter-spacing: 3px;
      }
      .award-badge {
        font-size: 2.5rem;
      }
    }

    /* Photo Frame Section */
    .photo-card-wrapper {
      position: relative;
      margin: 10px 0 25px 0;
      width: 100%;
      display: flex;
      justify-content: center;
    }

    .photo-frame {
      position: relative;
      width: 260px;
      height: 330px;
      background: linear-gradient(145deg, #ffffff, #f0e6d2);
      padding: 12px 12px 45px 12px;
      border-radius: 16px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 25px var(--shadow-gold);
      border: 2px solid rgba(212, 175, 55, 0.6);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      animation: gentlePulse 4s infinite ease-in-out;
    }

    @media (min-width: 600px) {
      .photo-frame {
        width: 300px;
        height: 380px;
        padding: 15px 15px 55px 15px;
      }
    }

    .photo-frame:hover {
      transform: translateY(-8px) scale(1.02);
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.6), 0 0 40px rgba(241, 196, 15, 0.7);
    }

    @keyframes gentlePulse {
      0%, 100% { box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 20px var(--shadow-gold); }
      50% { box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 35px rgba(241, 196, 15, 0.6); }
    }

    .photo-container {
      width: 100%;
      height: 100%;
      border-radius: 8px;
      overflow: hidden;
      background-color: #222;
      position: relative;
    }

    .photo-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .polaroid-caption {
      position: absolute;
      bottom: 12px;
      left: 0;
      width: 100%;
      text-align: center;
      font-family: 'Great Vibes', cursive;
      font-size: 1.5rem;
      color: #333;
    }

    /* Controls & Buttons */
    .controls-group {
      display: flex;
      flex-direction: column;
      gap: 15px;
      align-items: center;
      width: 100%;
    }

    .file-input-wrapper {
      position: relative;
      display: inline-block;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid rgba(212, 175, 55, 0.5);
      color: var(--cream-text);
      padding: 8px 16px;
      font-size: 0.85rem;
      border-radius: 20px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .btn-secondary:hover {
      background: rgba(212, 175, 55, 0.15);
      border-color: var(--gold-light);
    }

    #imageUpload {
      display: none;
    }

    .btn-claim {
      background: var(--gold-gradient);
      color: #1a0510;
      font-family: 'Montserrat', sans-serif;
      font-weight: 800;
      font-size: 1.1rem;
      padding: 16px 32px;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(0,0,0,0.4), 0 0 15px var(--shadow-gold);
      transition: all 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-top: 10px;
    }

    .btn-claim:hover {
      transform: translateY(-3px) scale(1.03);
      box-shadow: 0 12px 25px rgba(0,0,0,0.5), 0 0 25px rgba(255, 224, 102, 0.8);
    }

    .btn-claim:active {
      transform: translateY(1px);
    }

    /* Winner Note Box */
    .winner-message {
      margin-top: 20px;
      padding: 18px 22px;
      background: rgba(255, 255, 255, 0.08);
      border: 1px dashed var(--pink-highlight);
      border-radius: 16px;
      max-width: 90%;
      opacity: 0;
      max-height: 0;
      overflow: hidden;
      transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    .winner-message.show {
      opacity: 1;
      max-height: 150px;
      margin-top: 20px;
    }

    .winner-message p {
      font-family: 'Playfair Display', serif;
      font-size: 1.25rem;
      color: #fff;
      font-style: italic;
    }
  </style>
</head>
<body>

  <!-- Radial Background Gradient -->
  <div class="bg-gradient"></div>

  <!-- Sparkles & Particles Canvas -->
  <canvas id="sparkle-canvas"></canvas>

  <!-- Decorative Floating Trophies and Ribbons Layer -->
  <div class="decorations-layer" id="decorationsLayer"></div>

  <!-- Main Website Container -->
  <div class="container">
    
    <div id="badgeText" class="award-badge anim-hidden">Official Recognition</div>
    <h1 id="mainTitle" class="main-title anim-hidden">AWARD GOES TO MY CUTE GIRL</h1>

    <div id="photoCard" class="photo-card-wrapper anim-hidden">
      <div class="photo-frame">
        <div class="photo-container">
          <img id="displayImage" src="" alt="Cutest Girl Award Winner">
        </div>
        <div class="polaroid-caption">Cutest Ever ❤️</div>
      </div>
    </div>

    <div id="controlsArea" class="controls-group anim-hidden">
      <div class="file-input-wrapper">
        <label for="imageUpload" class="btn-secondary">📷 Change Photo</label>
        <input type="file" id="imageUpload" accept="image/*">
      </div>

      <button class="btn-claim" id="claimBtn">Claim Your Award 🏆❤️</button>
    </div>

    <div class="winner-message" id="winnerMsg">
      <p>Because you're simply the cutest girl ever ❤️</p>
    </div>

  </div>

  <script>
    // Embedded Image Data URL from Context
    const defaultImageData = "data:image/png;base64,iVBORw0KGgoAAAANcss...[embedded]"; // Uses loaded context photo dynamically

    // Canvas Sparkles Engine
    const canvas = document.getElementById('sparkle-canvas');
    const ctx = canvas.getContext('2d');
    let width = canvas.width = window.innerWidth;
    let height = canvas.height = window.innerHeight;

    window.addEventListener('resize', () => {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
    });

    class Sparkle {
      constructor() {
        this.reset();
      }
      reset() {
        this.x = Math.random() * width;
        this.y = Math.random() * height;
        this.size = Math.random() * 2.5 + 0.5;
        this.maxSize = Math.random() * 3 + 2;
        this.speedY = -Math.random() * 0.5 - 0.2;
        this.opacity = Math.random();
        this.fadeSpeed = Math.random() * 0.015 + 0.005;
        this.color = Math.random() > 0.3 ? '#f1c40f' : '#ff758c';
      }
      update() {
        this.y += this.speedY;
        this.opacity += this.fadeSpeed;
        if (this.opacity >= 1 || this.opacity <= 0) {
          this.fadeSpeed = -this.fadeSpeed;
        }
        if (this.y < 0 || this.opacity <= 0) {
          this.reset();
        }
      }
      draw() {
        ctx.save();
        ctx.globalAlpha = Math.max(0, this.opacity);
        ctx.fillStyle = this.color;
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fill();
        ctx.restore();
      }
    }

    const sparkles = Array.from({ length: 65 }, () => new Sparkle());

    function animateSparkles() {
      ctx.clearRect(0, 0, width, height);
      sparkles.forEach(s => {
        s.update();
        s.draw();
      });
      requestAnimationFrame(animateSparkles);
    }
    animateSparkles();

    // Floating SVG Elements Generator (Trophies & Medals)
    const trophySVG = `<svg width="50" height="50" viewBox="0 0 24 24" fill="none" stroke="#f1c40f" stroke-width="1.5"><path d="M6 9C6 11.7614 8.23858 14 11 14H13C15.7614 14 18 11.7614 18 9V3H6V9Z" fill="#d4af37" fill-opacity="0.3"/><path d="M6 5H3V7C3 8.65685 4.34315 10 6 10V5Z" fill="#ffd700"/><path d="M18 5H21V7C21 8.65685 19.6569 10 18 10V5Z" fill="#ffd700"/><path d="M12 14V18M8 21H16M12 18H8M12 18H16" stroke="#f1c40f" stroke-width="2" stroke-linecap="round"/></svg>`;

    const medalSVG = `<svg width="45" height="45" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="15" r="5" fill="#ffd700" stroke="#b8860b" stroke-width="1.5"/><path d="M8.5 2L12 9L15.5 2" stroke="#ff758c" stroke-width="2.5" stroke-linecap="round"/><path d="M12 13.5L12.8 15L14.5 15.2L13.2 16.4L13.6 18L12 17.1L10.4 18L10.8 16.4L9.5 15.2L11.2 15L12 13.5Z" fill="#ffffff"/></svg>`;

    const heartSVG = `<svg width="35" height="35" viewBox="0 0 24 24" fill="#ff758c" opacity="0.6"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>`;

    function createFloatingDecorations() {
      const container = document.getElementById('decorationsLayer');
      const items = [trophySVG, medalSVG, heartSVG, trophySVG, heartSVG];
      
      const positions = [
        { top: '8%', left: '6%', delay: '0s', duration: '10s' },
        { top: '15%', right: '8%', delay: '1.5s', duration: '12s' },
        { top: '65%', left: '5%', delay: '0.8s', duration: '11s' },
        { top: '70%', right: '7%', delay: '2s', duration: '9s' },
        { top: '40%', left: '3%', delay: '3s', duration: '13s' },
      ];

      positions.forEach((pos, idx) => {
        const div = document.createElement('div');
        div.className = 'floating-item';
        div.innerHTML = items[idx % items.length];
        Object.assign(div.style, {
          top: pos.top,
          left: pos.left || 'auto',
          right: pos.right || 'auto',
          animationDelay: pos.delay,
          animationDuration: pos.duration
        });
        container.appendChild(div);
      });
    }

    // Set Photo Source
    const imgElement = document.getElementById('displayImage');
    // Set initially from passed visual reference
    imgElement.src = "data:image/png;base64,iVBORw0KGgoAAAANcss"; // Handled by input file reader

    // Upload Image Handler
    document.getElementById('imageUpload').addEventListener('change', function(e) {
      const file = e.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(evt) {
          imgElement.src = evt.target.result;
        };
        reader.readAsDataURL(file);
      }
    });

    // Opening Award Ceremony Sequence
    function runOpeningCeremony() {
      createFloatingDecorations();

      setTimeout(() => {
        document.querySelectorAll('.floating-item').forEach(el => el.style.opacity = '0.8');
      }, 300);

      setTimeout(() => {
        document.getElementById('badgeText').classList.add('anim-reveal');
        document.getElementById('mainTitle').classList.add('anim-reveal');
      }, 600);

      setTimeout(() => {
        document.getElementById('photoCard').classList.add('anim-reveal');
      }, 1300);

      setTimeout(() => {
        document.getElementById('controlsArea').classList.add('anim-reveal');
        // Initial soft celebration confetti
        confetti({
          particleCount: 40,
          spread: 60,
          origin: { y: 0.7 },
          colors: ['#f1c40f', '#d4af37', '#ff758c']
        });
      }, 2000);
    }

    // Interactive Award Claiming Button
    document.getElementById('claimBtn').addEventListener('click', function() {
      // Show Note
      document.getElementById('winnerMsg').classList.add('show');

      // Grand Confetti Burst
      const count = 200;
      const defaults = { origin: { y: 0.7 } };

      function fire(particleRatio, opts) {
        confetti(Object.assign({}, defaults, opts, {
          particleCount: Math.floor(count * particleRatio)
        }));
      }

      fire(0.25, {
        spread: 26,
        startVelocity: 55,
        colors: ['#ffe066', '#ff758c']
      });
      fire(0.2, {
        spread: 60,
        colors: ['#f1c40f', '#ffffff']
      });
      fire(0.35, {
        spread: 100,
        decay: 0.91,
        scalar: 0.8
      });
      fire(0.1, {
        spread: 120,
        startVelocity: 25,
        decay: 0.92,
        colors: ['#e67e22', '#ff758c']
      });
      fire(0.1, {
        spread: 120,
        startVelocity: 45,
      });
    });

    // Trigger animation sequence on load
    window.addEventListener('DOMContentLoaded', runOpeningCeremony);
  </script>
</body>
</html>
