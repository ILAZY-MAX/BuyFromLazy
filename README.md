<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Shop</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Samsung+Sans:wght@400;700&display=swap');
        
        body { 
            font-family: Arial, sans-serif; 
            margin: 0; 
            padding: 0; 
            background: url('https://wallpaperaccess.com/full/2645955.jpg') no-repeat center center fixed; 
            background-size: cover; 
            text-align: center; 
        }
        
        header { 
            background: linear-gradient(90deg, #ff0000, #ff8c00, #ffff00, #00ff00, #0000ff, #4b0082, #8b00ff);
            padding: 20px; 
            font-size: 24px; 
            font-family: 'Samsung Sans', sans-serif;
            text-transform: uppercase;
            font-weight: bold;
            text-shadow: 0 0 5px #fff, 0 0 10px #ff0000, 0 0 15px #00ff00, 0 0 20px #0000ff;
            color: black; 
            display: inline-block;
            border-radius: 10px;
            padding: 15px 30px;
        }
        
        nav { background: #23272b; padding: 10px; }
        nav a { color: white; text-decoration: none; margin: 15px; font-size: 18px; }
        .container { display: flex; justify-content: center; flex-wrap: wrap; padding: 20px; }
        .category, .product { 
            background: black; 
            border-radius: 10px; 
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px; 
            margin: 15px; 
            width: 250px; 
            text-align: center;
            transition: transform 0.3s;
            cursor: pointer;
        }
        .category:hover, .product:hover { transform: scale(1.05); }
        .category img, .product img { width: 100%; border-radius: 10px; }
        .category h2, .product h2 { font-size: 18px; color: #333; }
        .category p, .product p { color: #666; }
        footer { background: #343a40; color: white; padding: 15px; margin-top: 20px; font-size: 16px; }
    </style>
</head>
<body>
    <header>NO COMPROMISE WITH PERFORMANCE</header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Categories</a>
        <a href="#">Contact</a>
    </nav>
    
    <div class="container" id="landing-page">
        <div class="category" onclick="showCategory('Prebuilt PCs')">
            <img src="https://th.bing.com/th/id/OIP.fkOKg96G5_2vp4F1ACs6gQHaHa?rs=1&pid=ImgDetMain" alt="Prebuilt PCs">
            <h2>Prebuilt PCs</h2>
            <p>High-performance gaming and work PCs.</p>
        </div>
        <div class="category" onclick="showCategory('PC Parts')">
            <img src="https://cdn.wccftech.com/wp-content/uploads/2018/09/DSC_0098-Custom.jpg" alt="PC Parts">
            <h2>PC Parts</h2>
            <p>Customize your build with high-quality components.</p>
        </div>
    </div>

    <div class="container" id="pc-parts" style="display: none;">
        <div class="category" onclick="showProducts('GPU')">
            <h2>GPU</h2>
        </div>
        <div class="category" onclick="showProducts('CPU')">
            <h2>CPU</h2>
        </div>
        <div class="category" onclick="showProducts('RAM')">
            <h2>RAM</h2>
        </div>
        <div class="category" onclick="showProducts('Motherboard')">
            <h2>Motherboard</h2>
        </div>
    </div>

    <div class="container" id="product-list" style="display: none;">
        <div class="product" onclick="showProductDetails('Product 1')">
            <img src="https://via.placeholder.com/250" alt="Product 1">
            <h2>Product 1</h2>
            <p>Price: $100</p>
        </div>
        <div class="product" onclick="showProductDetails('Product 2')">
            <img src="https://via.placeholder.com/250" alt="Product 2">
            <h2>Product 2</h2>
            <p>Price: $150</p>
        </div>
    </div>
    
    <footer>
        Contact us at: example@example.com | Phone: +123 456 7890
    </footer>
    
    <script>
        function showCategory(category) {
            document.getElementById('landing-page').style.display = 'none';
            if (category === 'PC Parts') {
                document.getElementById('pc-parts').style.display = 'flex';
            } else {
                document.getElementById('product-list').style.display = 'flex';
            }
        }

        function showProducts(category) {
            document.getElementById('pc-parts').style.display = 'none';
            document.getElementById('product-list').style.display = 'flex';
        }

        function showProductDetails(product) {
            alert("Showing details for " + product);
        }
    </script>
</body>
</html>
