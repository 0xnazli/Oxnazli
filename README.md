# Oxnazli

---

<!-- space.svg -->
<svg viewBox="0 0 600 600" xmlns="http://www.w3.org/2000/svg">
  <!-- Arkaplan -->
  <rect width="600" height="600" fill="#0b1020"/>

  <!-- Yıldızlar -->
  <g id="stars">
    <circle cx="60" cy="80" r="1.5" fill="#fff">
      <animate attributeName="opacity" values="0.2;1;0.2" dur="2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="540" cy="120" r="1.2" fill="#fff">
      <animate attributeName="opacity" values="0.2;1;0.2" dur="2.4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="120" cy="520" r="1.3" fill="#fff">
      <animate attributeName="opacity" values="0.2;1;0.2" dur="1.8s" repeatCount="indefinite"/>
    </circle>
    <circle cx="420" cy="460" r="1.4" fill="#fff">
      <animate attributeName="opacity" values="0.2;1;0.2" dur="2.2s" repeatCount="indefinite"/>
    </circle>
    <circle cx="300" cy="50" r="1.2" fill="#fff">
      <animate attributeName="opacity" values="0.2;1;0.2" dur="2.6s" repeatCount="indefinite"/>
    </circle>
  </g>

  <!-- Güneş -->
  <defs>
    <radialGradient id="sunG" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#ffe08a"/>
      <stop offset="60%" stop-color="#ffb347"/>
      <stop offset="100%" stop-color="#ff9030"/>
    </radialGradient>
  </defs>
  <circle cx="300" cy="300" r="40" fill="url(#sunG)"/>
  <!-- Güneş parıltısı -->
  <circle cx="300" cy="300" r="70" fill="#ffb347" opacity="0.15">
    <animate attributeName="r" values="60;80;60" dur="4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.1;0.25;0.1" dur="4s" repeatCount="indefinite"/>
  </circle>

  <!-- Birinci yörünge -->
  <circle cx="300" cy="300" r="110" fill="none" stroke="#2a3556" stroke-dasharray="4 6"/>
  <g>
    <g transform="translate(300,300)">
      <g>
        <circle cx="110" cy="0" r="10" fill="#50c2ff"/>
      </g>
      <animateTransform attributeName="transform" attributeType="XML"
        type="rotate" from="0" to="360" dur="10s" repeatCount="indefinite"/>
    </g>
  </g>

  <!-- İkinci yörünge -->
  <circle cx="300" cy="300" r="170" fill="none" stroke="#263051" stroke-dasharray="4 6"/>
  <g>
    <g transform="translate(300,300)">
      <g>
        <circle cx="170" cy="0" r="14" fill="#a2ff9d"/>
        <circle cx="170" cy="0" r="20" fill="none" stroke="#a2ff9d" opacity="0.25"/>
      </g>
      <animateTransform attributeName="transform" attributeType="XML"
        type="rotate" from="360" to="0" dur="18s" repeatCount="indefinite"/>
    </g>
  </g>

  <!-- Roket yolu -->
  <path id="orbitPath" d="M 300 130
                          C 470 160, 520 360, 300 470
                          C 120 420, 90 230, 300 130 Z"
        fill="none" stroke="#33406a" stroke-dasharray="5 7"/>

  <!-- Roket -->
  <g id="rocket">
    <g>
      <!-- gövde -->
      <polygon points="0,-10 28,0 0,10 5,0" fill="#e6e6e6" stroke="#9aa3b2"/>
      <!-- pencere -->
      <circle cx="10" cy="0" r="3.5" fill="#6bd3ff" stroke="#3a7ea1"/>
      <!-- alev -->
      <polygon points="-6,-4 0,0 -6,4" fill="#ffb347">
        <animate attributeName="points"
          values="-6,-4 0,0 -6,4; -8,-2 0,0 -8,2; -6,-4 0,0 -6,4"
          dur="0.25s" repeatCount="indefinite"/>
      </polygon>
    </g>
    <animateMotion dur="14s" repeatCount="indefinite" rotate="auto">
      <mpath xlink:href="#orbitPath"/>
    </animateMotion>
  </g>
</svg>
