<!DOCTYPE html>
<html>
<head>
<title>GreenBuild KE Calculator</title>
<style>
body{font-family:system-ui;background:#f0faf0;padding:20px;max-width:400px;margin:auto}
.card{background:white;border-radius:16px;padding:20px;box-shadow:0 4px 12px rgba(0,0,0,0.1);border-left:6px solid #2e7d32}
h2{color:#2e7d32;margin:0 0 10px}
input{width:100%;padding:10px;margin:8px 0;border-radius:8px;border:1px solid #ccc}
.btn{background:#2e7d32;color:white;border:none;padding:12px;width:100%;border-radius:10px;font-weight:bold;cursor:pointer}
.result{margin-top:15px;background:#e8f5e9;padding:12px;border-radius:10px;display:none}
</style>
</head>
<body>
<div class="card">
<h2>🌱 GreenBuild KE</h2>
<p>Estimate savings for homes under 2M KES</p>
<input id="homes" type="number" placeholder="Number of homes (e.g. 100)">
<input id="cost" type="number" placeholder="Avg cost per home (KES)">
<button class="btn" onclick="calc()">Calculate Impact</button>
<div id="out" class="result"></div>
</div>
<script>
function calc(){
 let h = document.getElementById('homes').value || 100;
 let c = document.getElementById('cost').value || 2000000;
 let energy = h * 0.5 * 12000; // 50% cut
 let waste = h * 0.3 * 2.5; // tons
 let families = h;
 document.getElementById('out').style.display='block';
 document.getElementById('out').innerHTML = `
  🏠 <b>${families} families housed</b><br>
  ⚡ KES ${energy.toLocaleString()} energy saved / year<br>
  ♻️ ${waste} tons waste diverted<br>
  💰 Total value: KES ${(h*c).toLocaleString()}<br><br>
  <small>Powered by solar + rainwater + recycled bricks</small>
 `;
}
</script>
</body>
</html>
<!-- ZICKEYMUTULI GREEN BUILD BRAND MARK -->
<svg width="400" height="120" viewBox="0 0 400 120" xmlns="http://www.w3.org/2000/svg">
  <!-- Icon: House + Leaf -->
  <g>
    <path d="M30 60 L60 30 L90 60 L80 60 L80 90 L40 90 L40 60 Z" fill="#2E7D32" stroke="#1B5E20" stroke-width="2"/>
    <path d="M60 90 C45 75 55 55 60 50 C65 55 75 75 60 90 Z" fill="#81C784"/>
    <circle cx="60" cy="72" r="4" fill="#1B5E20"/>
  </g>
  <!-- Brand Name -->
  <text x="110" y="55" font-family="system-ui, sans-serif" font-weight="800" font-size="22" fill="#1B5E20">GREENBUILD</text>
  <text x="110" y="78" font-family="system-ui, sans-serif" font-weight="300" font-size="16" fill="#2E7D32" letter-spacing="4">KE</text>
  
  <!-- Signature Line -->
  <line x1="110" y1="88" x2="320" y2="88" stroke="#C8E6C9" stroke-width="1"/>
  <text x="110" y="105" font-family="monospace" font-size="9" fill="#666">Created by zickeymutuli ©2026 all rights reserved</text>
</svg>
