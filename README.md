<!--
  README.md - Profile for annayev-dev (updated)
  - Animated SVG hero (pure SVG animations, no JS) so it renders on GitHub README
  - Turkish text, showcases HTML/CSS/JS skills
  - Accessibility: title/desc + prefers-reduced-motion handling
  - Project cards (placeholders) + GitHub stats + social links
  - Special font effect using layered SVG text (lightweight). If you want a real embedded font,
    provide a WOFF/WOFF2 file or say "embed font" and I'll add base64-embedded font (increases README size).
-->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 360" preserveAspectRatio="xMidYMid slice" width="100%" role="img" aria-labelledby="titleDesc">
  <title id="titleDesc">Anna Yev — Front-end geliştiricisi</title>
  <desc id="titleDescDesc">Animasyonlu hero: hareketli orblar, yetenek çubukları ve dikkat çekici başlık.</desc>

  <style><![CDATA[
    /* reduced motion: stop animations if user prefers reduced motion */
    @media (prefers-reduced-motion: reduce) {
      * { animation: none !important; }
      .anim { display: none !important; }
      rect[width] { transition: none !important; }
    }

    /* Decorative type treatment fallback to system fonts */
    .headline { font-family: 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; font-weight: 800; }
    .sub { font-family: 'Segoe UI', Roboto, Arial, sans-serif; }
  ]]></style>

  <defs>
    <linearGradient id="g1" x1="0" x2="1">
      <stop offset="0%" stop-color="#00d2ff" />
      <stop offset="50%" stop-color="#3a7bd5" />
      <stop offset="100%" stop-color="#b06ab3" />
    </linearGradient>

    <filter id="blur" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="30" />
    </filter>

    <pattern id="stripes" patternUnits="userSpaceOnUse" width="12" height="12">
      <rect width="12" height="12" fill="#ffffff" fill-opacity="0.03" />
      <path d="M0 12 L12 0" stroke="#ffffff" stroke-opacity="0.06" stroke-width="2" />
    </pattern>
  </defs>

  <rect width="1200" height="360" fill="#0b1020" />

  <!-- floating colorful orbs (decorative) -->
  <g filter="url(#blur)" opacity="0.95">
    <circle cx="120" cy="80" r="80" fill="#ff6b6b" class="orb">
      <animate attributeName="cx" dur="10s" values="120;300;180;120" repeatCount="indefinite" />
      <animate attributeName="cy" dur="12s" values="80;60;130;80" repeatCount="indefinite" />
      <animate attributeName="r" dur="8s" values="80;60;90;80" repeatCount="indefinite" />
    </circle>
    <circle cx="980" cy="60" r="60" fill="#3a7bd5">
      <animate attributeName="cx" dur="11s" values="980;850;1020;980" repeatCount="indefinite" />
      <animate attributeName="cy" dur="9s" values="60;120;40;60" repeatCount="indefinite" />
      <animate attributeName="r" dur="7s" values="60;90;50;60" repeatCount="indefinite" />
    </circle>
    <circle cx="600" cy="260" r="100" fill="#10ac84">
      <animate attributeName="cx" dur="14s" values="600;680;540;600" repeatCount="indefinite" />
      <animate attributeName="cy" dur="10s" values="260;220;300;260" repeatCount="indefinite" />
    </circle>
  </g>

  <!-- headline with layered stroke for 'special font' feel (no external font required) -->
  <g transform="translate(60,120)">
    <!-- shadow layer -->
    <text x="0" y="0" class="headline" font-size="68" fill="#050617" opacity="0.7" style="filter:url(#blur);">
      <tspan>Anna Yev</tspan>
    </text>
    <!-- main gradient text -->
    <text x="0" y="0" class="headline" font-size="68" fill="url(#g1)">
      <tspan>Anna Yev</tspan>
    </text>
    <!-- stripe mask to give texture -->
    <text x="0" y="0" class="headline" font-size="68" fill="url(#stripes)" opacity="0.12">
      <tspan>Anna Yev</tspan>
    </text>

    <text x="0" y="56" class="sub" font-size="18" fill="#cbd5e1">Front-end geliştiricisi • HTML • CSS • JavaScript</text>

    <!-- type caption -->
    <text x="0" y="96" font-family="Courier New, monospace" font-size="15" fill="#e2e8f0">"Kullanıcı dostu, performans odaklı arayüzler geliştiririm."</text>

  </g>

  <!-- skill bars -->
  <g transform="translate(60,200)" font-family="Segoe UI, Roboto, Helvetica, Arial" aria-hidden="true">
    <text x="0" y="0" font-size="14" fill="#94a3b8">HTML</text>
    <rect x="60" y="-12" width="420" height="14" rx="7" fill="#111827" />
    <rect x="60" y="-12" width="0" height="14" rx="7" fill="url(#g1)">
      <animate attributeName="width" from="0" to="420" dur="1200ms" begin="0.4s" fill="freeze" />
    </rect>

    <text x="0" y="36" font-size="14" fill="#94a3b8">CSS</text>
    <rect x="60" y="24" width="360" height="14" rx="7" fill="#111827" />
    <rect x="60" y="24" width="0" height="14" rx="7" fill="#5f27cd">
      <animate attributeName="width" from="0" to="360" dur="1200ms" begin="0.7s" fill="freeze" />
    </rect>

    <text x="0" y="72" font-size="14" fill="#94a3b8">JavaScript</text>
    <rect x="60" y="60" width="300" height="14" rx="7" fill="#111827" />
    <rect x="60" y="60" width="0" height="14" rx="7" fill="#00d2ff">
      <animate attributeName="width" from="0" to="300" dur="1200ms" begin="1s" fill="freeze" />
    </rect>

  </g>

  <!-- underline -->
  <line x1="60" y1="320" x2="1140" y2="320" stroke="url(#g1)" stroke-width="2" stroke-linecap="round" opacity="0.9">
    <animate attributeName="x2" values="60;1140;60" dur="8s" repeatCount="indefinite" />
  </line>
</svg>


# Merhaba — ben Anna 👋

Bu profil README'si tamamen sana özel hazırlandı: animasyonlu, dikkat çekici ve front-end yeteneklerini vurgulayan bir sunum.

Kısa Bio

- Front-end geliştiricisi — HTML, CSS, JavaScript
- Erişilebilir, performans odaklı ve estetik arayüzler geliştiriyorum.

Öne Çıkan Projeler

- [Project 1 — Örnek UI Kit](https://github.com/annayev-dev/project-1) — Minimal, erişilebilir UI bileşen kütüphanesi.
- [Project 2 — Interaktif Demo](https://github.com/annayev-dev/project-2) — JavaScript ile etkileşim örnekleri ve animasyonlar.
- [Project 3 — Performant Landing](https://github.com/annayev-dev/project-3) — Hız ve SEO odaklı açılış sayfası.

(Not: Bu linkler placeholder — istersen gerçek project repo/demosu ver, ben doğrudan buna göre güncellerim.)

Canlı İstatistikler ve Sosyal

<p align="left">
  <img alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=annayev-dev&show_icons=true&theme=dark&hide_border=true" />
  <img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=annayev-dev&layout=compact&theme=dark&hide_border=true" />
</p>

Sosyal: [LinkedIn](https://www.linkedin.com/in/annayev) • [Twitter](https://twitter.com/annayev) • Email: annayev.dev@gmail.com

Nasıl Özelleştirilir

- İsim veya başlık değiştirmek için README içindeki SVG ve başlık satırlarını düzenle.
- Renk paletini değiştirmek için SVG'deki linearGradient (#g1) renklerini güncelle.
- Proje linklerini güncelle: Öne çıkan projelerin linklerini gerçek repo/demo URL'leri ile değiştir.
- Özel font istersen: bana bir WOFF/WOFF2 dosyası yolla veya "embed font" de; ben base64 gömülü fontu eklerim (README boyutu büyür).

Erişilebilirlik ve performans notları

- SVG içinde title/desc eklendi; ayrıca prefers-reduced-motion destekleniyor.
- GitHub README'lerinde harici JS çalışmaz — etkileşimler SVG SMIL/CSS ile yapıldı.

İstersen hemen:
- Gerçek 3 proje linkini ver, ben kısaltılmış açıklamalarla güncellerim.
- "Embed font" dersen, kullanmak istediğin fontu veya izin verilecekse benim önerimi belirt (Ben Inter veya Rubik öneririm) ve ben base64 ile gömüp README'yi güncellerim.

---

README'yi güncelledim ve repo köküne koydum. Şimdi yapabileceğim şeyler:
1) Placeholder projeleri gerçek linklerle değiştirip canlı demo/snippet eklerim.
2) Eğer istersen fontu base64 olarak gömeyim (bunu uygulamak README boyutunu büyütecek).
3) Renk paletini tam olarak istediğin hex kodlarıyla güncelleyeyim.

Hemen hangi adımı (1–3) veya hepsini beraber mi yapayım? Eğer "tamam hepsini" dersen, gerçek proje linklerini ve tercih ettiğin font/hex paleti paylaş.