<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incognito Maggi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9fb; 
            color: #333; 
        }
        header {
            background: linear-gradient(90deg, #ff9800, #ff5722); 
            color: white;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        header img {
            width: 60px; /* Increased size for the logo */
            height: 60px;
            vertical-align: middle;
            margin-right: 10px;
        }
        img {
            width: 120px; /* Increased size for all images */
            height: auto; /* Maintain aspect ratio */
            border-radius: 8px; /* Optional rounded corners */
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 16px;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }
        .menu-item h3 {
            margin: 0;
            font-size: 20px;
            font-weight: bold;
        }
        .menu-item p {
            margin: 5px 0;
            color: #555;
            font-size: 14px;
        }
        .menu-item button {
            background-color: #ff9800; 
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
            transition: background-color 0.3s, transform 0.2s;
        }
        .menu-item button:hover {
            background-color: #e68900; /* Darker orange on hover */
            transform: scale(1.05);
        }
        footer {
            text-align: center;
            padding: 15px;
            background: linear-gradient(90deg, #ff5722, #ff9800); /* Gradient footer */
            color: white;
            font-size: 14px;
            box-shadow: 0 -4px 6px rgba(0, 0, 0, 0.1);
        }
        .cart {
            position: fixed;
            top: 20px;
            right: 20px;
            background: white;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border: 1px solid #ddd;
        }
        .cart h3 {
            margin: 0;
            font-size: 18px;
            font-weight: bold;
        }
        .cart ul {
            list-style: none;
            padding: 0;
            margin: 10px 0;
        }
        .cart ul li {
            font-size: 14px;
            margin-bottom: 5px;
        }
    </style>
</head>
</head>
<body>
    <header>        
        <h1>Incognito Maggi</h1>
        <p>Delicious Maggi, Delivered to Your Doorstep!</p>
        <nav>
            <a href="#menu">Menu</a>
            <a href="#about">About</a>
            <a href="contact us.mp4">Contact</a>
        </nav>
    </header>
    <div class="cart">
        <h3>Cart</h3>
        <ul id="cart-items">
            <li>No items in cart</li>
        </ul>
    </div>
    <div class="container" id="menu">
        <div class="menu-item">
            <img src="Classic Maggi.avif"style="width: 300px; height: 600spx;" alt="Classic Maggi"> <!-- Add image -->
            <div>
                <h3>Classic Maggi</h3>
                <p>Price: 70₹</p>
            </div>
            <button onclick="addToCart('Classic Maggi', 70)">Order Now</button>
        </div>
        <div class="menu-item">
            <img src="Cheese Maggi" style="width: 300px; height: 600spx;" alt="Cheese Maggi"> <!-- Add image -->
            <div>
                <h3>Cheese Maggi</h3>
                <p>Price: 90₹</p>
            </div>
            <button onclick="addToCart('Cheese Maggi', 90)">Order Now</button>
        </div>
        <div class="menu-item">
            <img src="Spicy Maggi" style="width: 300px; height: 600spx;" alt="Spicy Maggi"> <!-- Add image -->
            <div>
                <h3>Spicy Maggi</h3>
                <p>Price: 70₹</p>
            </div>
            <button onclick="addToCart('Spicy Maggie', 70)">Order Now</button>
        </div>
        <div class="menu-item">
            <img src="Veggie Maggie" style="width: 300px; height: 600spx;" alt="Veggie Maggie"> <!-- Add image -->
            <div>
                <h3>Veggie Maggi</h3>
                <p>Price: 80₹</p>
            </div>
            <button onclick="addToCart('Veggie Maggie', 80)">Order Now</button>
        </div>
    </div>
    <footer>
        <p>&copy; For any inquiries, call: 8767101084</p>
    </footer>
    <script>
        const cartItems = document.getElementById('cart-items');

        function addToCart(item, price) {
            const listItem = document.createElement('li');
            listItem.textContent = `${item} - ₹${price}`;
            if (cartItems.children[0].textContent === 'No items in cart') {
                cartItems.innerHTML = '';
            }
            cartItems.appendChild(listItem);
        }
    </script>
</body>
</html>
