<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohan Restaurant</title>

<section class="hero">
    <video autoplay muted loop playsinline class="bg-video">
        <source src="restaurant.mp4" type="video/mp4">
    </video>

    <div class="hero-content">
        <h1>Welcome to Mohan Restaurant</h1>
        <p>Fresh • Delicious • Healthy</p>
        <button onclick="window.location.href='dishes.html'">Order Now</button>

    </div>
</section>
<div class="cart">
    🛒 Cart: <span id="count">0</span>
</div>
<button class="cart-btn">Add to Cart</button>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700;800&family=Cormorant+Garamond:wght@600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#000;
color:white;
overflow-x:hidden;
position:relative;
min-height:100vh;
}

body::before{
content:'';
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:
radial-gradient(circle at 20% 20%,rgba(255,255,255,.08),transparent 18%),
radial-gradient(circle at 80% 80%,rgba(255,255,255,.06),transparent 20%),
radial-gradient(circle at 50% 10%,rgba(255,255,255,.05),transparent 18%),
linear-gradient(180deg, #000 0%, #03030a 100%);
z-index:-2;
}

body::after{
content:'';
position:fixed;
inset:0;
background-image:
radial-gradient(2px 2px at 20px 30px, rgba(255,255,255,0.95), transparent),
radial-gradient(2px 2px at 40px 70px, rgba(255,255,255,0.8), transparent),
radial-gradient(1px 1px at 90px 40px, rgba(255,255,255,0.9), transparent),
radial-gradient(1px 1px at 130px 80px, rgba(255,255,255,0.75), transparent),
radial-gradient(2px 2px at 160px 30px, rgba(255,255,255,0.85), transparent);
background-repeat:repeat;
background-size:200px 120px;
opacity:.55;
animation:twinkle 6s ease-in-out infinite alternate;
z-index:-1;
}

.lens-glow{
position:fixed;
border-radius:50%;
filter:blur(60px);
opacity:.35;
pointer-events:none;
z-index:-1;
animation:floatLens 8s ease-in-out infinite alternate;
}

.lens-one{width:280px;height:280px;left:8%;top:12%;background:rgba(255,140,0,.22);animation-delay:0s;}
.lens-two{width:220px;height:220px;right:10%;top:18%;background:rgba(255,0,120,.18);animation-delay:1.2s;}
.lens-three{width:320px;height:320px;left:40%;bottom:6%;background:rgba(255,255,255,.16);animation-delay:2s;}

.hero-content h1 {
font-family:'Cormorant Garamond', serif;
font-size:clamp(2.6rem, 4.5vw, 4.2rem);
line-height:1.05;
letter-spacing:0.04em;
text-transform:uppercase;
color:#ffb347;
margin-bottom:16px;
text-shadow:0 0 20px rgba(255,179,71,0.22);
animation:titleGlow 2.4s ease-in-out infinite alternate;
}

.hero-content p {
font-size:1.1rem;
letter-spacing:0.14em;
text-transform:uppercase;
color:#f7d9a0;
animation:fadeUp 1s ease both;
}

/* Animated Background */

body::before{
content:'';
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:
radial-gradient(circle at 20% 20%,rgba(255,140,0,.25),transparent 30%),
radial-gradient(circle at 80% 80%,rgba(255,0,80,.25),transparent 35%),
radial-gradient(circle at 50% 50%,rgba(255,255,0,.15),transparent 40%);
animation:moveBg 12s infinite alternate ease-in-out;
z-index:-2;
}

@keyframes moveBg{

0%{
transform:scale(1);
filter:hue-rotate(0deg);
}

100%{
transform:scale(1.3);
filter:hue-rotate(80deg);
}

}

@keyframes twinkle {
  from { opacity: 0.3; transform: scale(0.95); }
  to { opacity: 0.8; transform: scale(1.05); }
}

nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 8%;
background:rgba(0,0,0,.4);
backdrop-filter:blur(10px);
position:sticky;
top:0;
z-index:100;
}

.logo{
font-size:34px;
font-weight:bold;
color:orange;
}

nav ul{
display:flex;
gap:30px;
list-style:none;
}

nav ul li{
cursor:pointer;
transition:.4s;
}

nav ul li:hover{
color:orange;
}

.hero{

display:flex;
justify-content:space-between;
align-items:center;
padding:70px 8%;
flex-wrap:wrap;
min-height:90vh;

}

.hero-text{
max-width:550px;
}

.hero h1{
font-size:60px;
margin-bottom:20px;
}

.hero span{
color:orange;
}

.hero p{
line-height:1.8;
margin-bottom:30px;
color:#ddd;
}

button{

padding:15px 35px;
border:none;
background:linear-gradient(135deg, #ffb347, #ff7f50);
color:white;
font-size:18px;
border-radius:50px;
cursor:pointer;
transition:.4s;
box-shadow:0 10px 20px rgba(255,127,80,0.24);

}

button:hover{

background:red;
transform:scale(1.08);

}

.hero img{

width:450px;
animation:float 3s infinite ease-in-out;
filter:drop-shadow(0 0 30px orange);

}

@keyframes float{

50%{
transform:translateY(-20px);
}

}

/* dishes */

.title{

text-align:center;
font-size:45px;
margin:50px 0;
color:orange;

}

.container{

display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:35px;
padding:40px 8%;

}

.card{

background:#222;
border-radius:20px;
overflow:hidden;
transition:.5s;

}

.card:hover{

transform:translateY(-12px) scale(1.04);

box-shadow:0 15px 35px rgba(255,140,0,.5);

}

.card img{

width:100%;
height:220px;
object-fit:cover;

}

.card-content{

padding:20px;

}

.card h3{

margin-bottom:10px;

}

.price{

color:orange;
font-size:22px;
margin:15px 0;

}

footer{

text-align:center;
padding:40px;
background:#000;
margin-top:50px;

}

@keyframes titleGlow {
  from {
    text-shadow: 0 0 10px rgba(255,179,71,0.18);
    transform: translateY(0);
  }
  to {
    text-shadow: 0 0 24px rgba(255,179,71,0.32);
    transform: translateY(-2px);
  }
}

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.circle{

position:fixed;
border-radius:50%;
background:rgba(255,165,0,.15);
pointer-events:none;
animation:rise linear infinite;

}

@keyframes rise{

from{

transform:translateY(100vh) scale(.3);

}

to{

transform:translateY(-120vh) scale(1);

}

}

@keyframes floatLens {
  from { transform: translate3d(0,0,0) scale(1); }
  to { transform: translate3d(18px,-20px,0) scale(1.06); }
}


</style>

</head>

<body>
<div class="lens-glow lens-one"></div>
<div class="lens-glow lens-two"></div>
<div class="lens-glow lens-three"></div>

<nav>

<div class="logo">🍴 Mohan Restaurant</div>

<ul>

<li>Home</li>
<li>Menu</li>
<li>Special</li>
<li>Gallery</li>
<li>Contact</li>

</ul>

</nav>

<section class="hero">

<div class="hero-text">

<h1>Enjoy Delicious <span>Food</span></h1>

<p>
Fresh ingredients, traditional recipes and unforgettable taste.
Experience premium dining with beautiful dishes prepared by expert chefs.
</p>

<button>Order Now</button>

</div>

<img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=800" alt="Pizza">

</section>

<h2 class="title">Popular Dishes</h2>

<section class="container">

<div class="card">

<img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=700">

<div class="card-content">

<h3>Cheese Pizza</h3>

<p>Loaded with cheese and fresh vegetables.</p>

<div class="price">₹299</div>

<button>Buy</button>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1550547660-d9450f859349?w=700">

<div class="card-content">

<h3>Burger</h3>

<p>Juicy grilled burger with fries.</p>

<div class="price">₹249</div>

<button>Buy</button>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1604908176997-125f25cc6f3d?w=700">

<div class="card-content">

<h3>Pasta</h3>

<p>Italian creamy white sauce pasta.</p>

<div class="price">₹349</div>

<button>Buy</button>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1544025162-d76694265947?w=700">

<div class="card-content">

<h3>Grilled Chicken</h3>

<p>Perfectly grilled with herbs.</p>

<div class="price">₹499</div>

<button>Buy</button>

</div>

</div>

</section>

<footer>

<h2>Mohan Restaurant</h2>

<p>Fresh Food • Great Taste • Fast Delivery</p>

</footer>

<script>

// Floating animated circles

for(let i=0;i<30;i++){

let c=document.createElement("div");

c.className="circle";

let size=Math.random()*25+10;

c.style.width=size+"px";
c.style.height=size+"px";

c.style.left=Math.random()*100+"vw";

c.style.animationDuration=(Math.random()*10+8)+"s";

c.style.animationDelay=Math.random()*5+"s";

document.body.appendChild(c);

}

// Button Animation

document.querySelectorAll("button").forEach(btn=>{

btn.addEventListener("mouseenter",()=>{

btn.style.transform="scale(1.1)";

});

btn.addEventListener("mouseleave",()=>{

btn.style.transform="scale(1)";

});

});

</script>

</body>
</html>
