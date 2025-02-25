<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bloom N Love</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">
    <script src="https://js.stripe.com/v3/"></script> <!-- Stripe.js for real integration -->
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f5f5f5;
            color: #333;
            padding: 20px;
            line-height: 1.6;
        }
        header {
            text-align: center;
            padding: 20px;
            background: white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        #logo {
            max-width: 150px;
        }
        nav ul {
            list-style: none;
            padding: 10px 0;
        }
        nav ul li {
            display: inline-block;
            margin: 0 15px;
        }
        nav ul li a {
            font-size: 18px;
            text-decoration: none;
            color: #d63384;
        }
        nav ul li a:hover {
            color: #ad1457;
        }
        section {
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            max-width: 1200px;
            margin: 0 auto;
            display: none;
        }
        #design-tshirt {
            display: block;
        }
        .container {
            display: flex;
            justify-content: center;
            align-items: flex-start;
            max-width: 1200px;
            margin: 0 auto;
            flex-wrap: wrap;
            gap: 20px;
        }
        .preview {
            position: relative;
            flex: 1 1 400px;
            max-width: 500px;
            text-align: center;
            border: 2px dashed #ccc;
            background-color: #f0f0f0;
            overflow: hidden;
        }
        #tshirt-image {
            width: 100%;
            max-width: 400px;
            height: auto;
        }
        #design-overlay {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            max-width: 100%;
            height: auto;
            display: none;
            z-index: 5;
        }
        #text-overlay {
            position: absolute;
            top: 55%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 12px;
            font-weight: bold;
            color: rgb(255, 255, 255);
            text-align: center;
            width: 80%;
            display: none;
            z-index: 10;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }
        .dropped-image {
            position: absolute;
            max-width: 100px;
            height: auto;
            z-index: 15;
            cursor: move;
            pointer-events: auto;
        }
        .customization {
            flex: 1 1 300px;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .customization label {
            font-weight: bold;
            margin-bottom: 5px;
            display: block;
        }
        .customization select,
        .customization input[type="text"],
        .customization input[type="file"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .color-choices-container {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        .color-choice {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid #ccc;
            transition: transform 0.2s, border-color 0.2s;
        }
        .color-choice:hover {
            transform: scale(1.1);
            border-color: #d63384;
        }
        .color-choice[data-color="white"] { background-color: white; }
        .color-choice[data-color="black"] { background-color: black; }
        .color-choice[data-color="red"] { background-color: red; }
        .color-choice[data-color="pink"] { background-color: pink; }
        .color-choice[data-color="blue"] { background-color: blue; }
        .color-choice[data-color="gold"] { background-color: gold; }
        .image-upload-box {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            border: 1px solid #ddd;
            margin-bottom: 15px;
        }
        .image-count {
            display: flex;
            gap: 10px;
            margin-bottom: 10px;
        }
        .image-count button {
            padding: 5px 10px;
            background: #e0e0e0;
            border: 1px solid #ccc;
            border-radius: 4px;
            cursor: pointer;
        }
        .image-count button.active {
            background: #d63384;
            color: white;
            border-color: #d63384;
        }
        .upload-button {
            background: #4CAF50;
            color: white;
            padding: 8px 16px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .upload-button:hover {
            background: #45a049;
        }
        #uploaded-images-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        .image-box {
            position: relative;
            width: 100px;
            height: 100px;
            border: 2px solid #ccc;
            border-radius: 5px;
            overflow: hidden;
            background-color: #f0f0f0;
            cursor: pointer;
        }
        .image-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .remove-btn {
            position: absolute;
            top: 5px;
            right: 5px;
            background: red;
            color: white;
            border: none;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            cursor: pointer;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 20;
        }
        .remove-btn:hover {
            background: darkred;
        }
        .preview.dragover {
            background-color: #e1e1e1;
            border-color: #999;
        }
        button {
            padding: 8px 16px;
            background: #d63384;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background: #ad1457;
        }
        #cart-items, #checkout-form, #orders-list {
            margin-top: 20px;
        }
        .cart-item {
            padding: 15px;
            border-bottom: 1px solid #ccc;
            display: flex;
            align-items: center;
            gap: 10px;
            position: relative;
        }
        .cart-preview {
            position: relative;
            width: 150px;
            height: 150px;
        }
        .cart-preview img {
            position: absolute;
            width: 100%;
            height: auto;
        }
        .cart-preview .design-overlay {
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            max-width: 90%;
            z-index: 5;
        }
        .cart-preview .text-overlay {
            top: 55%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 10px;
            font-weight: bold;
            text-align: center;
            width: 80%;
            z-index: 10;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }
        .cart-preview .dropped-image {
            width: 30px;
            z-index: 15;
        }
        #checkout-form label, #orders-form label {
            font-weight: bold;
            margin-bottom: 5px;
            display: block;
        }
        #checkout-form input[type="email"], #orders-form input {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        #proceed-to-checkout {
            padding: 10px 20px;
            background: #000;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        #proceed-to-checkout:hover {
            background: #333;
        }
        #payment-info {
            margin-top: 20px;
            padding: 15px;
            background: #f0f0f0;
            border-radius: 8px;
            display: none;
        }
        #payment-info img {
            max-width: 50px;
            margin-right: 10px;
        }
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 20px;
            background: white;
            box-shadow: 0 -2px 5px rgba(0,0,0,0.1);
        }
        .product-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        .product-item {
            width: 200px;
            text-align: center;
        }
        .product-item img {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        .product-item p {
            margin: 10px 0;
        }
        #contact-form input, #contact-form textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .order-item {
            padding: 15px;
            border-bottom: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <header>
        <img src="Bloom N Love logo.png" alt="Bloom N Love" id="logo">
        <nav>
            <ul>          
                <li><a href="#design-tshirt" onclick="showSection('design-tshirt')">Design T-Shirt</a></li>
                <li><a href="#cart-section" onclick="showSection('cart-section')">Cart</a></li>
                <li><a href="#handmade-crochet" onclick="showSection('handmade-crochet')">Handmade Crochet</a></li>
                <li><a href="#basket-bundles" onclick="showSection('basket-bundles')">Basket Bundles</a></li>
                <li><a href="#about" onclick="showSection('about')">About Us</a></li>
                <li><a href="#services" onclick="showSection('services')">Services</a></li>
                <li><a href="#contact" onclick="showSection('contact')">Contact</a></li>
                <li><a href="#orders" onclick="showSection('orders')">Orders</a></li>
            </ul>
        </nav>
    </header>

 <section id="design-tshirt">
        <h2>Design Your T-Shirt</h2>
        <div class="container">
            <div class="preview">
                <img id="tshirt-image" src="black_shirt.webp" alt="Custom T-Shirt">
                <img id="design-overlay" src="red_design.png" alt="Design Overlay" style="display: none;">
                <div id="dropped-images-container"></div>
                <div id="text-overlay" style="display: none;">Your Text Here</div>
            </div>
            <div class="customization">
                <label for="choose-quotes">Choose Quotes:</label>
                <select id="choose-quotes" onchange="updateText()">
                    <option value="">Select a Quote</option>
                    <option value="girlfriend">I Love My Girlfriend</option>
                    <option value="boyfriend">I Love My Boyfriend</option>
                    <option value="wife">I Love My Wife</option>
                    <option value="husband">I Love My Husband</option>
                </select>

<label for="design-color">Choose Design Color:</label>
                <select id="design-color" onchange="updateDesignColor()">
                    <option value="red_design.png">Red</option>
                    <option value="pinkdesign_copy.webp">Pink</option>
                    <option value="blue_design.png">Blue</option>
                    <option value="yellow_design.png">Yellow</option>
                </select>

 <div class="image-upload-box">
                    <div class="image-count">
                        <button class="image-count-btn active" data-count="1">1</button>
                        <button class="image-count-btn" data-count="2">2</button>
                        <button class="image-count-btn" data-count="3">3</button>
                    </div>
                    <label>Image Upload:</label>
                    <input type="file" id="image-upload" accept="image/*" multiple onchange="processMultipleImages()" style="display: none;">
                    <button class="upload-button" onclick="triggerImageUpload()">Select Image</button>
                </div>

   <div id="uploaded-images-container"></div>

<label for="custom-text">Enter Custom Text:</label>
                <input type="text" id="custom-text" placeholder="Your Text Here" oninput="updateText()">

<label>Choose Text Color:</label>
                <div class="color-choices-container">
                    <div class="color-choice" data-color="white" onclick="changeTextColor('white')"></div>
                    <div class="color-choice" data-color="black" onclick="changeTextColor('black')"></div>
                    <div class="color-choice" data-color="red" onclick="changeTextColor('red')"></div>
                    <div class="color-choice" data-color="pink" onclick="changeTextColor('pink')"></div>
                    <div class="color-choice" data-color="blue" onclick="changeTextColor('blue')"></div>
                    <div class="color-choice" data-color="gold" onclick="changeTextColor('gold')"></div>
                </div>

   <div style="text-align: center; margin-top: 20px;">
                    <button id="add-to-cart" onclick="addToCart()">Add to Cart</button>
                </div>
            </div>
        </div>
    </section>

 <section id="cart-section">
        <h2>Shopping Cart</h2>
        <div id="cart-items"></div>
        <button onclick="showSection('checkout-section')">Proceed to Checkout</button>
    </section>

 <section id="checkout-section">
        <h2>Checkout</h2>
        <div id="checkout-form">
            <p>Enter your email to receive order confirmation.</p>
            <label for="email">Email address</label>
            <input type="email" id="email" placeholder="Enter your email" required>
            <button id="proceed-to-checkout" onclick="proceedToPayment()">PROCEED TO CHECKOUT</button>
        </div>
        <div id="payment-info" style="display: none;">
            <h3>Payment Information</h3>
            <p>Guaranteed safe & secure checkout via:</p>
            <div>
                <img src="https://cdn-icons-png.flaticon.com/512/196/196578.png" alt="PayPal">
                <img src="https://cdn-icons-png.flaticon.com/512/196/196564.png" alt="Visa">
                <img src="https://cdn-icons-png.flaticon.com/512/196/196570.png" alt="Apple Pay">
                <img src="https://cdn-icons-png.flaticon.com/512/196/196566.png" alt="MasterCard">
                <img src="https://cdn-icons-png.flaticon.com/512/196/196572.png" alt="McAfee">
                <img src="https://cdn-icons-png.flaticon.com/512/196/196562.png" alt="American Express">
            </div>
            <p><span style="color: #4CAF50;">✓</span> Secure transaction</p>
        </div>
    </section>

 <section id="handmade-crochet">
        <h2>Handmade Crochet</h2>
        <p>Explore our collection of beautifully crafted crochet items, made with love and care.</p>
        <div class="product-grid">
            <div class="product-item">
                <img src="crochet_scarf.jpg" alt="Crochet Scarf">
                <p>Crochet Scarf - $25</p>
            </div>
            <div class="product-item">
                <img src="crochet_hat.jpg" alt="Crochet Hat">
                <p>Crochet Hat - $20</p>
            </div>
            <div class="product-item">
                <img src="crochet_blanket.jpg" alt="Crochet Blanket">
                <p>Crochet Blanket - $50</p>
            </div>
        </div>
    </section>

 <section id="basket-bundles">
        <h2>Basket Bundles</h2>
        <p>Discover our curated gift baskets, perfect for any occasion.</p>
        <div class="product-grid">
            <div class="product-item">
                <img src="love_basket.jpg" alt="Love Basket">
                <p>Love Basket - $35</p>
            </div>
            <div class="product-item">
                <img src="friendship_basket.jpg" alt="Friendship Basket">
                <p>Friendship Basket - $30</p>
            </div>
            <div class="product-item">
                <img src="family_basket.jpg" alt="Family Basket">
                <p>Family Basket - $45</p>
            </div>
        </div>
    </section>

<section id="about">
        <h2>About Us</h2>
        <p>At Bloom N Love, we’re passionate about creating unique, heartfelt gifts that bring joy to your loved ones. Founded in 2025, our small team combines creativity and craftsmanship to offer personalized T-shirts, handmade crochet items, and thoughtful basket bundles. We believe in the power of love and expression through every stitch and design.</p>
    </section>

 <section id="services">
        <h2>Services</h2>
        <ul>
            <li>Custom T-Shirt Design: Create your own unique apparel.</li>
            <li>Handmade Crochet: Bespoke items crafted with care.</li>
            <li>Basket Bundles: Curated gifts for any occasion.</li>
            <li>Shipping: Fast and reliable delivery to your doorstep.</li>
            <li>Customer Support: We’re here to help with any questions!</li>
        </ul>
    </section>

  <section id="contact">
    <h2>Contact Us</h2>
        <p>Have a question or want to place a custom order? Reach out to us!</p>
        <form id="contact-form" onsubmit="submitContact(event)">
            <label for="name">Name</label>
            <input type="text" id="name" placeholder="Your Name" required>
            <label for="email-contact">Email</label>
            <input type="email" id="email-contact" placeholder="Your Email" required>
            <label for="message">Message</label>
            <textarea id="message" placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

<section id="orders">
        <h2>Orders</h2>
        <div id="orders-list"></div>
    </section>

 <footer>
        <p>© 2025 Bloom N Love. All rights reserved.</p>
    </footer>

<script>
        // T-Shirt Customization Functions
        function updateText() {
            const quote = document.getElementById('choose-quotes').value;
            const customText = document.getElementById('custom-text').value;
            const textOverlay = document.getElementById('text-overlay');
            const designOverlay = document.getElementById('design-overlay');

            textOverlay.textContent = customText || (quote ? `I Love My ${quote.charAt(0).toUpperCase() + quote.slice(1)}` : "Your Text Here");
            textOverlay.style.display = 'block';
            designOverlay.style.display = quote ? 'block' : customText ? 'none' : 'none';
        }

        function updateDesignColor() {
            const designOverlay = document.getElementById('design-overlay');
            const selectedColor = document.getElementById('design-color').value;
            designOverlay.src = selectedColor;
            designOverlay.style.display = document.getElementById('choose-quotes').value ? 'block' : 'none';
        }

        function changeTextColor(color) {
            document.getElementById('text-overlay').style.color = color;
        }

        // Image Upload and Drag/Drop Functions
        let selectedImageCount = 1;
        let isDragging = false;
        let draggedImage = null;
        let initialX = 0;
        let initialY = 0;

        document.querySelectorAll('.image-count-btn').forEach(button => {
            button.addEventListener('click', function() {
                document.querySelectorAll('.image-count-btn').forEach(btn => btn.classList.remove('active'));
                this.classList.add('active');
                selectedImageCount = parseInt(this.getAttribute('data-count'));
                triggerImageUpload();
            });
        });

        function triggerImageUpload() {
            document.getElementById('image-upload').click();
        }

        function processMultipleImages() {
            const fileInput = document.getElementById('image-upload');
            const files = fileInput.files;
            const container = document.getElementById('uploaded-images-container');
            container.innerHTML = '';

            if (files.length > selectedImageCount) {
                alert(`Please upload a maximum of ${selectedImageCount} image${selectedImageCount > 1 ? 's' : ''}.`);
                fileInput.value = '';
                return;
            }

            Array.from(files).slice(0, selectedImageCount).forEach(file => {
                const formData = new FormData();
                formData.append("image_file", file);
                formData.append("size", "auto");

                fetch("https://api.remove.bg/v1.0/removebg", {
                    method: "POST",
                    headers: { "X-Api-Key": "tb1Kjhju4cZpzmdiFa5eRfHs" },
                    body: formData
                })
                .then(response => {
                    if (!response.ok) throw new Error('Background removal failed');
                    return response.blob();
                })
                .then(blob => {
                    const imageUrl = URL.createObjectURL(blob);
                    const imageBox = document.createElement("div");
                    imageBox.classList.add("image-box");
                    imageBox.onclick = () => dropImageOnPreview(imageUrl);

                    const img = document.createElement("img");
                    img.src = imageUrl;
                    imageBox.appendChild(img);

                    const removeBtn = document.createElement("button");
                    removeBtn.classList.add("remove-btn");
                    removeBtn.textContent = "X";
                    removeBtn.onclick = (e) => { e.stopPropagation(); removeImage(imageBox); };
                    imageBox.appendChild(removeBtn);

                    container.appendChild(imageBox);
                })
                .catch(error => {
                    console.error("Error:", error);
                    alert("Failed to process image. Please try again.");
                });
            });
        }

        function removeImage(imageBox) {
            imageBox.remove();
            const droppedImg = document.querySelector(`.dropped-image[data-src="${imageBox.querySelector('img').src}"]`);
            if (droppedImg) droppedImg.remove();
        }

        function dropImageOnPreview(imageUrl) {
            if (isDragging) {
                draggedImage.style.left = `${initialX}px`;
                draggedImage.style.top = `${initialY}px`;
                draggedImage.style.pointerEvents = 'none';
                isDragging = false;
                draggedImage = null;
                return;
            }

            const preview = document.querySelector('.preview');
            const rect = preview.getBoundingClientRect();
            const randomX = Math.random() * (rect.width - 100);
            const randomY = Math.random() * (rect.height - 100);

            const droppedImg = document.createElement('img');
            droppedImg.src = imageUrl;
            droppedImg.classList.add('dropped-image');
            droppedImg.dataset.src = imageUrl;
            droppedImg.style.left = `${randomX}px`;
            droppedImg.style.top = `${randomY}px`;
            droppedImg.style.position = 'absolute';
            droppedImg.style.maxWidth = '100px';
            droppedImg.style.height = 'auto';
            droppedImg.style.zIndex = '15';

            preview.querySelector('#dropped-images-container').appendChild(droppedImg);

            droppedImg.addEventListener('click', (e) => {
                if (!isDragging) {
                    isDragging = true;
                    draggedImage = droppedImg;
                    initialX = parseFloat(droppedImg.style.left) || randomX;
                    initialY = parseFloat(droppedImg.style.top) || randomY;
                    e.preventDefault();
                } else {
                    dropImageOnPreview(imageUrl);
                }
            });

            document.addEventListener('mousemove', handleDrag);
            document.addEventListener('mouseup', () => {
                if (isDragging) {
                    isDragging = false;
                    draggedImage = null;
                    document.removeEventListener('mousemove', handleDrag);
                }
            });
        }

        function handleDrag(e) {
            if (isDragging && draggedImage) {
                const preview = document.querySelector('.preview');
                const rect = preview.getBoundingClientRect();
                const newX = initialX + (e.clientX - rect.left - 50);
                const newY = initialY + (e.clientY - rect.top - 50);
                const maxX = rect.width - 100;
                const maxY = rect.height - 100;
                draggedImage.style.left = `${Math.max(0, Math.min(newX, maxX))}px`;
                draggedImage.style.top = `${Math.max(0, Math.min(newY, maxY))}px`;
            }
        }

        // Cart, Checkout, and Order Functions
        let cart = JSON.parse(localStorage.getItem('cart')) || [];
        let orders = JSON.parse(localStorage.getItem('orders')) || [];

        function addToCart() {
            const tshirtImage = document.getElementById('tshirt-image').src;
            const designOverlay = document.getElementById('design-overlay').src;
            const textOverlay = document.getElementById('text-overlay').textContent;
            const textColor = document.getElementById('text-overlay').style.color;
            const droppedImages = Array.from(document.querySelectorAll('.dropped-image')).map(img => ({
                src: img.src,
                left: img.style.left,
                top: img.style.top
            }));

            const hasDesign = document.getElementById('choose-quotes').value !== "" || 
                             document.getElementById('custom-text').value.trim() !== "" || 
                             droppedImages.length > 0;

            if (!hasDesign) {
                const confirm = window.confirm("Are you sure you want to proceed without a design?");
                if (!confirm) return;
            }

            const cartItem = {
                tshirtImage,
                designOverlay: hasDesign && document.getElementById('design-overlay').style.display === 'block' ? designOverlay : null,
                textOverlay: textOverlay !== "Your Text Here" ? textOverlay : null,
                textColor: textColor || 'white',
                droppedImages,
                price: 19.99,
                timestamp: new Date().toISOString()
            };

            cart.push(cartItem);
            localStorage.setItem('cart', JSON.stringify(cart));
            alert('T-Shirt added to cart!');
            showSection('cart-section');
            displayCart();
        }

        function displayCart() {
            const cartItems = document.getElementById('cart-items');
            cartItems.innerHTML = '';

            if (cart.length === 0) {
                cartItems.innerHTML = '<p>Your cart is empty.</p>';
                return;
            }

            cart.forEach((item, index) => {
                const div = document.createElement('div');
                div.classList.add('cart-item');

                const previewDiv = document.createElement('div');
                previewDiv.classList.add('cart-preview');

                const tshirtImg = document.createElement('img');
                tshirtImg.src = item.tshirtImage;
                previewDiv.appendChild(tshirtImg);

                if (item.designOverlay) {
                    const designImg = document.createElement('img');
                    designImg.src = item.designOverlay;
                    designImg.classList.add('design-overlay');
                    previewDiv.appendChild(designImg);
                }

                if (item.textOverlay) {
                    const textDiv = document.createElement('div');
                    textDiv.textContent = item.textOverlay;
                    textDiv.classList.add('text-overlay');
                    textDiv.style.color = item.textColor;
                    previewDiv.appendChild(textDiv);
                }

                item.droppedImages.forEach(imgData => {
                    const droppedImg = document.createElement('img');
                    droppedImg.src = imgData.src;
                    droppedImg.classList.add('dropped-image');
                    droppedImg.style.left = `${parseFloat(imgData.left) * (150 / 500)}px`;
                    droppedImg.style.top = `${parseFloat(imgData.top) * (150 / 500)}px`;
                    previewDiv.appendChild(droppedImg);
                });

                div.appendChild(previewDiv);

                div.innerHTML += `
                    <div>
                        <p>T-Shirt Color: ${item.tshirtImage.includes('white') ? 'White' : 'Black'}</p>
                        <p>Design: ${item.designOverlay ? item.designOverlay.split('/').pop() : 'None'}</p>
                        <p>Text: ${item.textOverlay || 'None'} (Color: ${item.textColor})</p>
                        <p>Custom Images: ${item.droppedImages.length > 0 ? 'Yes' : 'No'}</p>
                        <p>Price: $${item.price.toFixed(2)}</p>
                        <button onclick="removeFromCart(${index})">Remove</button>
                    </div>
                `;
                cartItems.appendChild(div);
            });
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            localStorage.setItem('cart', JSON.stringify(cart));
            displayCart();
        }

        function proceedToPayment() {
            const email = document.getElementById('email').value.trim();
            if (!email || !isValidEmail(email)) {
                alert('Please enter a valid email address.');
                return;
            }

            if (cart.length === 0) {
                alert('Your cart is empty!');
                return;
            }

            document.getElementById('payment-info').style.display = 'block';

            // Simulated Stripe Payment (replace with real Stripe integration)
            const orderId = `ORD-${Date.now()}`;
            const order = {
                id: orderId,
                items: [...cart],
                email: email,
                total: cart.reduce((sum, item) => sum + item.price, 0).toFixed(2),
                status: 'Processing',
                timestamp: new Date().toISOString()
            };

            orders.push(order);
            localStorage.setItem('orders', JSON.stringify(orders));

            // Simulated Stripe Payment
            console.log('Simulating Stripe payment for order:', order);
            
            // Real Stripe implementation (requires Stripe.js and backend):
            // const stripe = Stripe('YOUR_STRIPE_PUBLISHABLE_KEY');
            // stripe.redirectToCheckout({
            //     sessionId: 'session_id_from_backend', // Generated by backend
            // }).then(result => {
            //     if (result.error) alert(result.error.message);
            // });

            sendOrderConfirmationEmail(email, order);
            sendAdminNotification(order);

            alert('Payment processed successfully! Check your email for confirmation. This is a demo - no real payment occurred.');
            cart = [];
            localStorage.setItem('cart', JSON.stringify(cart));
            displayOrders();
            setTimeout(() => showSection('design-tshirt'), 2000);
        }

        function sendOrderConfirmationEmail(email, order) {
            // Simulated SendGrid email (replace with real API call)
            const subject = `Order Confirmation - ${order.id}`;
            const body = `
                <html>
                    <body>
                        <img src="https://yourdomain.com/Bloom_N_Love_logo.png" alt="Bloom N Love Logo" style="max-width: 200px;">
                        <p>Thank you for ordering from Bloom N Love!</p>
                        <p>Order ID: ${order.id}</p>
                        <p>Total: $${order.total}</p>
                        <p>Items: ${order.items.map(item => item.textOverlay || 'Custom T-Shirt').join(', ')}</p>
                        <p>Status: ${order.status}</p>
                        <p>Thank you for ordering. Shipment will be sent out 1-3 weeks. For any questions, email bloomnlove@gmail.com.</p>
                    </body>
                </html
                `;
            console.log(`Sending email to ${email}: Subject: ${subject}, Body: ${body}`);
            
            // Real SendGrid implementation (requires backend):
            // fetch('https://api.sendgrid.com/v3/mail/send', {
            //     method: 'POST',
            //     headers: {
            //         'Authorization': 'Bearer YOUR_SENDGRID_API_KEY',
            //         'Content-Type': 'application/json'
            //     },
            //     body: JSON.stringify({
            //         personalizations: [{ to: [{ email: email }], subject: subject }],
            //         from: { email: 'admin@bloomnlove.com', name: 'Bloom N Love' },
            //         content: [{ type: 'text/html', value: body }]
            //     })
            // }).then(response => response.json())
            //   .then(data => console.log('Email sent:', data))
            //   .catch(error => console.error('Error sending email:', error));
        }

 function sendAdminNotification(order) {
            // Simulated admin notification (replace with real API call)
            const adminEmail = 'admin@bloomnlove.com'; // Replace with your email
            const subject = `New Order Received - ${order.id}`;
            const body = `
                <html>
                <body>
                <img src="https://yourdomain.com/Bloom_N_Love_logo.png" alt="Bloom N Love Logo" style="max-width: 200px;">
                        <p>New order received!</p>
                        <p>Order ID: ${order.id}</p>
                        <p>Customer Email: ${order.email}</p>
                        <p>Total: $${order.total}</p>
                        <p>Items: ${order.items.map(item => item.textOverlay || 'Custom T-Shirt').join(', ')}</p>
                        <p>Status: ${order.status}</p>
                    </body>
                </html>
            `;
            console.log(`Sending email to ${adminEmail}: Subject: ${subject}, Body: ${body}`);
            
  // Real SendGrid implementation (requires backend, same as above but to adminEmail)
        }

 function displayOrders() {
            const ordersList = document.getElementById('orders-list');
            ordersList.innerHTML = '';

 if (orders.length === 0) {
                ordersList.innerHTML = '<p>No orders yet.</p>';
                return;
            }

  orders.forEach(order => {
                const div = document.createElement('div');
                div.classList.add('order-item');
                div.innerHTML = `
                    <p>Order ID: ${order.id}</p>
                    <p>Customer Email: ${order.email}</p>
                    <p>Total: $${order.total}</p>
                    <p>Items: ${order.items.map(item => item.textOverlay || 'Custom T-Shirt').join(', ')}</p>
  <p>Status: ${order.status}</p>
                    <p>Date: ${new Date(order.timestamp).toLocaleString()}</p>
                `;
  ordersList.appendChild(div);
            });
            }

function isValidEmail(email) {
            return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
        }

function showSection(sectionId) {
            const sections = ['design-tshirt', 'cart-section', 'checkout-section', 'handmade-crochet', 'basket-bundles', 'about', 'services', 'contact', 'orders'];
            sections.forEach(id => {
                document.getElementById(id).style.display = id === sectionId ? 'block' : 'none';
            });
            if (sectionId === 'cart-section') displayCart();
            if (sectionId === 'orders') displayOrders();
        }

function submitContact(event) {
            event.preventDefault();
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email-contact').value.trim();
            const message = document.getElementById('message').value.trim();

 if (!name || !isValidEmail(email) || !message) {
                alert('Please fill in all fields with valid information.');
                return;
            }

 alert('Thank you for your message! We’ll get back to you soon. (This is a demo - no real email is sent.)');
            document.getElementById('contact-form').reset();
        }

 // Initialize
        window.onload = () => {
            showSection('design-tshirt');
            if (cart.length > 0) displayCart();
            if (orders.length > 0) displayOrders();
 };
 </script>  
</body>
</html>
