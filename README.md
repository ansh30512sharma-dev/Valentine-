<!DOCTYPE html>
<html>
<head>
  <title>For Vaibhavi 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: url("bg.jpg") no-repeat center center/cover;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .overlay {
      background: rgba(0,0,0,0.6);
      width: 100%;
      height: 100%;
      position: absolute;
      text-align: center;
      color: white;
    }

    h1 {
      margin-top: 80px;
      color: pink;
      font-size: 40px;
    }

    button {
      padding: 15px 30px;
      font-size: 22px;
      border-radius: 12px;
      border: none;
      cursor: pointer;
      position: absolute;
    }

    #yesBtn {
      background-color: #ff4d6d;
      color: white;
      left: 35%;
      top: 300px;
    }

    #noBtn {
      background-color: white;
      color: red;
      left: 55%;
      top: 300px;
    }

    #result {
      margin-top: 180px;
      font-size: 28px;
      color: #ffb6c1;
    }

    .heart, .rose {
      position: absolute;
      font-size: 24px;
      animation: floatUp 5s linear infinite;
    }

    @keyframes floatUp {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-900px); opacity: 0; }
    }

    .firework {
      position: absolute;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      animation: explode 1s ease-out forwards;
    }

    @keyframes explode {
      from { transform: scale(1); opacity: 1; }
      to { transform: scale(5); opacity: 0; }
    }
  </style>
</head>
<body>

<audio autoplay loop>
  <source src="ishq.mp3" type="audio/mpeg">
</audio>

<div class="overlay">
  <h1>Vaibhavi 💖 Will you be my Valentine?</h1>

  <button id="yesBtn" onclick="yesClick()">YES</button>
  <button id="noBtn" onmouseover="moveNo()">NO</button>

  <div id="result"></div>
</div>

<script>
  function yesClick() {
    document.getElementById("result").innerHTML =
      "Yayyy Vaibhavi 💕 You made my day! 🌹💖";
    setInterval(createFirework, 300);
  }

  function moveNo() {
    let x = Math.random() * (window.innerWidth - 100);
    let y = Math.random() * (window.innerHeight - 100);
    document.getElementById("noBtn").style.left = x + "px";
    document.getElementById("noBtn").style.top = y + "px";
  }

  function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * window.innerWidth + "px";
    heart.style.top = window.innerHeight + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
  }

  function createRose() {
    const rose = document.createElement("div");
    rose.classList.add("rose");
    rose.innerHTML = "🌹";
    rose.style.left = Math.random() * window.innerWidth + "px";
    rose.style.top = window.innerHeight + "px";
    document.body.appendChild(rose);
    setTimeout(() => rose.remove(), 5000);
  }

  function createFirework() {
    const firework = document.createElement("div");
    firework.classList.add("firework");
    firework.style.left = Math.random() * window.innerWidth + "px";
    firework.style.top = Math.random() * window.innerHeight + "px";
    firework.style.background =
      `hsl(${Math.random()*360},100%,60%)`;
    document.body.appendChild(firework);
    setTimeout(() => firework.remove(), 1000);
  }

  setInterval(createHeart, 300);
  setInterval(createRose, 600);
</script>

</body>
</html>
her
bg.jpg 

