<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Noor | Daily Islamic Reminders</title>
  <style>
    :root {
      --primary-green: #0f382c;
      --accent-gold: #d4af37;
      --bg-cream: #faf8f5;
      --card-bg: #ffffff;
      --text-dark: #2c3e50;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--bg-cream);
      color: var(--text-dark);
      text-align: center;
      line-height: 1.6;
    }

    /* Navigation Bar */
    nav {
      background-color: var(--primary-green);
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }

    .logo {
      color: var(--accent-gold);
      font-size: 24px;
      font-weight: bold;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      font-weight: 500;
    }

    .nav-links a:hover {
      color: var(--accent-gold);
    }

    /* Hero Banner */
    header {
      background: linear-gradient(135deg, #0f382c 0%, #1a5e4a 100%);
      padding: 80px 20px;
      color: white;
      border-bottom: 4px solid var(--accent-gold);
    }

    header h1 {
      font-size: 48px;
      margin: 0;
      color: var(--accent-gold);
    }

    header p {
      font-size: 20px;
      margin-top: 10px;
      opacity: 0.9;
    }

    /* Main Container */
    .container {
      max-width: 800px;
      margin: 40px auto;
      padding: 0 20px;
    }

    /* Cards */
    .card {
      background: var(--card-bg);
      padding: 30px;
      margin-bottom: 30px;
      border-radius: 16px;
      border-top: 5px solid var(--accent-gold);
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }

    .card h2 {
      color: var(--primary-green);
      margin-top: 0;
    }

    .arabic-text {
      font-size: 28px;
      color: var(--primary-green);
      margin: 15px 0;
      direction: rtl;
    }

    /* Tasbeeh Counter */
    .tasbeeh-display {
      font-size: 50px;
      font-weight: bold;
      color: var(--primary-green);
      margin: 20px 0;
    }

    .btn {
      padding: 12px 28px;
      font-size: 16px;
      font-weight: bold;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: transform 0.2s, background-color 0.2s;
    }

    .btn-primary {
      background-color: var(--accent-gold);
      color: #0f382c;
    }

    .btn-primary:hover {
      background-color: #c29d2b;
      transform: scale(1.05);
    }

    .btn-secondary {
      background-color: #e0e0e0;
      color: #333;
      margin-left: 10px;
    }

    /* Footer */
    footer {
      background-color: var(--primary-green);
      color: white;
      padding: 20px;
      margin-top: 60px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <nav>
    <div class="logo">🌙 Noor</div>
    <div class="nav-links">
      <a href="#verse">Verse</a>
      <a href="#hadith">Hadith</a>
      <a href="#tasbeeh">Tasbeeh</a>
    </div>
  </nav>

  <header>
    <h1>🌙 Noor</h1>
    <p>Illuminate your day with reminders, Quran, and Dhikr.</p>
  </header>

  <div class="container">

    <section id="verse" class="card">
      <h2>📖 Quran Verse of the Day</h2>
      <div class="arabic-text">فَاذْكُرُونِي أَذْكُرْكُمْ</div>
      <p><em>"So remember Me; I will remember you."</em></p>
      <small><strong>Surah Al-Baqarah (2:152)</strong></small>
    </section>

    <section id="hadith" class="card">
      <h2>✨ Daily Authentic Hadith</h2>
      <p>"The best of people are those who are most beneficial to others."</p>
      <small><strong>— Prophet Muhammad ﷺ (Al-Mu'jam al-Awsat)</strong></small>
    </section>

    <section id="tasbeeh" class="card">
      <h2>📿 Digital Tasbeeh Counter</h2>
      <p>Tap the button to count your Dhikr (e.g., <em>SubhanAllah</em>, <em>Alhamdulillah</em>, <em>Allahu Akbar</em>).</p>
      
      <div class="tasbeeh-display" id="count">0</div>
      
      <button class="btn btn-primary" onclick="countUp()">Count +1</button>
      <button class="btn btn-secondary" onclick="resetCount()">Reset</button>
    </section>

  </div>

  <footer>
    <p>Built with heart | Reliable sources guaranteed 🌙</p>
  </footer>

  <script>
    let counterValue = 0;

    function countUp() {
      counterValue++;
      document.getElementById('count').innerText = counterValue;
    }

    function resetCount() {
      counterValue = 0;
      document.getElementById('count').innerText = counterValue;
    }
  </script>

</body>
</html>
