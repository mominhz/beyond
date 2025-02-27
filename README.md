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
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
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
    </style>
</head>
<body>
    <div class="container" id="landing">
        <h1 id="title">Beyond</h1>
    </div>
    <div class="container" id="auth" style="display: none;">
        <button class="button sign-in">Sign In</button>
        <button class="button sign-up">Sign Up</button>
    </div>
    <script>
        setTimeout(() => {
            document.getElementById('landing').style.display = 'none';
            document.getElementById('auth').style.display = 'flex';
        }, 2000);
    </script>
</body>
</html>
