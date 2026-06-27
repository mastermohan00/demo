<!DOCTYPE html>
<!-- saved from url=(0033)http://127.0.0.1:5500/dishes.html -->
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mohan Restaurant - Dishes</title>
  
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
    body {
      background: #111;
      color: white;
      min-height: 100vh;
      padding: 30px 8%;
    }
    h1 { color: orange; margin-bottom: 20px; }
    p { color: #ddd; margin-bottom: 30px; }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }
    .card {
      background: #222;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      display: block;
    }
    .card-content { padding: 20px; }
    .card h3 { margin-bottom: 10px; color: orange; }
    .card .price { color: #fff; font-weight: 600; margin-top: 10px; }
    .back-btn {
      display: inline-block;
      margin-bottom: 24px;
      padding: 10px 20px;
      background: orange;
      color: white;
      text-decoration: none;
      border-radius: 999px;
    }
  </style>
<link href="./Mohan Restaurant - Dishes_files/css2" rel="stylesheet"></head>
<body>
  <a class="back-btn" href="http://127.0.0.1:5500/index.html">← Back to Home</a>
  <h1>Our Delicious Dishes</h1>
  <p>Choose from fresh, healthy, and flavorful meals.</p>

  <div class="grid">
    <div class="card">
      <img src="./Mohan Restaurant - Dishes_files/photo-1512621776951-a57141f2eefd" alt="Grilled Chicken Bowl">
      <div class="card-content">
        <h3>Grilled Chicken Bowl</h3>
        <p>Fresh vegetables, rice, and juicy grilled chicken.</p>
        <div class="price">$12.99</div>
      </div>
    </div>
    <div class="card">
      <img src="./Mohan Restaurant - Dishes_files/photo-1621996346565-e3dbc646d9a9" alt="Veggie Pasta">
      <div class="card-content">
        <h3>Veggie Pasta</h3>
        <p>Healthy pasta with herbs, tomato sauce, and veggies.</p>
        <div class="price">$10.49</div>
      </div>
    </div>
    <div class="card">
      <img src="./Mohan Restaurant - Dishes_files/photo-1547592180-85f173990554" alt="Fresh Salad">
      <div class="card-content">
        <h3>Fresh Salad</h3>
        <p>Crunchy greens with avocado, nuts, and dressing.</p>
        <div class="price">$8.99</div>
      </div>
    </div>
  </div>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>


</body></html>
