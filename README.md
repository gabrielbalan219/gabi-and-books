<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Cărțile lui Gabi</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    header {
      background: #222;
      color: #fff;
      padding: 1em;
      text-align: center;
    }
    .tricolor-title span {
      font-weight: bold;
      font-size: 2em;
      padding: 0 0.2em;
    }
    .albastru { color: #0057b7; }
    .galben { color: #ffd700; }
    .rosu { color: #dc143c; }

    nav {
      background: #444;
      display: flex;
      justify-content: center;
    }
    nav a {
      color: white;
      padding: 1em;
      text-decoration: none;
      transition: background 0.3s;
    }
    nav a:hover {
      background: #666;
    }
    section {
      padding: 2em;
      display: none;
    }
    section.active {
      display: block;
    }
    .story {
      background: white;
      margin-bottom: 1em;
      padding: 1em;
      border-radius: 5px;
    }
  </style>
</head>
<body>

<header>
  <div class="tricolor-title">
    <span class="albastru">Cărțile</span>
    <span class="galben">lui</span>
    <span class="rosu">Gabi</span>
  </div>
  <p>Alege un gen pentru a începe lectura!</p>
</header>

<nav>
  <a href="#" onclick="showSection('horror')">Horror</a>
  <a href="#" onclick="showSection('aventura')">Aventură</a>
  <a href="#" onclick="showSection('actiune')">Acțiune</a>
  <a href="#" onclick="showSection('sf')">SF</a>
</nav>

<section id="horror" class="active">
  <h2>Povești Horror</h2>
  <div class="story">
    <h3>Titlu poveste horror</h3>
    <p>Aici scrii povestea ta de groază...</p>
  </div>
</section>

<section id="aventura">
  <h2>Povești de Aventură</h2>
  <div class="story">
    <h3>Titlu poveste aventură</h3>
    <p>Aici scrii povestea ta de aventură...</p>
  </div>
</section>

<section id="actiune">
  <h2>Povești de Acțiune</h2>
  <div class="story">
    <h3>Titlu poveste acțiune</h3>
    <p>Aici scrii povestea ta de acțiune...</p>
  </div>
</section>

<section id="sf">
  <h2>Povești SF</h2>
  <div class="story">
    <h3>Titlu poveste SF</h3>
    <p>Aici scrii povestea ta science-fiction...</p>
  </div>
</section>

<script>
  function showSection(id) {
    const sections = document.querySelectorAll('section');
    sections.forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
  }
</script>

</body>
</html>
