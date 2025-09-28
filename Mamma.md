<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Love</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #87CEFA, #1E90FF);
      overflow: hidden;
      text-align: center;
      color: white;
    }
    h1 {
      font-size: 3em;
      margin-top: 50px;
      text-shadow: 2px 2px 5px #000;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      0% { text-shadow: 2px 2px 10px #fff; }
      100% { text-shadow: 2px 2px 20px #FFD700; }
    }
    .photo-container {
      margin: 50px auto;
      width: 300px;
      height: 300px;
      border-radius: 50%;
      overflow: hidden;
      border: 5px solid #fff;
      box-shadow: 0 0 20px #FFD700;
      background: #fff url('placeholder.jpg') center/cover no-repeat;
    }
    .message {
      font-size: 1.5em;
      margin: 20px;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }
    .surprise-btn {
      margin-top: 30px;
      padding: 15px 30px;
      font-size: 1.2em;
      background-color: #FFD700;
      color: #1E90FF;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .surprise-btn:hover {
      transform: scale(1.1);
    }
    .hidden-message {
      display: none;
      font-size: 1.3em;
      margin-top: 20px;
      animation: fadeIn 2s forwards;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 5s linear infinite;
    }
    .heart::before, .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }
    .heart::before { top: -10px; left: 0; }
    .heart::after { left: 10px; top: 0; }
    @keyframes float {
      0% { transform: translateY(100vh) rotate(45deg); }
      100% { transform: translateY(-10vh) rotate(45deg); }
    }
  </style>
</head>
<body>

  <h1>Happy Birthday My Love 💖</h1>
  
  <div class="photo-container"></div>
  
  <p class="message">You are my sunshine, my happiness, and the reason I smile every day. 💌</p>
  
  <button class="surprise-btn" onclick="showSurprise()">Click to See Why I Love You ❤️</button>
  <p class="hidden-message" id="surpriseText">You are my everything, my heart, and my forever. 🌹 Happy Birthday!</p>
  
  <div class="hearts" id="heartsContainer"></div>
  
  <!-- YouTube background music -->
  <iframe id="ytplayer" type="text/html" width="0" height="0"
    src="https://www.youtube.com/embed/UNPZxw0iENg?autoplay=1&loop=1&playlist=UNPZxw0iENg&controls=0&mute=0"
    frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

  <script>
    function showSurprise() {
      document.getElementById('surpriseText').style.display = 'block';
    }

    // Generate floating hearts
    const heartsContainer = document.getElementById('heartsContainer');
    setInterval(() => {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (3 + Math.random() * 3) + 's';
      heartsContainer.appendChild(heart);
      setTimeout(() => { heartsContainer.removeChild(heart); }, 5000);
    }, 500);
  </script>
</body>
</html>
