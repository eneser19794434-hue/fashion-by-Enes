<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Fashion Luxury</title>
  <style>
    body { margin:0; font-family:'Helvetica Neue', Arial, sans-serif; background:#f4f4f4; color:#111; }
    header { background:#000; color:#fff; padding:20px 40px; display:flex; justify-content:space-between; align-items:center; }
    header h1 { margin:0; letter-spacing:3px; font-weight:600; }
    nav a { color:#fff; margin-left:20px; text-decoration:none; font-size:15px; }
    nav a:hover { opacity:0.7; }

    .hero { height:70vh; background:linear-gradient(rgba(0,0,0,.5),rgba(0,0,0,.5)), url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d') center/cover no-repeat; display:flex; align-items:center; justify-content:center; text-align:center; color:#fff; padding:20px; }
    .hero h2 { font-size:52px; margin-bottom:10px; letter-spacing:2px; }
    .hero p { font-size:18px; }
    .hero p.sub { letter-spacing:2px; font-size:14px; }

    .section { max-width:1200px; margin:auto; padding:70px 40px; }
    .section h3 { font-size:34px; margin-bottom:30px; text-align:center; letter-spacing:1px; }

    .products { display:grid; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); gap:30px; }
    .product { background:#fff; border-radius:10px; box-shadow:0 10px 25px rgba(0,0,0,.08); overflow:hidden; text-align:center; padding-bottom:15px; }
    .product img { width:100%; height:320px; object-fit:cover; }
    .product h4 { margin:15px 0 5px; font-size:18px; }
    select { padding:5px 8px; margin-bottom:10px; font-size:14px; }
    .price { font-weight:600; margin-bottom:10px; }
    .btn { display:inline-block; margin-bottom:10px; padding:12px 28px; background:#000; color:#fff; text-decoration:none; border-radius:30px; font-size:14px; cursor:pointer; }

    .payments { display:flex; justify-content:center; gap:30px; margin-top:20px; font-weight:600; }

    footer { background:#000; color:#fff; text-align:center; padding:30px 20px; }
    footer p { margin:8px 0; font-size:14px; }
  </style>
</head>
<body>

<header>
  <h1>FASHION LUXURY</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero" id="home">
  <div>
    <h2>FASHION LUXURY</h2>
    <p class="sub">EST. 2026</p>
  </div>
</section>

<section class="section" id="products">
  <h3>Luxury Collection</h3>
  <div class="products">
    <div class="product">
      <img src="https://images.unsplash.com/photo-1520975867597-0f1b6f6f1f8f" alt="Luxury Hoodie">
      <h4>Luxury Hoodie</h4>
      <select><option>Size S</option><option>Size M</option><option>Size L</option><option>Size XL</option></select>
      <p class="price">€89.99</p>
      <button class="btn" onclick="addToCart('Luxury Hoodie')">Add to Cart</button>
    </div>
    <div class="product">
      <img src="https://images.unsplash.com/photo-1523381210434-271e8be1f52b" alt="Designer T-Shirt">
      <h4>Designer T-Shirt</h4>
      <select><option>Size S</option><option>Size M</option><option>Size L</option><option>Size XL</option></select>
      <p class="price">€49.99</p>
      <button class="btn" onclick="addToCart('Designer T-Shirt')">Add to Cart</button>
    </div>
    <div class="product">
      <img src="https://images.unsplash.com/photo-1542060748-10c28b62716f" alt="Premium Jacket">
      <h4>Premium Jacket</h4>
      <select><option>Size S</option><option>Size M</option><option>Size L</option><option>Size XL</option></select>
      <p class="price">€159.99</p>
      <button class="btn" onclick="addToCart('Premium Jacket')">Add to Cart</button>
    </div>
    <div class="product">
      <img src="https://images.unsplash.com/photo-1600180758890-6b94519a8ba6" alt="Luxury Sneakers">
      <h4>Luxury Sneakers</h4>
      <select><option>40</option><option>41</option><option>42</option><option>43</option><option>44</option></select>
      <p class="price">€199.99</p>
      <button class="btn" onclick="addToCart('Luxury Sneakers')">Add to Cart</button>
    </div>
  </div>
  <p style="text-align:center;margin-top:30px;font-weight:600;">
    🛒 Cart items: <span id="cartCount">0</span><br><br>
    <button class="btn" onclick="checkout()">Checkout</button>
  </p>
</section>

<section class="section" id="about">
  <h3>About Us</h3>
  <p style="text-align:center; max-width:800px; margin:auto;">
    Fashion is a luxury fashion brand focused on premium quality, clean design and modern elegance.
  </p>
</section>

<section class="section" id="contact">
  <h3>Contact</h3>
  <p style="text-align:center;">Email: info@fashion.com</p>
  <p style="text-align:center;">Phone: 0493 48 77 07</p>
</section>

<footer>
  <p>&copy; 2026 Fashion Luxury</p>
  <p>Secure payments via Bancontact & PayPal (demo)</p>
</footer>

<script>
let cart = 0;
let orders = [];
function addToCart(item){
  cart++;
  orders.push(item);
  document.getElementById('cartCount').innerText = cart;
}
function checkout(){
  if(cart===0){ alert('Your cart is empty'); return; }
  alert('Order confirmed!\nPayment via PayPal / Bancontact (demo).\nThank you for your purchase.');
  cart = 0; orders = [];
  document.getElementById('cartCount').innerText = cart;
}
</script>

</body>
</html>
