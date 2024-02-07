<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f8e0e0; /* Light pink background */
            text-align: center;
            margin: 50px;
        }

        h1 {
            color: #cc0000; /* Dark red text color */
            font-size: 36px;
            margin-bottom: 20px;
        }

        #container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 70vh;
        }

        #yesButton, #noButton {
            padding: 15px 30px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
            border-radius: 10px;
            border: none;
            outline: none;
            transition: font-size 0.5s; /* Added transition property here */
        }

        #yesButton {
            background-color: #ff6666; /* Light red button */
            color: white;
        }

        #noButton {
            background-color: #ff9999; /* Light pink button */
            color: #cc0000; /* Dark red text color */
        }

        #hoorayContainer {
            display: none;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            background-color: #f0a5c4; /* Yellow background */
            border-radius: 10px;
            margin-top: 50px;
        }

        #hoorayText {
            font-size: 24px;
            color: #cc0000; /* Dark red text color */
        }
    </style>
</head>
<body>
    <h1>Will You Be My Valentine?</h1>
    <h1>👉👈</h1>
    <div id="container">
        <button id="yesButton" onclick="showHooray()">Yes</button>
        <button id="noButton" onclick="moveNoButton()">No</button>
    </div>

    <div id="hoorayContainer">
        <p id="hoorayText">YIPPEEE! 🎉 You're the Binoo to my Toopie! Happy Valentine's Day baby!</p>
    </div>

    <script>
        let yesButtonSize = 18; // Initial font size of the Yes button

        function showHooray() {
            // Hide buttons and show hooray container
            document.getElementById("container").style.display = "none";
            document.getElementById("hoorayContainer").style.display = "flex";
        }

        function moveNoButton() {
            // Move the No button to a random position
            const button = document.getElementById("noButton");
            const maxX = window.innerWidth - button.offsetWidth;
            const maxY = window.innerHeight - button.offsetHeight;
            const newX = Math.floor(Math.random() * maxX);
            const newY = Math.floor(Math.random() * maxY);

            button.style.position = "absolute";
            button.style.left = `${newX}px`;
            button.style.top = `${newY}px`;

            // Increase font size of Yes button
            yesButtonSize += 10;
            document.getElementById("yesButton").style.fontSize = `${yesButtonSize}px`;
        }
    </script>
</body>
</html>
