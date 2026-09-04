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
