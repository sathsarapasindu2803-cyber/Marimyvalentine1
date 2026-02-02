# Marimyvalentine1
Oalal
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>
  <style>
    body {
      height: 100vh;
      margin: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 35px;
      border-radius: 18px;
      text-align: center;
      box-shadow: 0 15px 30px rgba(0,0,0,0.25);
      z-index: 2;
    }

    h1 {
      margin-bottom: 25px;
    }

    button {
      padding: 14px 24px;
      font-size: 17px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      margin: 10px;
    }

    #yes {
      background: #ff4d6d;
      color: white;
      box-shadow: 0 6px 15px rgba(255,77,109,0.6);
    }

    #no {
      background: #ccc;
      position: absolute;
    }

    /* Floating hearts */
    .heart {
      position: absolute;
      font-size: 20px;
      animation: float 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) scale(1);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.5);
        opacity: 0;
      }
    }

    /* GLOWING NAME */
    .glow {
      color: #fff;
      font-weight: bold;
      animation: glow 1.5s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow:
          0 0 5px #ff4d6d,
          0 0 10px #ff4d6d,
          0 0 20px #ff85a1;
      }
      to {
        text-shadow:
          0 0 10px #ff85a1,
          0 0 20px #ff85a1,
          0 0 40px #ffc2d1;
      }
    }
  </style>
</head>
<body>

  <!-- Music (hidden YouTube embed) -->
  <iframe
    width="0"
    height="0"
    src="https://www.youtube.com/embed/kyK1D6e0WzM?autoplay=1&loop=1&playlist=kyK1D6e0WzM"
    frameborder="0"
    allow="autoplay">
  </iframe>

  <div class="card">
    <h1>Will u be my valentine my precious girl 💖</h1>
    <button id="yes" onclick="yesClicked()">Yes 💕</button>
    <button id="no" onmouseover="moveNo()">No 😢</button>
  </div>

  <script>
    function moveNo() {
      const noBtn = document.getElementById("no");
      const x = Math.random() * (window.innerWidth - 120);
      const y = Math.random() * (window.innerHeight - 60);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClicked() {
      document.body.innerHTML = `
        <div style="text-align:center; color:white; padding:40px;">
          <h1>
            Thank u soo muchh 
            <span class="glow">marii</span> 💘
          </h1>
          <p style="font-size:22px; line-height:1.6;">
            u mean the world to me 💖<br>
            u made me the happiest person ever<br>
            n even more happy by being my valentine 💕
          </p>
        </div>
      `;
      createHearts();
    }

    function createHearts() {
      setInterval(() => {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (Math.random() * 20 + 15) + "px";
        document.body.appendChild(heart);

        setTimeout(() => heart.remove(), 6000);
      }, 300);
    }
  </script>

</body>
</html>
