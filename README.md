<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SHADOW X</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #ff0000;
            text-align: center;
            padding: 50px;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            background-color: #222;
            padding: 20px;
            border-radius: 10px;
            transition: background-color 0.3s ease;
        }
        input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: none;
            border-radius: 5px;
        }
        input[type="submit"] {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.2s ease;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
        .download-button {
            display: none;
        }
        .logged-in .download-button {
            display: block;
            margin-top: 20px;
        }
        .download-button a {
            display: inline-block;
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.2s ease;
        }
        .download-button a:hover {
            background-color: #0056b3;
        }
        .floating-window {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #444;
            padding: 20px;
            border-radius: 10px;
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        h1 {
            font-size: 2.5rem;
            text-transform: uppercase;
            color: #ff0000;
            text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000, 0 0 30px #ff0000;
            animation: neon 1s ease-in-out infinite alternate;
        }
        @keyframes neon {
            0% { opacity: 0.8; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>SHADOW X</h1>
        <form action="verification.php" method="POST">
            <label for="password">Mot de passe :</label>
            <input type="password" id="password" name="password" placeholder="Entrez le mot de passe" required>
            <input type="submit" value="Se connecter">
        </form>
        <div class="download-button">
            <a href="https://fs5.dupload.xyz/cgi-bin/dl.cgi/4s3vkj6vokqpuxvr4j64hi6yg3d7yosmrcdvfbhxegl5urizmqngrhq/Free_Fire_32_Bit.apk" target="_blank">TÉLÉCHARGER LE MOD</a>
        </div>
        <div class="floating-window">
            <p>Votre mot de passe expirera dans 24 heures.</p>
            <button onclick="closeFloatingWindow()">OK</button>
            <audio id="notification-sound" src="notification.mp3"></audio>
        </div>
    </div>
    <script>
        const passwordInput = document.getElementById('password');
        const container = document.querySelector('.container');
        const floatingWindow = document.querySelector('.floating-window');
        const notificationSound = document.getElementById('notification-sound');

        container.addEventListener('submit', (e) => {
            e.preventDefault();
            const enteredPassword = passwordInput.value;
            if (enteredPassword === 'shadow2024') {
                container.classList.add('logged-in');
                setTimeout(() => {
                    floatingWindow.style.display = 'block';
                    notificationSound.play(); // Play the notification sound
                }, 1000); // Show the floating window after 1 second (24 hours in real-world scenario)
            }
        });

        function closeFloatingWindow() {
            floatingWindow.style.display = 'none';
        }
    </script>
</body>
</html>
