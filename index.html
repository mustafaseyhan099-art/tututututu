<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mms.com - 3D Rengarenk Dünya Haritası</title>

  <!-- Three.js ve OrbitControls Kütüphaneleri -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;700;900&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-dark: #02040a;
      --card-bg: rgba(10, 15, 30, 0.85);
      --border-color: rgba(255, 255, 255, 0.15);
      --text-main: #f3f4f6;
      --text-muted: #9ca3af;
      --accent-rainbow: linear-gradient(135deg, #ff007f, #7928ca, #00dfd8, #00f0ff);
      --accent-green: #10b981;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; user-select: none; }

    body {
      font-family: 'Outfit', sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      overflow: hidden;
      height: 100vh;
      width: 100vw;
    }

    #webgl-container {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 1;
      cursor: grab;
    }

    #webgl-container:active { cursor: grabbing; }

    .ui-layer {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 10;
      pointer-events: none;
      display: grid;
      grid-template-rows: auto 1fr;
      padding: 16px;
    }

    .ui-layer * { pointer-events: auto; }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: var(--card-bg);
      backdrop-filter: blur(16px);
      border: 1px solid var(--border-color);
      padding: 10px 20px;
      border-radius: 16px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
      gap: 12px;
    }

    .brand { display: flex; align-items: center; gap: 12px; }

    .brand-logo {
      width: 40px; height: 40px;
      background: var(--accent-rainbow);
      background-size: 200% 200%;
      animation: pulseGlow 4s infinite alternate;
      border-radius: 10px;
      display: flex; align-items: center; justify-content: center;
      color: white; font-weight: 900; font-size: 1.2rem;
    }

    @keyframes pulseGlow {
      0% { background-position: 0% 50%; transform: scale(1); }
      100% { background-position: 100% 50%; transform: scale(1.05); }
    }

    .brand-title {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.3rem; font-weight: 700;
      background: linear-gradient(90deg, #ffffff, #00dfd8, #ff007f);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .header-controls { display: flex; gap: 8px; align-items: center; flex-wrap: wrap; }

    .btn-action {
      background: rgba(255, 255, 255, 0.08);
      border: 1px solid var(--border-color);
      color: white; padding: 8px 14px;
      border-radius: 10px; cursor: pointer;
      display: flex; align-items: center; gap: 6px;
      font-size: 0.85rem; font-weight: 600;
      transition: all 0.2s ease;
    }

    .btn-action:hover {
      background: rgba(255, 255, 255, 0.2);
      transform: translateY(-2px);
    }

    .btn-rgb {
      background: var(--accent-rainbow);
      border: none;
      box-shadow: 0 0 15px rgba(0, 223, 216, 0.6);
    }

    .music-widget {
      display: flex;
      align-items: center;
      gap: 8px;
      background: rgba(16, 185, 129, 0.15);
      border: 1px solid rgba(16, 185, 129, 0.4);
      padding: 4px 10px;
      border-radius: 12px;
    }

    .music-btn {
      background: var(--accent-green);
      color: white;
      border: none;
      padding: 6px 12px;
      border-radius: 8px;
      cursor: pointer;
      font-weight: 700;
      font-size: 0.8rem;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.2s ease;
    }

    .music-btn:hover {
      filter: brightness(1.1);
      transform: scale(1.02);
    }

    .volume-slider {
      width: 70px;
      accent-color: var(--accent-green);
      cursor: pointer;
    }

    .main-content {
      display: grid;
      grid-template-columns: 280px 1fr 340px;
      gap: 16px; margin-top: 16px;
      height: calc(100% - 16px);
    }

    .sidebar-left, .sidebar-right {
      background: var(--card-bg);
      backdrop-filter: blur(16px);
      border: 1px solid var(--border-color);
      border-radius: 16px; padding: 16px;
      display: flex; flex-direction: column; gap: 12px;
      overflow: hidden; max-height: calc(100vh - 100px);
    }

    .search-box { position: relative; }

    .search-box input {
      width: 100%; padding: 10px 12px 10px 38px;
      background: rgba(0, 0, 0, 0.4);
      border: 1px solid var(--border-color);
      border-radius: 10px; color: white;
      outline: none; font-size: 0.9rem;
    }

    .search-box i {
      position: absolute; left: 12px; top: 50%;
      transform: translateY(-50%); color: var(--text-muted);
    }

    .continent-chips { display: flex; gap: 4px; flex-wrap: wrap; }

    .chip {
      padding: 4px 8px; border-radius: 12px; font-size: 0.7rem;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid var(--border-color); cursor: pointer;
      transition: all 0.2s ease;
    }

    .chip.active { background: #00dfd8; color: #000; font-weight: 700; }

    .country-list {
      overflow-y: auto; display: flex; flex-direction: column;
      gap: 6px; padding-right: 4px;
    }

    .country-list::-webkit-scrollbar { width: 4px; }
    .country-list::-webkit-scrollbar-thumb { background: rgba(255,255,255,0.2); border-radius: 4px; }

    .country-item {
      padding: 10px 12px; border-radius: 10px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid transparent; cursor: pointer;
      display: flex; align-items: center; justify-content: space-between;
      transition: all 0.2s ease;
    }

    .country-item:hover, .country-item.active {
      background: rgba(255, 255, 255, 0.12);
      border-color: rgba(0, 223, 216, 0.5);
      transform: translateX(4px);
    }

    .country-info-mini { display: flex; align-items: center; gap: 8px; }

    .country-detail-panel {
      display: flex; flex-direction: column; gap: 14px;
      overflow-y: auto; height: 100%;
    }

    .country-header {
      display: flex; align-items: center; gap: 12px;
      border-bottom: 1px solid var(--border-color); padding-bottom: 12px;
    }

    .country-flag-large {
      font-size: 2.5rem; background: rgba(255,255,255,0.05);
      padding: 6px; border-radius: 12px;
    }

    .tabs {
      display: flex; gap: 6px; background: rgba(0,0,0,0.4);
      padding: 4px; border-radius: 10px;
    }

    .tab-btn {
      flex: 1; padding: 6px; border: none; background: transparent;
      color: var(--text-muted); border-radius: 6px; cursor: pointer;
      font-weight: 600; font-size: 0.8rem;
      display: flex; align-items: center; justify-content: center; gap: 4px;
      transition: all 0.2s ease;
    }

    .tab-btn.active { background: rgba(255,255,255,0.2); color: white; }

    .tab-content { display: none; }
    .tab-content.active { display: flex; flex-direction: column; gap: 10px; }

    .data-card {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 12px; padding: 12px;
      display: flex; flex-direction: column; gap: 4px;
    }

    .data-card-header {
      display: flex; justify-content: space-between; align-items: center;
      font-weight: 700; color: #00dfd8; font-size: 0.9rem;
    }

    .legend-box {
      position: absolute; bottom: 16px; left: 310px;
      background: var(--card-bg); backdrop-filter: blur(16px);
      border: 1px solid var(--border-color); border-radius: 12px;
      padding: 8px 14px; display: flex; gap: 12px; align-items: center;
    }

    .legend-item { display: flex; align-items: center; gap: 6px; font-size: 0.75rem; }

    .legend-color {
      width: 10px; height: 10px; border-radius: 50%;
      box-shadow: 0 0 6px currentColor;
    }
  </style>
</head>
<body>

  <!-- Yerel MP3 ve İnternet Akış Kaynağı -->
  <audio id="bgAudio" loop preload="auto">
    <source src="muzik.mp3" type="audio/mpeg">
    <source src="https://upload.wikimedia.org/wikipedia/commons/e/e8/Grieg_Morning_Mood.ogg" type="audio/ogg">
  </audio>

  <div id="webgl-container"></div>

  <div class="ui-layer">
    <header>
      <div class="brand">
        <div class="brand-logo">M</div>
        <div>
          <div class="brand-title">Mms.com</div>
          <div style="font-size: 0.7rem; color: var(--text-muted);">3D İnteraktif Keşif Dünyası</div>
        </div>
      </div>

      <div class="header-controls">
        <!-- Grow a Garden Müzik Kontrolcüsü -->
        <div class="music-widget">
          <button class="music-btn" id="musicToggleBtn" onclick="toggleAudio()">
            <i data-lucide="music"></i> <span id="musicBtnText">Müzik Çal</span>
          </button>
          <i data-lucide="volume-2" style="width: 14px; color: var(--accent-green);"></i>
          <input type="range" class="volume-slider" id="volumeSlider" min="0" max="1" step="0.05" value="0.7" oninput="changeVolume(this.value)">
        </div>

        <button class="btn-action btn-rgb" onclick="toggleRainbowMode()">
          <i data-lucide="sparkles"></i> 🌈 Rengarenk Mod: <span id="rgb-status">AÇIK</span>
        </button>
        <button class="btn-action" onclick="toggleAutoRotate()">
          <i data-lucide="rotate-cw" id="rotate-icon"></i> Dönüşü Durdur/Aç
        </button>
        <button class="btn-action" onclick="selectRandomCountry()">
          <i data-lucide="shuffle"></i> Rastgele Keşfet
        </button>
      </div>
    </header>

    <div class="main-content">
      <!-- Sol Ülke Listesi -->
      <div class="sidebar-left">
        <div class="search-box">
          <i data-lucide="search"></i>
          <input type="text" id="searchInput" placeholder="Ülke, icat veya hayvan ara..." oninput="filterCountries()">
        </div>

        <div class="continent-chips" id="continentChips">
          <div class="chip active" onclick="filterContinent('ALL', this)">Tümü</div>
          <div class="chip" onclick="filterContinent('Europe', this)">Avrupa</div>
          <div class="chip" onclick="filterContinent('Asia', this)">Asya</div>
          <div class="chip" onclick="filterContinent('North America', this)">K. Amerika</div>
          <div class="chip" onclick="filterContinent('South America', this)">G. Amerika</div>
          <div class="chip" onclick="filterContinent('Africa', this)">Afrika</div>
          <div class="chip" onclick="filterContinent('Oceania', this)">Okyanusya</div>
        </div>

        <div class="country-list" id="countryList"></div>
      </div>

      <div></div>

      <!-- Sağ Detay Paneli -->
      <div class="sidebar-right">
        <div id="countryDetail" class="country-detail-panel">
          <div style="text-align: center; margin-top: 60px; color: var(--text-muted);">
            <i data-lucide="globe" style="width: 48px; height: 48px; opacity: 0.4; margin-bottom: 12px;"></i>
            <p>Dünyayı fare ile çevirebilir, tıklayarak icatları ve hayvanları görebilirsiniz!</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Kıta Renkleri Efsanesi -->
    <div class="legend-box">
      <div class="legend-item"><div class="legend-color" style="background:#00f0ff; color:#00f0ff;"></div> Avrupa</div>
      <div class="legend-item"><div class="legend-color" style="background:#ff3366; color:#ff3366;"></div> Asya</div>
      <div class="legend-item"><div class="legend-color" style="background:#e040fb; color:#e040fb;"></div> K. Amerika</div>
      <div class="legend-item"><div class="legend-color" style="background:#00e676; color:#00e676;"></div> G. Amerika</div>
      <div class="legend-item"><div class="legend-color" style="background:#ffd600; color:#ffd600;"></div> Afrika</div>
      <div class="legend-item"><div class="legend-color" style="background:#ff9100; color:#ff9100;"></div> Okyanusya</div>
    </div>
  </div>

  <script>
    const countriesData = [
      {
        id: "TR", name: "Türkiye", flag: "🇹🇷", continent: "Europe", lat: 38.9637, lng: 35.2433, capital: "Ankara", population: "85 Milyon",
        inventions: [
          { title: "El-Cezeri Otomatları & Su Saatleri", year: "1200", desc: "İlk sibernetik ve robotik otomatik makineler." },
          { title: "Modern Biyomedikal Geliştirmeler", year: "Günümüz", desc: "Cerrahi aletler ve kanser araştırma teknolojileri." }
        ],
        wildlife: [
          { name: "Anadolu Parsı", desc: "Anadolu dağlarında yaşayan nadir leopar türü." },
          { name: "Van Kedisi", desc: "Farklı renkli gözleri ve suda yüzmesiyle meşhur endemik kedi." }
        ]
      },
      {
        id: "JP", name: "Japonya", flag: "🇯🇵", continent: "Asia", lat: 36.2048, lng: 138.2529, capital: "Tokyo", population: "125 Milyon",
        inventions: [
          { title: "Mermer Hızlı Tren (Shinkansen)", year: "1964", desc: "Dünyanın ilk yüksek hızlı tren hattı." },
          { title: "QR Kod Teknolojisi", year: "1994", desc: "Lojistik takibi için icat edilen 2D barkod sistemi." }
        ],
        wildlife: [
          { name: "Japon Kar Maymunu", desc: "Sıcak kaplıcalarda yıkanan özel şebek türü." },
          { name: "Dev Japon Semenderi", desc: "Nehirlerde yaşayan dev amfibi." }
        ]
      },
      {
        id: "DE", name: "Almanya", flag: "🇩🇪", continent: "Europe", lat: 51.1657, lng: 10.4515, capital: "Berlin", population: "83 Milyon",
        inventions: [
          { title: "Benzinli Otomobil", year: "1886", desc: "Karl Benz tarafından tasarlanan ilk modern araba." },
          { title: "Matbaa", year: "1440", desc: "Gutenberg'in geliştirdiği hareketli tip matbaa makinesi." }
        ],
        wildlife: [
          { name: "Avrupa Porsuğu", desc: "Ormanlarda karmaşık tüneller açan gececil canlı." },
          { name: "Kızıl Geyik", desc: "Bavyera ormanlarının görkemli geyiği." }
        ]
      },
      {
        id: "US", name: "ABD", flag: "🇺🇸", continent: "North America", lat: 37.0902, lng: -95.7129, capital: "Washington D.C.", population: "331 Milyon",
        inventions: [
          { title: "Pratik Elektrik Ampulü", year: "1879", desc: "Thomas Edison tarafından geliştirilen uzun ömürlü ampul." },
          { title: "Motorlu Uçak", year: "1903", desc: "Wright Kardeşler'in gerçekleştirdiği ilk motorlu uçuş." }
        ],
        wildlife: [
          { name: "Amerikan Bizonu", desc: "Kuzey Amerika bozkırlarının devasa otobur memelisi." },
          { name: "Kel Kartal", desc: "ABD'nin simgesi olan keskin görüşlü yırtıcı kuş." }
        ]
      },
      {
        id: "BR", name: "Brezilya", flag: "🇧🇷", continent: "South America", lat: -14.2350, lng: -51.9253, capital: "Brasília", population: "214 Milyon",
        inventions: [
          { title: "Arayan Kimliği (Caller ID)", year: "1982", desc: "Telefonda arayanı gösteren teknolojinin doğuşu." },
          { title: "14-bis Uçağı", year: "1906", desc: "Santos-Dumont'un yardım almadan havalanan ilk uçağı." }
        ],
        wildlife: [
          { name: "Jaguar", desc: "Amazon yağmur ormanlarının en büyük yırtıcı kedisi." },
          { name: "Kapibara", desc: "Suda yaşayan dünyanın en büyük kemirgeni." }
        ]
      },
      {
        id: "EG", name: "Mısır", flag: "🇪🇬", continent: "Africa", lat: 26.8206, lng: 30.8025, capital: "Kahire", population: "104 Milyon",
        inventions: [
          { title: "Papirüs Kağıdı", year: "MÖ 3000", desc: "İnsanlık tarihinin ilk yazı kağıdı." },
          { title: "Güneş Takvimi", year: "MÖ 4000", desc: "365 güne dayalı hassas takvim hesaplaması." }
        ],
        wildlife: [
          { name: "Çöl Tilkisi (Fennec)", desc: "Dev kulaklarıyla çöl sıcaklığını dağıtan şirin tilki." },
          { name: "Mısır Kobrası", desc: "Çöllerde yaşayan yüksek zehirli kobra türü." }
        ]
      },
      {
        id: "AU", name: "Avustralya", flag: "🇦🇺", continent: "Oceania", lat: -25.2744, lng: 133.7751, capital: "Canberra", population: "25 Milyon",
        inventions: [
          { title: "Uçak Kara Kutusu", year: "1953", desc: "Uçuş verilerini kaydeden güvenlik cihazı." },
          { title: "Wi-Fi Algoritması", year: "1992", desc: "Kablosuz hızlı internetin temel çekirdek patenti." }
        ],
        wildlife: [
          { name: "Kanguru", desc: "Zıplayarak hareket eden keseli simge hayvan." },
          { name: "Koala", desc: "Okaliptüs ağaçlarında yaşayan sevimli otobur." }
        ]
      }
    ];

    let scene, camera, renderer, controls;
    let globe, atmosphere, dirLight;
    const markers = [];
    let autoRotate = true;
    let isRainbowMode = true;
    let hue = 0;
    let isAudioPlaying = false;
    let audioCtx = null;

    let pointerDownPos = { x: 0, y: 0 };

    const continentColors = {
      "Europe": 0x00f0ff,
      "Asia": 0xff3366,
      "North America": 0xe040fb,
      "South America": 0x00e676,
      "Africa": 0xffd600,
      "Oceania": 0xff9100
    };

    function playSynthFallback() {
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === 'suspended') audioCtx.resume();

      const notes = [261.63, 329.63, 392.00, 523.25, 659.25];
      let noteIndex = 0;

      function playNote() {
        if (!isAudioPlaying) return;
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'triangle';
        osc.frequency.setValueAtTime(notes[noteIndex % notes.length], audioCtx.currentTime);
        
        gain.gain.setValueAtTime(0.15, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 1.2);

        osc.connect(gain);
        gain.connect(audioCtx.destination);

        osc.start();
        osc.stop(audioCtx.currentTime + 1.2);

        noteIndex++;
        setTimeout(playNote, 600);
      }
      playNote();
    }

    function toggleAudio() {
      const audio = document.getElementById('bgAudio');
      const btnText = document.getElementById('musicBtnText');

      if (!isAudioPlaying) {
        audio.volume = document.getElementById('volumeSlider').value;
        const playPromise = audio.play();
        
        if (playPromise !== undefined) {
          playPromise.then(() => {
            isAudioPlaying = true;
            btnText.innerText = "Müziği Durdur";
          }).catch(err => {
            isAudioPlaying = true;
            btnText.innerText = "Müziği Durdur";
            playSynthFallback();
          });
        }
      } else {
        audio.pause();
        isAudioPlaying = false;
        btnText.innerText = "Müzik Çal";
      }
    }

    function changeVolume(val) {
      const audio = document.getElementById('bgAudio');
      audio.volume = val;
    }

    function init3D() {
      const container = document.getElementById('webgl-container');

      scene = new THREE.Scene();
      camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
      camera.position.set(0, 0, 320);

      renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
      renderer.setSize(window.innerWidth, window.innerHeight);
      renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
      container.appendChild(renderer.domElement);

      controls = new THREE.OrbitControls(camera, renderer.domElement);
      controls.enableDamping = true;
      controls.dampingFactor = 0.05;
      controls.rotateSpeed = 0.8;
      controls.zoomSpeed = 1.2;
      controls.minDistance = 140;
      controls.maxDistance = 500;

      scene.add(new THREE.AmbientLight(0xffffff, 0.8));
      dirLight = new THREE.DirectionalLight(0x00f0ff, 1.5);
      dirLight.position.set(400, 200, 400);
      scene.add(dirLight);

      const sphereGeo = new THREE.SphereGeometry(100, 64, 64);
      const texture = new THREE.CanvasTexture(generateProceduralGlobe());

      const globeMat = new THREE.MeshStandardMaterial({
        map: texture,
        roughness: 0.4,
        metalness: 0.2
      });

      globe = new THREE.Mesh(sphereGeo, globeMat);
      scene.add(globe);

      const atmosGeo = new THREE.SphereGeometry(104, 64, 64);
      const atmosMat = new THREE.ShaderMaterial({
        vertexShader: `
          varying vec3 vNormal;
          void main() {
            vNormal = normalize(normalMatrix * normal);
            gl_Position = projectionMatrix * modelViewMatrix * vec4(position, 1.0);
          }
        `,
        fragmentShader: `
          varying vec3 vNormal;
          uniform vec3 color;
          void main() {
            float intensity = pow(0.65 - dot(vNormal, vec3(0, 0, 1.0)), 2.0);
            gl_FragColor = vec4(color, 1.0) * intensity;
          }
        `,
        uniforms: { color: { value: new THREE.Color(0x00dfd8) } },
        blending: THREE.AdditiveBlending,
        side: THREE.BackSide,
        transparent: true
      });
      atmosphere = new THREE.Mesh(atmosGeo, atmosMat);
      scene.add(atmosphere);

      createStars();
      createMarkers();

      window.addEventListener('resize', onResize);

      renderer.domElement.addEventListener('pointerdown', (e) => {
        pointerDownPos = { x: e.clientX, y: e.clientY };
      });

      renderer.domElement.addEventListener('pointerup', (e) => {
        const dist = Math.hypot(e.clientX - pointerDownPos.x, e.clientY - pointerDownPos.y);
        if (dist < 5) onClick(e);
      });

      animate();
    }

    function generateProceduralGlobe() {
      const canvas = document.createElement('canvas');
      canvas.width = 1024; canvas.height = 512;
      const ctx = canvas.getContext('2d');

      ctx.fillStyle = '#0a0d24';
      ctx.fillRect(0, 0, canvas.width, canvas.height);

      ctx.strokeStyle = 'rgba(0, 240, 255, 0.25)';
      ctx.lineWidth = 1;
      for (let x = 0; x < canvas.width; x += 32) {
        ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, canvas.height); ctx.stroke();
      }
      for (let y = 0; y < canvas.height; y += 32) {
        ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(canvas.width, y); ctx.stroke();
      }

      return canvas;
    }

    function createStars() {
      const geo = new THREE.BufferGeometry();
      const pos = new Float32Array(1500 * 3);
      for(let i=0; i<4500; i++) pos[i] = (Math.random() - 0.5) * 1000;
      geo.setAttribute('position', new THREE.BufferAttribute(pos, 3));
      const mat = new THREE.PointsMaterial({ color: 0xffffff, size: 1 });
      scene.add(new THREE.Points(geo, mat));
    }

    function latLngToVec3(lat, lng, r) {
      const phi = (90 - lat) * (Math.PI / 180);
      const theta = (lng + 180) * (Math.PI / 180);
      return new THREE.Vector3(
        -(r * Math.sin(phi) * Math.cos(theta)),
        (r * Math.cos(phi)),
        (r * Math.sin(phi) * Math.sin(theta))
      );
    }

    function createMarkers() {
      countriesData.forEach(country => {
        const pos = latLngToVec3(country.lat, country.lng, 101);
        const col = continentColors[country.continent] || 0x00f0ff;

        const group = new THREE.Group();
        group.position.copy(pos);

        const dot = new THREE.Mesh(
          new THREE.SphereGeometry(2.2, 16, 16),
          new THREE.MeshBasicMaterial({ color: col })
        );
        group.add(dot);

        group.userData = country;
        globe.add(group);
        markers.push(group);
      });
    }

    function animate() {
      requestAnimationFrame(animate);

      if (autoRotate) globe.rotation.y += 0.0025;

      if (isRainbowMode) {
        hue += 0.004;
        if (hue > 1) hue = 0;
        const rgbColor = new THREE.Color().setHSL(hue, 0.9, 0.5);
        atmosphere.material.uniforms.color.value = rgbColor;
        dirLight.color = rgbColor;
      }

      controls.update();
      renderer.render(scene, camera);
    }

    function onClick(e) {
      const mouse = new THREE.Vector2(
        (e.clientX / window.innerWidth) * 2 - 1,
        -(e.clientY / window.innerHeight) * 2 + 1
      );
      const ray = new THREE.Raycaster();
      ray.setFromCamera(mouse, camera);

      const hits = ray.intersectObjects(markers, true);
      if (hits.length > 0) {
        let target = hits[0].object;
        while (target.parent && !target.userData.id) target = target.parent;
        if (target.userData.id) selectCountry(target.userData);
      }
    }

    function selectCountry(country) {
      const targetPos = latLngToVec3(country.lat, country.lng, 250);
      let p = 0;
      const startPos = camera.position.clone();

      function move() {
        p += 0.05;
        if (p <= 1) {
          camera.position.lerpVectors(startPos, targetPos, p);
          requestAnimationFrame(move);
        }
      }
      move();

      renderDetail(country);
      confetti({ particleCount: 35, spread: 60 });
    }

    function renderDetail(country) {
      const panel = document.getElementById('countryDetail');
      panel.innerHTML = `
        <div class="country-header">
          <div class="country-flag-large">${country.flag}</div>
          <div>
            <h2 style="font-size: 1.4rem;">${country.name}</h2>
            <div style="font-size: 0.8rem; color: var(--text-muted);">${country.capital} • ${country.population}</div>
          </div>
        </div>

        <div class="tabs">
          <button class="tab-btn active" onclick="switchTab('inventions', this)">
            <i data-lucide="lightbulb" style="width:14px;"></i> İcatlar
          </button>
          <button class="tab-btn" onclick="switchTab('wildlife', this)">
            <i data-lucide="paw-print" style="width:14px;"></i> Hayvanlar
          </button>
        </div>

        <div id="tab-inventions" class="tab-content active">
          ${country.inventions.map(i => `
            <div class="data-card">
              <div class="data-card-header">
                <span>${i.title}</span>
                <span style="font-size: 0.7rem; background: rgba(0,223,216,0.2); padding: 2px 6px; border-radius: 8px;">${i.year}</span>
              </div>
              <p style="font-size: 0.8rem; color: #d1d5db; margin-top: 4px;">${i.desc}</p>
            </div>
          `).join('')}
        </div>

        <div id="tab-wildlife" class="tab-content">
          ${country.wildlife.map(w => `
            <div class="data-card">
              <div class="data-card-header" style="color: #00e676;">
                <span>🐾 ${w.name}</span>
              </div>
              <p style="font-size: 0.8rem; color: #d1d5db; margin-top: 4px;">${w.desc}</p>
            </div>
          `).join('')}
        </div>
      `;
      lucide.createIcons();
    }

    function switchTab(tab, btn) {
      document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
      document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById(`tab-${tab}`).classList.add('active');
    }

    function populateList(list) {
      const c = document.getElementById('countryList');
      c.innerHTML = '';
      list.forEach(item => {
        const div = document.createElement('div');
        div.className = 'country-item';
        div.onclick = () => selectCountry(item);
        div.innerHTML = `
          <div class="country-info-mini">
            <span style="font-size: 1.2rem;">${item.flag}</span>
            <span style="font-weight: 600; font-size: 0.9rem;">${item.name}</span>
          </div>
          <i data-lucide="chevron-right" style="width: 14px; color: var(--text-muted);"></i>
        `;
        c.appendChild(div);
      });
      lucide.createIcons();
    }

    function filterCountries() {
      const q = document.getElementById('searchInput').value.toLowerCase();
      populateList(countriesData.filter(c => c.name.toLowerCase().includes(q)));
    }

    function filterContinent(cont, el) {
      document.querySelectorAll('.chip').forEach(c => c.classList.remove('active'));
      el.classList.add('active');
      populateList(cont === 'ALL' ? countriesData : countriesData.filter(c => c.continent === cont));
    }

    function toggleAutoRotate() { autoRotate = !autoRotate; }

    function toggleRainbowMode() { 
      isRainbowMode = !isRainbowMode; 
      document.getElementById('rgb-status').innerText = isRainbowMode ? "AÇIK" : "KAPALI";
      if(!isRainbowMode) {
        atmosphere.material.uniforms.color.value = new THREE.Color(0x00f0ff);
        dirLight.color = new THREE.Color(0x00f0ff);
      }
    }

    function selectRandomCountry() { 
      selectCountry(countriesData[Math.floor(Math.random() * countriesData.length)]); 
    }

    function onResize() {
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    }

    window.onload = () => {
      init3D();
      populateList(countriesData);
      lucide.createIcons();
    };
  </script>
</body>
</html>
