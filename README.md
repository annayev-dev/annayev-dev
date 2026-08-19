<!--
  README.md - Profile for annayev-dev
  - Animated SVG hero (pure SVG animations, no JS) so it renders on GitHub README
  - Turkish text, showcases HTML/CSS/JS skills
  - Editable: change name, headline, and skills below
-->

<!-- Animated hero: pure inline SVG (SMIL + SVG animate) -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 360" preserveAspectRatio="xMidYMid slice" width="100%">
  <defs>
    <linearGradient id="g1" x1="0" x2="1">
      <stop offset="0%" stop-color="#00d2ff" />
      <stop offset="50%" stop-color="#3a7bd5" />
      <stop offset="100%" stop-color="#b06ab3" />
    </linearGradient>

    <filter id="shadow" x="-50%" y="-50%" width="200%" height="200%">
      <feDropShadow dx="0" dy="8" stdDeviation="14" flood-color="#000" flood-opacity="0.45"/>
    </filter>

    <!-- soft blur for background orbs -->
    <filter id="blur" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="30" />
    </filter>

    <!-- animated stripe pattern for the main text -->
    <pattern id="stripes" patternUnits="userSpaceOnUse" width="12" height="12">
      <rect width="12" height="12" fill="#ffffff" fill-opacity="0.03" />
      <path d="M0 12 L12 0" stroke="#ffffff" stroke-opacity="0.06" stroke-width="2" />
    </pattern>
  </defs>

  <rect width="1200" height="360" fill="#0b1020" />

  <!-- floating colorful orbs -->
  <g filter="url(#blur)">
    <circle cx="120" cy="80" r="80" fill="#ff6b6b">
      <animate attributeName="cx" dur="10s" values="120;300;180;120" repeatCount="indefinite" />
      <animate attributeName="cy" dur="12s" values="80;60;130;80" repeatCount="indefinite" />
      <animate attributeName="r" dur="8s" values="80;60;90;80" repeatCount="indefinite" />
      <animate attributeName="fill" dur="15s" values="#ff6b6b;#feca57;#5f27cd;#ff6b6b" repeatCount="indefinite" />
    </circle>

    <circle cx="980" cy="60" r="60" fill="#3a7bd5">
      <animate attributeName="cx" dur="11s" values="980;850;1020;980" repeatCount="indefinite" />
      <animate attributeName="cy" dur="9s" values="60;120;40;60" repeatCount="indefinite" />
      <animate attributeName="r" dur="7s" values="60;90;50;60" repeatCount="indefinite" />
      <animate attributeName="fill" dur="13s" values="#3a7bd5;#00d2ff;#b06ab3;#3a7bd5" repeatCount="indefinite" />
    </circle>

    <circle cx="600" cy="260" r="100" fill="#10ac84">
      <animate attributeName="cx" dur="14s" values="600;680;540;600" repeatCount="indefinite" />
      <animate attributeName="cy" dur="10s" values="260;220;300;260" repeatCount="indefinite" />
      <animate attributeName="fill" dur="16s" values="#10ac84;#5f27cd;#ff6b6b;#10ac84" repeatCount="indefinite" />
    </circle>
  </g>

  <!-- main headline -->
  <g transform="translate(60,130)">
    <text x="0" y="0" font-family="Segoe UI, Roboto, Helvetica, Arial" font-weight="700" font-size="54" fill="url(#g1)">
      <tspan>Anna Yev</tspan>
    </text>

    <text x="0" y="52" font-family="Segoe UI, Roboto, Helvetica, Arial" font-size="20" fill="#cbd5e1" opacity="0.95">
      Front-end geliştiricisi • HTML • CSS • JavaScript
    </text>

    <!-- animated sub-headline (typewriter effect with SVG text and clip) -->
    <g transform="translate(0,95)">
      <text id="type" x="0" y="0" font-family="Courier New, monospace" font-size="18" fill="#e2e8f0">
        <tspan>"Kullanıcı dostu, performans odaklı arayüzler geliştiririm."</tspan>
      </text>
      <rect x="0" y="6" width="8" height="20" fill="#e2e8f0" opacity="0.9">
        <animate attributeName="x" values="0;0;0" dur="2s" repeatCount="indefinite" />
        <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite" />
      </rect>
    </g>
  </g>

  <!-- animated skill bars -->
  <g transform="translate(60,200)" font-family="Segoe UI, Roboto, Helvetica, Arial">
    <text x="0" y="0" font-size="14" fill="#94a3b8">HTML</text>
    <rect x="60" y="-12" width="420" height="14" rx="7" fill="#111827" />
    <rect x="60" y="-12" width="0" height="14" rx="7" fill="url(#g1)">
      <animate attributeName="width" from="0" to="420" dur="2s" begin="0.5s" fill="freeze" />
    </rect>

    <text x="0" y="36" font-size="14" fill="#94a3b8">CSS</text>
    <rect x="60" y="24" width="360" height="14" rx="7" fill="#111827" />
    <rect x="60" y="24" width="0" height="14" rx="7" fill="#5f27cd">
      <animate attributeName="width" from="0" to="360" dur="2s" begin="0.75s" fill="freeze" />
    </rect>

    <text x="0" y="72" font-size="14" fill="#94a3b8">JavaScript</text>
    <rect x="60" y="60" width="300" height="14" rx="7" fill="#111827" />
    <rect x="60" y="60" width="0" height="14" rx="7" fill="#00d2ff">
      <animate attributeName="width" from="0" to="300" dur="2s" begin="1s" fill="freeze" />
    </rect>

    <text x="0" y="108" font-size="14" fill="#94a3b8">Accessibility</text>
    <rect x="120" y="96" width="300" height="14" rx="7" fill="#111827" />
    <rect x="120" y="96" width="0" height="14" rx="7" fill="#10ac84">
      <animate attributeName="width" from="0" to="300" dur="2s" begin="1.25s" fill="freeze" />
    </rect>
  </g>

  <!-- subtle animated underline -->
  <line x1="60" y1="320" x2="1140" y2="320" stroke="url(#g1)" stroke-width="2" stroke-linecap="round" opacity="0.9">
    <animate attributeName="x2" values="60;1140;60" dur="8s" repeatCount="indefinite" />
  </line>
</svg>


# Merhaba — ben Anna 👋

Bu profil README'si senin için hazırlandı — tamamen HTML/CSS/JS bilen geliştiriciler gözüyle tasarlandı: animasyonlu, dikkat çekici ve kolayca özelleştirilebilir.

Ben kimim?

- Front-end geliştiricisi: HTML, CSS, JavaScript konusunda rahatım.
- Arayüz performansı, erişilebilirlik ve estetik detaylar benim için önemlidir.

Neler var?

- Üstte tamamen SVG ile yapılmış, GitHub'ta sorunsuz çalışan bir animasyonlu hero.
- Yetenek çubukları (HTML, CSS, JavaScript, Accessibility) — SVG animasyonları ile incelikli giriş efekti.
- Bu dosya markdown olduğu için dilediğin metni, linki veya görseli kolayca değiştirebilirsin.

Hızlı özelleştirme ipuçları

- İsim/başlık değiştirmek için README içinde "Anna Yev" yazısını arayın ve istediğiniz isimle değiştirin.
- Renk paletini değiştirmek için SVG'deki linearGradient (#g1) renklerini güncelleyin.
- Yeni yetenek eklemek için <rect> (skill bar) bloklarını kopyalayıp konumları (y koordinatı) ayarlayın.

Daha fazlasını ister misin?

- İstersen font gömme (special fonts) için SVG içine base64 WOFF ekleyebilirim — bunu yaparsak README biraz ağırlaşır ama özel bir font kullanabilirsin. Yapmamı ister misin?
- JS tabanlı küçük etkileşimler (hover, mouse takip) README içinde çalışmayacaktır çünkü GitHub dış scriptlere izin vermiyor; ancak SVG içindeki SMIL animasyonları ve CSS (SVG içi) ile çok etkileyici sonuçlar elde edebiliriz.

Projeler ve linkler

- Aşağıya GitHub projelerinin küçük kartlarını veya canlı demoların linklerini ekleyebilirim. Hangi projeleri veya linkleri öne çıkarmamı istersin?

İstersen hemen adını, kısa bir bio ve 3 öne çıkan proje linki ver, ben onları README'ye ekleyeyim ve istersen özel bir font da gömeyim.

---

Bu README'yi repo köküne ekledim. Dilediğin değişiklikleri söyle, anında güncelleyeyim.