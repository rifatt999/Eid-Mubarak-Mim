# Eid-Mubarak-Mim
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<title>Eid Salami Magic</title>
<style>
body {
  margin: 0;
  padding: 0;
  background: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  font-family: 'Segoe UI', sans-serif;
}

.button {
  padding: 20px 40px;
  font-size: 24px;
  border: none;
  border-radius: 12px;
  background: linear-gradient(45deg, #FFD700, #FF8C00, #FF69B4);
  cursor: pointer;
  box-shadow: 0 0 25px #FFD700;
  transition: 0.3s;
  color: #fff;
  font-weight: bold;
}
.button:hover {
  transform: scale(1.1);
  box-shadow: 0 0 50px #FF69B4;
}

#message {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 32px;
  text-align: center;
  display: none;
  font-weight: bold;
  background: linear-gradient(90deg, #FFD700, #FF69B4, #00FFFF, #ADFF2F);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.sparkle, .confetti {
  position: absolute;
  pointer-events: none;
}

.sparkle {
  color: #fff;
  font-size: 20px;
  animation: float 3s linear infinite;
}

.confetti {
  font-size: 16px;
  animation: confetti-fall 4s linear forwards;
}

@keyframes float {
  0% { transform: translateY(0) rotate(0deg); opacity: 1; }
  100% { transform: translateY(-600px) rotate(360deg); opacity: 0; }
}

@keyframes confetti-fall {
  0% { transform: translateY(-20px) rotate(0deg); opacity:1; }
  100% { transform: translateY(600px) rotate(720deg); opacity:0; }
}
</style>
</head>
<body>

<button class="button" onclick="showMessage()">Mim Apu ke Salami Deu ✨</button>
<div id="message">Eid Mubarak, Senior Mim! 🌙💖  
তোমার salami-er জন্য অনেক ধন্যবাদ 😘</div>

<script>
function showMessage() {
  const msg = document.getElementById('message');
  msg.style.display = 'block';
  
  // Sparkles
  for(let i=0;i<40;i++){
    const sparkle = document.createElement('div');
    sparkle.classList.add('sparkle');
    sparkle.innerText = Math.random() > 0.5 ? '🌟' : '❤️';
    sparkle.style.left = Math.random()*100 + 'vw';
    sparkle.style.top = Math.random()*100 + 'vh';
    sparkle.style.fontSize = (10+Math.random()*25)+'px';
    sparkle.style.animationDuration = (2+Math.random()*3)+'s';
    document.body.appendChild(sparkle);
    setTimeout(()=> sparkle.remove(), 4000);
  }
  
  // Confetti
  const confettiColors = ['🎉','✨','💖','🌈','💫'];
  for(let i=0;i<50;i++){
    const confetti = document.createElement('div');
    confetti.classList.add('confetti');
    confetti.innerText = confettiColors[Math.floor(Math.random()*confettiColors.length)];
    confetti.style.left = Math.random()*100 + 'vw';
    confetti.style.top = '-50px';
    confetti.style.fontSize = (12+Math.random()*18)+'px';
    confetti.style.animationDuration = (3+Math.random()*2)+'s';
    document.body.appendChild(confetti);
    setTimeout(()=> confetti.remove(), 4000);
  }
}
</script>

</body>
</html>
