<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Shop</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            margin: 0; 
            padding: 0; 
            background: url('https://www.getsims.com/wp-content/uploads/2020/12/gradient-background-02.jpg') no-repeat center center fixed; 
            background-size: cover; 
            text-align: center; 
        }
        header { background-color: #343a40; color: white; padding: 20px; font-size: 24px; }
        nav { background: #23272b; padding: 10px; }
        nav a { color: white; text-decoration: none; margin: 15px; font-size: 18px; }
        .container { display: flex; justify-content: center; flex-wrap: wrap; padding: 20px; }
        .product { 
            background: white; 
            border-radius: 10px; 
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px; 
            margin: 15px; 
            width: 250px; 
            text-align: center;
            transition: transform 0.3s;
        }
        .product:hover { transform: scale(1.05); }
        .product img { width: 100%; border-radius: 10px; }
        .product h2 { font-size: 18px; color: #333; }
        .product p { color: #666; }
        button { 
            background-color: #28a745; 
            color: white; 
            border: none; 
            padding: 10px 15px; 
            cursor: pointer; 
            border-radius: 5px;
            font-size: 16px;
        }
        button:hover { background-color: #218838; }
        footer { background: #343a40; color: white; padding: 15px; margin-top: 20px; font-size: 16px; }
    </style>
</head>
<body>
    <header>Welcome to Simple Shop</header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Products</a>
        <a href="#">Contact</a>
    </nav>
    <div class="container">
        <div class="product">
            <img src="https://via.placeholder.com/250" alt="Product 1">
            <h2>Product 1</h2>
            <p>Price: $10</p>
            <button onclick="orderNow('Product 1')">Order Now</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/250" alt="Product 2">
            <h2>Product 2</h2>
            <p>Price: $15</p>
            <button onclick="orderNow('Product 2')">Order Now</button>
        </div>
    </div>
    <footer>
        Contact us at: example@example.com | Phone: +123 456 7890
    </footer>
    <script>
        function orderNow(product) {
            let name = prompt("Enter your name:");
            let address = prompt("Enter your address:");
            if (name && address) {
                alert("Order placed for " + product + "\nName: " + name + "\nAddress: " + address + "\nPayment: Cash on Delivery");
            } else {
                alert("Order cancelled. Please enter valid details.");
            }
        }
    </script>
</body>
</html>
