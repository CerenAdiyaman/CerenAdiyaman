<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    body, html {
      margin: 0; padding: 0;
      width: 100%; height: 100%;
      background: #1e3a5f; /* derin deniz rengi */
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }
    .ocean {
      position: relative;
      width: 100%; height: 100%;
    }
    .island {
      position: absolute;
      width: 180px; height: 100px;
      background: #f4d35e; /* kum rengi */
      border-radius: 50% 50% 40% 40%;
      box-shadow: 0 10px 15px rgba(0,0,0,0.3);
      display: flex;
      justify-content: center;
      align-items: center;
      color: #333;
      font-weight: bold;
      text-align: center;
      padding: 0.5rem;
      animation: bob 4s ease-in-out infinite;
    }
    /* Adaların konumlarını ayarlıyoruz */
    .island-code      { top: 40%; left: 45%; width: 220px; height: 120px; background: #e76f51; color: #fff; }
    .island-creativity{ top: 20%; left: 15%; }
    .island-logic     { top: 60%; left: 20%; }
    .island-innovation{ top: 30%; left: 75%; }

    /* Hafif dalgalanma (bob) animasyonu */
    @keyframes bob {
      0%,100%   { transform: translateY(0); }
      50%       { transform: translateY(-8px); }
    }
    /* Deniz yüzeyi hafif parıltı */
    .ocean::before {
      content: '';
      position: absolute;
      top: -20%; left: -20%;
      width: 140%; height: 140%;
      background: radial-gradient(circle at 50% 50%, rgba(255,255,255,0.05), transparent 70%);
      animation: ripple 6s linear infinite;
    }
    @keyframes ripple {
      0%   { transform: scale(0.8); opacity: 0.8; }
      100% { transform: scale(1.2); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="ocean">
    <div class="island island-code">Cego’s Code Island</div>
    <div class="island island-creativity">Creativity Island</div>
    <div class="island island-logic">Logic Island</div>
    <div class="island island-innovation">Innovation Island</div>
  </div>
</body>
</html>
