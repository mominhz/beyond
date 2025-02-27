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
            background-color: #ffffff;
            color: #333;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            background-color: white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
        }
        .navbar a {
            text-decoration: none;
            color: #333;
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
            background: url('https://source.unsplash.com/1600x900/?nature,freedom') no-repeat center center/cover;
            color: white;
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
            background-color: #0066ff;
            color: white;
        }
        .sign-up {
            background-color: transparent;
            border: 2px solid #0066ff;
            color: #0066ff;
        }
        .button:hover {
            transform: scale(1.1);
        }
        .section {
            padding: 100px 50px;
            text-align: center;
        }
        .about, .membership {
            background-color: #f5f5f7;
        }
        .membership button {
            background-color: #28a745;
            color: white;
            padding: 10px 25px;
            border-radius: 20px;
            font-size: 18px;
            cursor: pointer;
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
            <a onclick="goToSection('membership')">Membership</a>
        </div>
    </div>
    <div class="hero" id="home">
        <h1>Beyond</h1>
        <p>Helping you break free from habits and achieve your goals through structured challenges and tracking.</p>
        <div class="auth-buttons">
            <button class="button sign-in" onclick="goToSignIn()">Sign In</button>
            <button class="button sign-up" onclick="goToSignUp()">Sign Up</button>
        </div>
    </div>
    <div class="section about" id="about">
        <h2>About Us</h2>
        <p>Beyond is dedicated to helping individuals overcome personal challenges through structured goal setting and tracking.</p>
    </div>
    <div class="section membership" id="membership">
        <h2>Membership</h2>
        <p>Join our community and gain access to exclusive challenges, personalized goal tracking, and expert guidance.</p>
        <button onclick="alert('Membership purchased!')">Buy Membership</button>
    </div>
</body>
</html>

