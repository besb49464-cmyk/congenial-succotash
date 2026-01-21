# congenial-succotash
<!DOCTYPE html>
<html lang="sq">
<head>
  <meta charset="UTF-8">
  <title>School Helper AI</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {margin:0;font-family:Arial;background:#eef2ff;}
    header {background:#1e40af;color:white;padding:20px;text-align:center;}
    nav {background:#1e3a8a;display:flex;flex-wrap:wrap;justify-content:center;gap:15px;padding:10px;}
    nav a {color:white;text-decoration:none;font-weight:bold;}
    nav a:hover {text-decoration:underline;}
    .container {padding:20px;}
    .card {background:white;padding:15px;margin-bottom:15px;border-radius:10px;box-shadow:0 2px 6px rgba(0,0,0,0.15);}    
    h2 {color:#1e40af;}
    button {background:#1e40af;color:white;border:none;padding:8px 14px;border-radius:5px;cursor:pointer;margin-top:5px;}
    button:hover {background:#1e3a8a;}
    input, textarea {width:100%;padding:8px;margin:5px 0;border-radius:5px;border:1px solid #ccc;}
    footer {background:#1e40af;color:white;text-align:center;padding:10px;}
  </style>
</head>
<body>

<header>
  <h1>📘 School Helper AI</h1>
  <p>Mësime • Teste • Inteligjencë Artificiale</p>
</header>

<nav>
  <a href="#mesime">Mësime</a>
  <a href="#teste">Teste</a>
  <a href="#ai">AI Ndihmës</a>
</nav>

<div class="container">

<!-- MESIME -->
<div id="mesime" class="card">
  <h2>📚 Mësime</h2>
  <ul>
    <li>Matematikë – Thyesa, barazime</li>
    <li>Fizikë – Forca, shpejtësia</li>
    <li>Kimi – Reaksione, atomi</li>
    <li>Biologji – Qeliza, organizmi</li>
  </ul>
</div>

<!-- TESTE -->
<div id="teste" class="card">
  <h2>📝 Test i Shpejtë</h2>
  <p>1️⃣ Sa është 8 × 7 ?</p>
  <button onclick="kontrollo(56)">56</button>
  <button onclick="kontrollo(48)">48</button>

  <p>2️⃣ Cili është planeti më i madh?</p>
  <button onclick="kontrollo2('Jupiter')">Jupiter</button>
  <button onclick="kontrollo2('Mars')">Mars</button>

  <p id="rezTest"></p>
</div>

<!-- AI -->
<div id="ai" class="card">
  <h2>🤖 AI Ndihmës</h2>
  <p>Shkruaj pyetjen tënde:</p>
  <textarea id="pyetje"></textarea>
  <button onclick="aiPergjigje()">Pyet AI</button>
  <p id="aiRez"></p>
</div>

</div>

<footer>
  <p>© 2026 School Helper AI | Projekt Shkollor</p>
</footer>

<script>
  function kontrollo(v){
    if(v === 56)
      document.getElementById('rezTest').innerText = 'Saktë ✅';
    else
      document.getElementById('rezTest').innerText = 'Gabim ❌';
  }

  function kontrollo2(p){
    if(p === 'Jupiter')
      document.getElementById('rezTest').innerText = 'Saktë ✅';
    else
      document.getElementById('rezTest').innerText = 'Gabim ❌';
  }

  function aiPergjigje(){
    let p = document.getElementById('pyetje').value;
    if(p.length < 3)
      document.getElementById('aiRez').innerText = 'Shkruaj një pyetje të plotë.';
    else
      document.getElementById('aiRez').innerText = 'AI: Ky është një simulim. Për version real lidhet me ChatGPT API.';
  }
</script>

</body>
</html>


