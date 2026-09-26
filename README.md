# dennoh<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Dennoh</title>
<style>
  :root{
    --bg:#111; --card:#1c1c1c; --text:#f5f5f5; --accent:#7c5cff;
    padding-top: env(safe-area-inset-top,0px);
    padding-bottom: env(safe-area-inset-bottom,0px);
  }
  *{box-sizing:border-box;}
  html,body{height:100%;margin:0;}
  body{
    background:var(--bg); color:var(--text);
    font-family:-apple-system,Segoe UI,Roboto,sans-serif;
    display:flex; align-items:center; justify-content:center;
    min-height:100%;
  }
  .card{
    background:var(--card); padding:2.5rem 2rem; border-radius:20px;
    text-align:center; max-width:90vw; width:360px;
    box-shadow:0 10px 40px rgba(0,0,0,.5);
  }
  h1{font-size:2rem; margin:0 0 2rem;}
  .btns{display:flex; gap:1rem; justify-content:center;}
  button{
    flex:1; padding:.9rem 1rem; font-size:1.1rem; border:none;
    border-radius:12px; cursor:pointer; font-weight:600;
  }
  #yes{background:var(--accent); color:#fff;}
  #no{background:#333; color:#fff;}
  .hidden{display:none;}
</style>
</head>
<body>
  <div class="card" id="screen-main">
    <h1>Dennoh</h1>
    <div class="btns">
      <button id="yes">Yes</button>
      <button id="no">No</button>
    </div>
  </div>

  <div class="card hidden" id="screen-yes">
    <h1>F*** you.</h1>
  </div>

  <div class="card hidden" id="screen-no">
    <h1>You're a great friend. 🎉</h1>
  </div>

<script>
  const main = document.getElementById('screen-main');
  const yesScreen = document.getElementById('screen-yes');
  const noScreen = document.getElementById('screen-no');

  document.getElementById('yes').onclick = () => {
    main.classList.add('hidden');
    yesScreen.classList.remove('hidden');
  };
  document.getElementById('no').onclick = () => {
    main.classList.add('hidden');
    noScreen.classList.remove('hidden');
  };
</script>
</body>
</html>
