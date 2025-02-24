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


</html>
