<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sistema Bilingüe de Panificación</title>
  <style>
    :root {
      --main-bg: #f0f4f8;
      --section-bg: #ffffff;
      --text-color: #222;
      --accent-color: #4CAF50;
      --token-bg: #e0e0e0;
    }

    @media (prefers-color-scheme: dark) {
      :root {
        --main-bg: #121212;
        --section-bg: #1e1e1e;
        --text-color: #eee;
        --accent-color: #81c784;
        --token-bg: #333;
      }
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--main-bg);
      color: var(--text-color);
      padding: 20px;
      transition: background 0.3s, color 0.3s;
    }

    h1 {
      text-align: center;
      font-size: 2em;
      margin-bottom: 20px;
    }

    .section {
      background-color: var(--section-bg);
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      margin-bottom: 30px;
      transition: background 0.3s;
    }

    h2 {
      font-size: 1.5em;
      border-bottom: 2px solid var(--accent-color);
      padding-bottom: 8px;
      margin-bottom: 20px;
    }

    .item {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      margin: 10px 0;
      border-bottom: 1px dashed #ccc;
      padding-bottom: 10px;
    }

    .language {
      flex: 1 1 40%;
      font-weight: bold;
      font-size: 1.1em;
    }

    .controls {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 10px;
    }

    .token {
      background-color: var(--token-bg);
      padding: 6px 12px;
      border-radius: 6px;
      font-family: monospace;
      font-size: 0.9em;
    }

    .audio-btn {
      background-color: var(--accent-color);
      color: #fff;
      border: none;
      border-radius: 50px;
      width: 45px;
      height: 45px;
      font-weight: bold;
      font-size: 0.9em;
      cursor: pointer;
      transition: background 0.3s;
    }

    .audio-btn:hover {
      background-color: #388e3c;
    }

    @media (max-width: 600px) {
      .language {
        flex: 1 1 100%;
        margin-bottom: 8px;
      }
    }

    footer {
      margin-top: 40px;
      text-align: center;
      font-size: 0.9em;
      color: #888;
    }
  </style>
</head>
<body>

  <h1>Sistema Bilingüe de Panificación</h1>

  <div class="section">
    <h2>Elementos de Panificación / Bakery Elements</h2>

    <div class="item">
      <div class="language">BALANZA DIGITAL</div>
      <div class="language">DIGITAL SCALE</div>
      <div class="controls">
        <span class="token">BAL001</span>
        <button class="audio-btn" onclick="speak('BALANZA DIGITAL', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('DIGITAL SCALE', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">AMASADORA</div>
      <div class="language">KNEADER</div>
      <div class="controls">
        <span class="token">AMA002</span>
        <button class="audio-btn" onclick="speak('AMASADORA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('KNEADER', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">BATIDORA</div>
      <div class="language">BLENDER / MIX</div>
      <div class="controls">
        <span class="token">BAT003</span>
        <button class="audio-btn" onclick="speak('BATIDORA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('BLENDER', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">TERMOSELLADORA</div>
      <div class="language">HEAT SEALER</div>
      <div class="controls">
        <span class="token">TER004</span>
        <button class="audio-btn" onclick="speak('TERMOSELLADORA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('HEAT SEALER', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">HORNO PIZZERO</div>
      <div class="language">PIZZA OVEN</div>
      <div class="controls">
        <span class="token">HOR005</span>
        <button class="audio-btn" onclick="speak('HORNO PIZZERO', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('PIZZA OVEN', 'en')">EN</button>
      </div>
    </div>
  </div>

  <div class="section">
    <h2>Vestimenta / Clothing</h2>

    <div class="item">
      <div class="language">COFIA</div>
      <div class="language">CAP</div>
      <div class="controls">
        <span class="token">COF006</span>
        <button class="audio-btn" onclick="speak('COFIA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('CAP', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">DELANTAL DE COCINA</div>
      <div class="language">KITCHEN APRON</div>
      <div class="controls">
        <span class="token">DEL007</span>
        <button class="audio-btn" onclick="speak('DELANTAL DE COCINA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('KITCHEN APRON', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">GUANTES DE COCINA</div>
      <div class="language">KITCHEN GLOVES</div>
      <div class="controls">
        <span class="token">GUA008</span>
        <button class="audio-btn" onclick="speak('GUANTES DE COCINA', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('KITCHEN GLOVES', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">GUANTES DE LATEX</div>
      <div class="language">LATEX GLOVES</div>
      <div class="controls">
        <span class="token">GUL009</span>
        <button class="audio-btn" onclick="speak('GUANTES DE LATEX', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('LATEX GLOVES', 'en')">EN</button>
      </div>
    </div>

    <div class="item">
      <div class="language">BARBIJO</div>
      <div class="language">HEADSCARF</div>
      <div class="controls">
        <span class="token">BAR010</span>
        <button class="audio-btn" onclick="speak('BARBIJO', 'es')">ES</button>
        <button class="audio-btn" onclick="speak('HEADSCARF', 'en')">EN</button>
      </div>
    </div>
  </div>

  <footer>
    © 2025 Sistema Bilingüe de Panificación — Todos los derechos reservados.
  </footer>

  <script>
    function speak(text, lang) {
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = lang === 'es' ? 'es-ES' : 'en-US';
      window.speechSynthesis.speak(utterance);
    }
  </script>
</body>
</html>
