<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beyond - Achieve Your Best</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }
        body {
            background-color: #f8f8f8;
            color: #333;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 80px;
            background: #fff;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }
        .navbar a {
            text-decoration: none;
            color: #333;
            font-size: 18px;
            margin: 0 15px;
            font-weight: 600;
        }
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?motivation,health') no-repeat center center/cover;
        }
        .hero h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 20px;
        }
        .hero p {
            font-size: 1.5rem;
            max-width: 600px;
        }
        .auth-buttons {
            display: flex;
            gap: 20px;
            margin-top: 30px;
        }
        .button {
            padding: 15px 40px;
            font-size: 18px;
            border-radius: 30px;
            border: none;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s ease;
        }
        .sign-in {
            background-color: #007AFF;
            color: white;
        }
        .sign-up {
            background-color: transparent;
            border: 2px solid #007AFF;
            color: #007AFF;
        }
        .button:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="navbar">
        <div class="logo"><h2>Beyond</h2></div>
        <div>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#features">Features</a>
            <a href="#testimonials">Testimonials</a>
            <a href="#membership">Join Now</a>
        </div>
    </div>
    <div class="hero" id="home">
        <h1>Beyond</h1>
        <p>Helping you break free from distractions and achieve your best self through structured goals and tracking.</p>
        <div class="auth-buttons">
            <button class="button sign-in">Log In</button>
            <button class="button sign-up">Get Started</button>
        </div>
    </div>
</body>
</html>

