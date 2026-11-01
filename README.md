<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fashion World | Online Store</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:Arial,sans-serif;color:#222;background:#fff}
header{background:#171717;color:white;padding:20px;text-align:center}
header h1{letter-spacing:3px}
nav{display:flex;justify-content:center;gap:22px;padding:15px;background:#292929}
nav a{color:white;text-decoration:none;font-size:14px}
.hero{background:#eee;text-align:center;padding:65px 15px}
.hero h2{font-size:36px;margin-bottom:12px}
.hero p{color:#555;margin-bottom:20px}
.btn{display:inline-block;background:#171717;color:white;padding:13px 24px;text-decoration:none;border:none;cursor:pointer}
section{padding:40px 18px}
h2.title{text-align:center;margin-bottom:28px}
.products{display:grid;grid-template-columns:repeat(2,1fr);gap:18px;max-width:850px;margin:auto}
.product{border:1px solid #eee;padding:10px;text-align:center}
.product img{width:100%;height:190px;object-fit:cover}
.product h3{font-size:16px;margin:12px 0}
.product p{margin-bottom:12px;color:#555}
.product button{background:#171717;color:white;border:0;padding:10px 14px;cursor:pointer}
#cart{text-align:center;background:#f5f5f5;padding:25px}
.about{text-align:center;line-height:1.8;max-width:650px;margin:auto}
.contact{text-align:center;background:#eee}
.contact p{margin:15px}
footer{background:#171717;color:white;text-align:center;padding:22px}
@media(max-width:380px){
 .hero h2{font-size:29px}
 .product img{height:150px}
 nav{gap:12px}
}
</style>
</head>
<body>

<header>
<h1>FASHION WORLD</h1>
<p>Your Style, Your Fashion</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#shop">Shop</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</nav>

<div class="hero" id="home">
<h2>Discover Your Style</h2>
<p>Explore the latest fashion collections.</p>
<a href="#shop" class="btn">SHOP NOW</a>
</div>

<section id="shop">
<h2 class="title">Our Collection</h2>
<div class="products">

<div class="product">
<img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?w=500" alt="T Shirt">
<h3>Classic T-Shirt</h3>
<p>₹499</p>
<button onclick="addCart('Classic T-Shirt',499)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1542272604-787c3835535d?w=500" alt="Jeans">
<h3>Denim Jeans</h3>
<p>₹999</p>
<button onclick="addCart('Denim Jeans',999)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1591047139829-d91aecb6caea?w=500" alt="Jacket">
<h3>Stylish Jacket</h3>
<p>₹1,499</p>
<button onclick="addCart('Stylish Jacket',1499)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1483985988355-763728e1935b?w=500" alt="Fashion Outfit">
<h3>Fashion Outfit</h3>
<p>₹1,299</p>
<button onclick="addCart('Fashion Outfit',1299)">Add to Cart</button>
</div>

</div>
</section>

<div id="cart">
<h2>Your Cart 🛒</h2>
<p id="cartItems">No items added yet.</p>
<h3 id="total">Total: ₹0</h3>
</div>

<section id="about">
<h2 class="title">About Us</h2>
<div class="about">
<p>Welcome to Fashion World! We bring you stylish and modern fashion collections. Discover your favorite looks and express your unique style with us.</p>
</div>
</section>

<section class="contact" id="contact">
<h2 class="title">Contact Us</h2>
<p>Interested in our collection?</p>
<a class="btn" href="https://wa.me/91XXXXXXXXXX">WhatsApp Us</a>
</section>

<footer>
<p>© 2026 Fashion World. All Rights Reserved.</p>
<p>Website Demo by Dev</p>
</footer>

<script>
let cart=[];
function addCart(name,price){
cart.push({name,price});
document.getElementById("cartItems").innerText=
cart.map(item=>item.name+" - ₹"+item.price).join(" | ");
let total=cart.reduce((sum,item)=>sum+item.price,0);
document.getElementById("total").innerText="Total: ₹"+total;
}
</script>

</body>
</html>
