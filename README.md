<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Your Name | Portfolio</title>

  <style>
    /* === COLOR VARIABLES === */
    :root {
      --bg-color: #f2f6f9;
      --text-color: #333;
      --primary-color: #0077cc;
      --accent-color: #ffaa00;
      --card-color: #ffffff;
      --nav-bg: #ffffff;
      --nav-text: #0077cc;
    }

    /* === GLOBAL STYLES === */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: var(--bg-color);
      color: var(--text-color);
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: var(--nav-text);
      font-weight: 500;
    }

    h1, h2, h3 {
      margin-bottom: 10px;
    }

    section {
      padding: 160px 20px;
      max-width: 1000px;
      margin: auto;
    }

    /* === NAVBAR === */
    nav {
      background: var(--nav-bg);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 20px;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .logo {
      font-size: 1.4rem;
      font-weight: bold;
      color: var(--primary-color);
    }

    .nav-links {
      display: flex;
      gap: 20px;
    }

    .menu-toggle {
      display: none;
      font-size: 1.8rem;
      cursor: pointer;
      color: var(--primary-color);
    }

    /* === HERO SECTION === */
    header {
      text-align: center;
      padding: 160px 20px;
    }

    header h1 {
      font-size: 2.5rem;
      color: var(--primary-color);
    }

    header p {
      font-size: 1.1rem;
      color: var(--accent-color);
    }

    /* === CARDS (PROJECTS & SKILLS) === */
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .card {
      background: var(--card-color);
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
      transition: transform 0.3s;
    }

    .card:hover {
      transform: scale(1.03);
    }

    /* === CONTACT FORM === */
    form input, form textarea, form button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-family: inherit;
    }

    form button {
      background: var(--primary-color);
      color: white;
      font-weight: bold;
      border: none;
      cursor: pointer;
    }

    /* === FOOTER === */
    footer {
      text-align: center;
      background: #e0e0e0;
      padding: 20px;
      font-size: 0.9rem;
      color: #555;
    }

    /* === MOBILE RESPONSIVE === */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 60px;
        right: 20px;
        background: white;
        padding: 15px;
        border-radius: 8px;
        box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      }

      .nav-links.show {
        display: flex;
      }

      .menu-toggle {
        display: block;
      }
    }
  </style>
</head>

<body>

  <!-- === NAVIGATION === -->
  <nav>
    <div class="logo">Portfolio</div>
    <div class="menu-toggle" onclick="toggleMenu()">&#9776;</div>
    <div class="nav-links" id="navLinks">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- === HERO === -->
  <header>
  <section id="home">
    <h1>Hello, I'm Kolusu Geetha Madhuri</h1>
    <p>Aspiring Data Analyst & Developer</p>
  </section>
  </header>

  <!-- === ABOUT === -->
  <section id="about">
    <h2>About Me</h2>
    <p>
      I am passionate about analyzing data to uncover insights and building interactive websites. 
      With a solid foundation in data analytics tools and frontend technologies, I aim to bridge the gap between data and design.
    </p>
  </section>

  <!-- === SKILLS === -->
  <section id="skills">
    <h2>Skills</h2>
    <div class="card-grid">
      <div class="card">Python for Data Analysis</div>
      <div class="card">Excel & Power BI</div>
      <div class="card">HTML, CSS, JavaScript</div>
      <div class="card">SQL & Databases</div>
    </div>
  </section>

  <!-- === PROJECTS === -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="card-grid">
      <div class="card">
        <h3>Responsive Portfolio</h3>
        <p>Designed and developed this portfolio using HTML, CSS, and JavaScript.</p>
      </div>
      <div class="card">
        <h3>Weather App</h3>
        <p>Real-time weather updates using API integration.</p>
      </div>
      <div class="card">
        <h3>To-Do List</h3>
        <p>A simple, dynamic to-do list to manage daily tasks.</p>
      </div>
    </div>
  </section>

  <!-- === CONTACT === -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form onsubmit="submitForm(event)">
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="4" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
  </section>

  <!-- === FOOTER === -->
  <footer>
    &copy; 2025 Kolusu Geetha Madhuri | Aspiring Data Analyst & Developer
  </footer>

  <!-- === SCRIPT === -->
  <script>
    function toggleMenu() {
      const navLinks = document.getElementById('navLinks');
      navLinks.classList.toggle('show');
    }

    function submitForm(e) {
      e.preventDefault();
      alert("Thanks! I'll get back to you shortly.");
    }
  </script>

</body>
</html>
