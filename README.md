<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proposal Game</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            margin: 10px;
            cursor: pointer;
        }
        #noButton {
            position: relative;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Do you like me?</h1>
        <button id="yesButton">Yes</button>
        <button id="noButton">No</button>
        <p id="message"></p>
    </div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const message = document.getElementById('message');

        yesButton.addEventListener('click', () => {
            message.textContent = "Yay! I'm so glad to hear that! ❤️";
        });

        noButton.addEventListener('click', () => {
            // Move the "No" button to a random position
            const randomX = Math.random() * (window.innerWidth - 150); // 150 is the button width
            const randomY = Math.random() * (window.innerHeight - 50); // 50 is the button height
            noButton.style.position = 'absolute';
            noButton.style.left = `${randomX}px`;
            noButton.style.top = `${randomY}px`;
        });
    </script>
</body>
</html>