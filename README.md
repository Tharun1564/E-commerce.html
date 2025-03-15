<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" 
          content="width=device-width, initial-scale=1.0">
    <title>E-commerce website</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f3f4f6;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin:0 auto;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            position:relative;
        }
        .logo{
            position: absolute;
            height: 100px;
            left: 40px;
            width: 100px;
            top: 10px;
            display: flex;
        }

        header {
            background: linear-gradient(to right, #48c184, #a273e5);
            color: #ffffff;
            padding: 20px 0;
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            position:fixed;        
        }

        header h1 {
            font-size: 2.5rem;
            margin: 0;
        }

        header nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        header nav ul li {
            display: inline;
        }

        header nav ul li a {
            color: #ffffff;
            text-decoration: none;
            font-size: 1.2rem;
            transition: color 0.3s ease;
        }

        header nav ul li a:hover {
            color: #f3f4f6;
        }

        #products {
            margin-bottom: 20px;
            flex: 1;
        }

        .product {
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            padding: 10px;
            margin-bottom: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .product:hover {
            transform: translateY(-5px);
        }

        .product img {
            width: 100%;
            max-width: 200px;
            height: auto;
            margin-bottom: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .product h3 {
            font-size: 1.5rem;
            margin: 0;
        }

        .product p {
            color: #666666;
            margin-bottom: 0.5rem;
        }

        .product button {
            background: linear-gradient(to right, #11998e, #38ef7d);
            color: #ffffff;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            outline: none;
        }

        .product button:hover {
            background: linear-gradient(to right, #0c8976, #30c270);
        }

        #cart {
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            padding: 20px;
            width: 300px;
        }

        #cart h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #333;
        }

        #cart-items {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .cart-item button {
            background: linear-gradient(to right, #ff4d4f, #ff6382);
            color: #ffffff;
            border: none;
            padding: 4px 8px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            outline: none;
        }

        .cart-item button:hover {
            background: linear-gradient(to right, #e63c3f, #f34d6f);
        }

        .quantity {
            display: flex;
            align-items: center;
        }

        .quantity button {
            background: linear-gradient(to right, #11998e, #38ef7d);
            color: #ffffff;
            border: none;
            padding: 4px 8px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            outline: none;
        }

        .quantity button:hover {
            background: linear-gradient(to right, #0bb940, #36ed61);
        }

        .quantity input {
            width: 40px;
            text-align: center;
            border: 1px solid #ccc;
            border-radius: 4px;
            margin: 0 0.5rem;
            padding: 4px;
            outline: none;
        }
        footer {
background-color: #333;
color: #fff;
padding:1em;
text-align: center;
clear: both;
}

footer{
    position:relative;
    
}
    </style>
</head>

<body>
    <header>
        <div class="container">
            <h1>E-commerse</h1>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Products</a></li>
                    <li><a href="#">Cart</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <div class="container">
        <section id="products">
            <h2>Available Products</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 
                        md:grid-cols-3 lg:grid-cols-4 gap-6">
                <div class="product">
                    <img 
                    src=
"https://media.geeksforgeeks.org/wp-content/uploads/20240308174326/d12.jpg"
                     alt="Salt">
                    <h3>Salt</h3>
                    <p>$2.00</p>
                    <button onclick="addToCart('Salt', 2.00)">
                          Add to Cart
                      </button>
                </div>
                <div class="product">
                    <img 
                    src=
"https://media.geeksforgeeks.org/wp-content/uploads/20240308174500/f12.jpg"
                     alt="Apple">
                    <h3>Apple</h3>
                    <p>$5.00</p>
                    <button onclick="addToCart('Apple', 5.00)">
                          Add to Cart
                      </button>
                </div>
                <div class="product">
                    <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20240308174616/o12.jpg" alt="Orange">
                    <h3>Orange</h3>
                    <p>$4.00</p>
                    <button onclick="addToCart('Orange', 4.00)">
                          Add to Cart
                      </button>
                </div>
                <div class="product">
                    <img src=
"https://media.geeksforgeeks.org/wp-content/uploads/20240308181947/o123.jpg"
                     alt="Oil">
                    <h3>Oil</h3>
                    <p>$8.00</p>
                    <button onclick="addToCart('Oil', 8.00)">
                          Add to Cart
                      </button>
                    </div>
            </div>
        </section>
        <aside id="cart">
            <h2>Shopping Cart</h2>
            <ul id="cart-items">
            </ul>
            <button id="buy-button" onclick="checkout()">Buy</button>
        </aside>
    </div>
   <script>
        let Items = [];
        function addToCart(name, price) {
            const index = Items.findIndex(item => item.name === name);
            if (index !== -1) {
                Items[index].quantity += 1;
            } else {
                const item = {
                    name: name,
                    price: price,
                    quantity: 1
                };
                Items.push(item);
            }
            updateCartDisplay();
        }
        function deleteFromCart(index) {
            Items.splice(index, 1);
            updateCartDisplay();
        }
        function updateQuantity(index, quantity) {
            Items[index].quantity = quantity;
            updateCartDisplay();
        }
        function checkout() {
            let totalPrice = 0;
            Items.forEach(item => {
                totalPrice += item.price * item.quantity;
            });
            alert(Totalprice: $$ {totalPrice.toFixed(2)} );
        }
        function updateCartDisplay() {
            const cartElement = document.getElementById('cart-items');
            cartElement.innerHTML = '';
            Items.forEach((item, index) => {
                const li = document.createElement('li');
                li.className = 'cart-item';
                li.innerHTML = `
                    <span>${item.name} - $${item.price.toFixed(2)} x 
                    <div class="quantity">
                        <button onclick="updateQuantity(${index},
                         ${item.quantity - 1})">-</button>
                        <input type="number" 
                        value="${item.quantity}" 
                        min="1" max="10" 
                        onchange="updateQuantity(${index},
                         this.value)">
                        <button 
                        onclick="updateQuantity(${index},
                         ${item.quantity + 1})">+</button>
                    </div>
                    </span>
                    <button onclick="deleteFromCart(${index})">Delete</button>
                `;
                cartElement.appendChild(li);
            });
        }
    </script>
    <footer>
        <p>&copy; 2025 Your Name. All rights reserved.</p>
        </footer>
</body>

</html>
