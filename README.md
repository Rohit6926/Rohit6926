<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Diwali</title>
<style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #1a1a1a;
      color: #ffcc00;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .container {
      text-align: center;
      position: relative;
    }

    .diwali-message {
      font-size: 3em;
      font-weight: bold;
      margin-bottom: 20px;
    }

    .diya {
      font-size: 3em;
      color: #ff6600;
      animation: flicker 0.1s infinite alternate;
    }

    @keyframes flicker {
      0% { opacity: 1; transform: scale(1); }
      100% { opacity: 0.8; transform: scale(1.05); }
    }

    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: #ffcc00;
      border-radius: 50%;
      animation: fall linear infinite;
      opacity: 0;
    }

    @keyframes fall {
      0% { transform: translateY(-100vh) rotate(0); opacity: 1; }
      100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
    }
</style>
</head>
<body>

<div class="container">
<div class="diwali-message">✨ Happy Diwali ✨</div>
<div class="diya">🪔</div>
</div>

<script>
    // Generate falling confetti
    function createConfetti() {
const confetti = document.createElement("div");
confetti.classList.add("confetti");
confetti.style.left = Math.random() * 100 + "vw";
confetti.style.animationDuration = Math.random() * 3 + 2 + "s";
confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
document.body.appendChild(confetti);

setTimeout(() => {
confetti.remove();
      }, 5000);
    }

setInterval(createConfetti, 100); // Create new confetti every 100ms
</script>

</body>
</html>
