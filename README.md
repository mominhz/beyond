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
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #0066ff;
            color: white;
            font-family: 'Inter', sans-serif;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: absolute;
            width: 100%;
        }
        h1 {
            font-size: 5rem;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        .arrow {
            position: absolute;
            bottom: 50px;
            font-size: 24px;
            cursor: pointer;
            animation: bounce 1.5s infinite;
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        .auth {
            display: none;
            flex-direction: column;
            gap: 20px;
            animation: fadeIn 1s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
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
            background-color: white;
            color: #0066ff;
        }
        .sign-up {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }
        .button:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="container" id="landing">
        <h1>Beyond</h1>
        <div class="arrow" id="arrow">⬇ Click to Continue ⬇</div>
    </div>
    <div class="container auth" id="auth">
        <button class="button sign-in">Sign In</button>
        <button class="button sign-up">Sign Up</button>
    </div>
    <script>
        document.getElementById('arrow').addEventListener('click', () => {
            document.getElementById('landing').style.display = 'none';
            document.getElementById('auth').style.display = 'flex';
        });
    </script>
</body>
</html>

