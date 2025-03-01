<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beyond</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Inter', sans-serif;
            background-color: #000;
            color: #fff;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            background-color: black;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        .navbar a {
            text-decoration: none;
            color: #fff;
            font-size: 18px;
            margin: 0 15px;
            cursor: pointer;
        }
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding-top: 80px;
            background: url('https://source.unsplash.com/1600x900/?luxury,lifestyle') no-repeat center center/cover;
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
            background-color: #ff0055;
            color: white;
        }
        .sign-up {
            background-color: transparent;
            border: 2px solid #ff0055;
            color: #ff0055;
        }
        .button:hover {
            transform: scale(1.1);
        }
        .section {
            padding: 100px 50px;
            text-align: center;
            background-color: #111;
        }
        .about, .membership, .achievements, .testimonials {
            background-color: #222;
        }
        .membership button {
            background-color: #ff0055;
            color: white;
            padding: 10px 25px;
            border-radius: 20px;
            font-size: 18px;
            cursor: pointer;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 50px;
        }
        .gallery img {
            width: 300px;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
        }
    </style>
    <script>
        function goToSignIn() {
            window.location.href = 'signin.html';
        }
        function goToSignUp() {
            window.location.href = 'signup.html';
        }
        function goToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }
    </script>
</head>
<body>
    <div class="navbar">
        <div class="logo"><h2>Beyond</h2></div>
        <div>
            <a onclick="goToSection('home')">Home</a>
            <a onclick="goToSection('about')">About Us</a>
            <a onclick="goToSection('achievements')">Achievements</a>
            <a onclick="goToSection('testimonials')">Testimonials</a>
            <a onclick="goToSection('membership')">Membership</a>
        </div>
    </div>
    <div class="hero" id="home">
        <h1>Beyond</h1>
        <p>Helping you break free from habits and achieve your goals through structured challenges and tracking.</p>
        <div class="auth-buttons">
            <button class="button sign-in" onclick="goToSignIn()">Log In</button>
            <button class="button sign-up" onclick="goToSignUp()">Get Started</button>
        </div>
    </div>
    <div class="gallery">
        <img src="https://source.unsplash.com/400x300/?success" alt="Success">
        <img src="https://source.unsplash.com/400x300/?goal" alt="Goal">
        <img src="https://source.unsplash.com/400x300/?motivation" alt="Motivation">
    </div>
    <div class="section about" id="about">
        <h2>About Us</h2>
        <p>Beyond is dedicated to helping individuals overcome personal challenges through structured goal setting and tracking.</p>
    </div>
    <div class="section achievements" id="achievements">
        <h2>Greatest Achievements</h2>
        <p>We've helped thousands of users reach their personal and professional goals.</p>
    </div>
    <div class="section testimonials" id="testimonials">
        <h2>What People Say</h2>
        <p>"Beyond changed my life! I finally overcame my biggest challenges and achieved my dreams." - User A</p>
        <p>"A game-changer for self-improvement! Highly recommend it to everyone." - User B</p>
    </div>
    <div class="section membership" id="membership">
        <h2>Membership</h2>
        <p>Join our community and gain access to exclusive challenges, personalized goal tracking, and expert guidance.</p>
        <button onclick="alert('Membership purchased!')">Buy Membership</button>
    </div>
</body>
</html>
