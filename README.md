# mindease
“MindEase: A calming, interactive website for students and Gen-Z to explore coping tips, self-care exercises, and mental health resources.”
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MindEase 🌸</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav>
    <h1>MindEase 🌿</h1>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#facts">Know the Facts</a></li>
      <li><a href="#tips">Coping Tips</a></li>
      <li><a href="#selfcare">Self-Care Space</a></li>
      <li><a href="#helplines">Helplines</a></li>
    </ul>
  </nav>

  <section id="home" class="section">
    <h2>Hey there 👋</h2>
    <p>Life can get heavy sometimes. This space is for you — to breathe, learn, and heal.</p>
    <button onclick="scrollToSection('selfcare')">Take a Deep Breath 🌬️</button>
  </section>

  <section id="facts" class="section">
    <h2>🧠 Know the Facts</h2>
    <p>Stress and anxiety are normal reactions — they don’t mean you’re weak. 
       But when they feel too heavy, reaching out helps more than you think.</p>
  </section>

  <section id="tips" class="section">
    <h2>💡 Coping Tips</h2>
    <ul>
      <li>🎧 Listen to music you love</li>
      <li>📝 Write down your thoughts</li>
      <li>☀️ Go outside for 10 mins</li>
      <li>📞 Talk to someone you trust</li>
      <li>💤 Get enough sleep</li>
    </ul>
  </section>

  <section id="selfcare" class="section">
    <h2>🕊️ Self-Care Space</h2>
    <p>Try a mini breathing exercise below 👇</p>
    <div class="breathing-circle" id="breathingCircle"></div>
    <p id="breathingText">Breathe In</p>
  </section>

  <section id="helplines" class="section">
    <h2>☎️ Helplines</h2>
    <p>If you’re struggling, you don’t have to face it alone 💬</p>
    <ul>
      <li><b>AASRA (India):</b> 91-9820466726</li>
      <li><b>Vandrevala Foundation:</b> 1860 266 2345</li>
      <li><b>Samaritans (UK):</b> 116 123</li>
      <li><b>988 Suicide & Crisis Lifeline (US):</b> 988</li>
    </ul>
  </section>

  <footer>
    <p>Made with 💜 by Anshika for Gen-Z minds 🌈</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: linear-gradient(180deg, #dbeafe, #fce7f3);
  color: #333;
  text-align: center;
  scroll-behavior: smooth;
}

nav {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(10px);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  position: sticky;
  top: 0;
  border-bottom: 1px solid #e5e7eb;
}

nav h1 {
  font-weight: 600;
  color: #5b21b6;
}

nav ul {
  display: flex;
  gap: 15px;
  list-style: none;
}

nav a {
  text-decoration: none;
  color: #374151;
  font-weight: 500;
}

nav a:hover {
  color: #5b21b6;
}

.section {
  padding: 60px 20px;
  max-width: 700px;
  margin: auto;
}

button {
  background: #a5b4fc;
  border: none;
  padding: 10px 20px;
  border-radius: 25px;
  color: white;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #818cf8;
}

.breathing-circle {
  width: 120px;
  height: 120px;
  margin: 30px auto;
  background: #c7d2fe;
  border-radius: 50%;
  animation: breathe 8s ease-in-out infinite;
}

@keyframes breathe {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.5); }
}

footer {
  padding: 20px;
  font-size: 14px;
  background: #f3e8ff;
  margin-top: 30px;
  color: #4b5563;
  border-top: 1px solid #e5e7eb;
}
function scrollToSection(id) {
  document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
}

// Simple breathing text changer
const text = document.getElementById("breathingText");
let stage = 0;
setInterval(() => {
  const phrases = ["Breathe In 🌿", "Hold...", "Breathe Out 💨"];
  text.textContent = phrases[stage];
  stage = (stage + 1) % phrases.length;
}, 3000);

