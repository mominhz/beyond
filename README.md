<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beyond</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/framer-motion/10.12.6/framer-motion.umd.min.js"></script>
    <style>
        body {
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #007bff;
            color: white;
            font-family: 'Poppins', sans-serif;
            text-align: center;
            position: relative;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        h1 {
            font-size: 4rem;
            font-weight: bold;
        }
        .button {
            margin-top: 20px;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 25px;
            border: none;
            cursor: pointer;
        }
        .sign-in {
            background-color: white;
            color: #007bff;
        }
        .sign-up {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }
        .arrow {
            position: absolute;
            bottom: 50px;
            font-size: 24px;
            animation: bounce 1.5s infinite;
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body>
    <div class="container" id="landing">
        <h1>Beyond</h1>
        <div class="arrow">⬇ Click to Continue ⬇</div>
    </div>
    <div class="container" id="auth" style="display: none;">
        <button class="button sign-in">Sign In</button>
        <button class="button sign-up">Sign Up</button>
    </div>
    <script>
        document.querySelector('.arrow').addEventListener('click', () => {
            document.getElementById('landing').style.display = 'none';
            document.getElementById('auth').style.display = 'flex';
        });
    </script>
</body>
</html>
