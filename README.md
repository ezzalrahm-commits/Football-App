<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Football App</title>
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<link rel="icon" href="https://upload.wikimedia.org/wikipedia/commons/7/7a/FIFA_Logo.svg">
<style>
  body { font-family: 'Arial', sans-serif; margin:0; padding:0; background:#f4f4f4; }
  header { background:#1e3a8a; color:white; text-align:center; padding:1rem; }
  header h1 { margin:0; font-size:2rem; }
  header p { margin:0.2rem 0 0 0; font-size:1rem; }
  main { padding:1rem; }
  h2 { margin-top:1rem; color:#1e3a8a; }
  .teams, .matches { display:flex; flex-wrap:wrap; gap:0.5rem; margin-top:0.5rem; }
  .team, .match { background:white; border-radius:8px; padding:0.5rem; flex:1 1 45%; display:flex; align-items:center; box-shadow:0 2px 5px rgba(0,0,0,0.1); }
  .team img { width:40px; height:40px; margin-right:0.5rem; }
  .match span { flex:1; text-align:center; }
  .match .score { font-weight:bold; color:#1e3a8a; }
</style>
</head>
<body>

<header>
  <h1>Football App</h1>
  <p id="season"></p>
</header>

<main>
  <h2>Teams</h2>
  <div class="teams">
    <div class="team"><img src="https://upload.wikimedia.org/wikipedia/en/7/7a/Manchester_United_FC_crest.svg" alt="ManU">Manchester United</div>
    <div class="team"><img src="https://upload.wikimedia.org/wikipedia/en/0/0c/Liverpool_FC.svg" alt="Liverpool">Liverpool</div>
    <div class="team"><img src="https://upload.wikimedia.org/wikipedia/en/5/56/Real_Madrid_CF.svg" alt="RM">Real Madrid</div>
    <div class="team"><img src="https://upload.wikimedia.org/wikipedia/en/4/47/FC_Barcelona_%28crest%29.svg" alt="Barca">Barcelona</div>
    <div class="team"><img src="https://upload.wikimedia.org/wikipedia/en/2/2d/Juventus_Turin.svg" alt="Juventus">Juventus</div>
  </div>

  <h2>Upcoming Matches</h2>
  <div class="matches">
    <div class="match"><span>Manchester United</span><span class="score">vs</span><span>Liverpool</span><span>12 Mar 2026</span></div>
    <div class="match"><span>Real Madrid</span><span class="score">vs</span><span>Barcelona</span><span>14 Mar 2026</span></div>
    <div class="match"><span>Juventus</span><span class="score">vs</span><span>Liverpool</span><span>16 Mar 2026</span></div>
  </div>
</main>

<script>
// Automatically set current season
const today = new Date();
const year = today.getFullYear();
const month = today.getMonth() + 1;
const season = month >= 7 ? `${year}/${year+1}` : `${year-1}/${year}`;
document.getElementById('season').textContent = `Season: ${season}`;
</script>

</body>
</html>
