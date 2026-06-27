<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mohan Restaurant - Dishes</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700;800&family=Cormorant+Garamond:wght@600;700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="style.css" />
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
    body {
      background: #111;
      color: white;
      min-height: 100vh;
      padding: 30px 8%;
    }
    .page-title {
      font-family: 'Cormorant Garamond', serif;
      color: #ffb347;
      margin-bottom: 10px;
      letter-spacing: 0.04em;
      font-size: clamp(2rem, 3.8vw, 2.8rem);
      text-transform: uppercase;
      text-shadow: 0 0 18px rgba(255,179,71,0.25);
    }
    .page-subtitle { color: #ddd; margin-bottom: 30px; font-size: 1rem; }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }
    .card {
      background: rgba(34, 34, 34, 0.92);
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 14px 30px rgba(0,0,0,0.28);
      border: 1px solid rgba(255,255,255,0.07);
      backdrop-filter: blur(8px);
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
      background: linear-gradient(135deg, #ffb347, #ff7f50);
      color: white;
      text-decoration: none;
      border-radius: 999px;
      box-shadow: 0 10px 18px rgba(255,127,80,0.25);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
    }
    .back-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 22px rgba(255,127,80,0.35);
    }
  </style>
</head>
<body>
  <a class="back-btn" href="index.html">← Back to Home</a>
  <h1 class="page-title">Mohan Restaurant</h1>
  <p class="page-subtitle">Choose from fresh, healthy, and flavorful meals.</p>

  <div class="grid">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1512621776951-a57141f2eefd?auto=format&fit=crop&w=800&q=80" alt="Grilled Chicken Bowl" />
      <div class="card-content">
        <h3>Grilled Chicken Bowl</h3>
        <p>Fresh vegetables, rice, and juicy grilled chicken.</p>
        <div class="price">₹1,299</div>
      </div>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1621996346565-e3dbc646d9a9?auto=format&fit=crop&w=800&q=80" alt="Veggie Pasta" />
      <div class="card-content">
        <h3>Veggie Pasta</h3>
        <p>Healthy pasta with herbs, tomato sauce, and veggies.</p>
        <div class="price">₹1,049</div>
      </div>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=800&q=80" alt="Fresh Salad" />
      <div class="card-content">
        <h3>Fresh Salad</h3>
        <p>Crunchy greens with avocado, nuts, and dressing.</p>
        <div class="price">₹899</div>
      </div>
    </div>
  </div>
</body>
</html>
