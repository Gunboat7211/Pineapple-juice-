<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love Message</title>
    <style>
        /* Basic Page Styling */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #fbeaff;
            font-family: Arial, sans-serif;
            overflow: hidden;
            position: relative;
        }

        /* Container Styling */
        .container {
            text-align: center;
            position: relative;
            z-index: 1;
        }

        /* Message Styling */
        h1 {
            color: #e91e63;
            font-size: 2em;
            display: none;
        }

        /* Heart Styling */
        .heart {
            font-size: 4em;
            color: #ff8a80;
            display: none;
            margin-top: 10px;
            animation: popHeart 1s forwards ease-in-out;
        }

        /* Button Styling */
        button {
            padding: 10px 20px;
            font-size: 1em;
            background-color: #ff8a80;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #ff5252;
        }

        /* Floating Hearts */
        .floating-heart {
            position: absolute;
            color: #ff8a80;
            font-size: 2em;
            opacity: 0;
            animation: floatUp 5s ease-in-out infinite;
        }

        /* Animation for Pop-Up Heart */
        @keyframes popHeart {
            0% {
                transform: scale(0);
            }
            50% {
                transform: scale(1.5);
            }
            100% {
                transform: scale(1);
            }
        }

        /* Floating Animation */
        @keyframes floatUp {
            0% {
                transform: translateY(0);
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 id="loveMessage"></h1>
        <div class="heart" id="heart">❤️</div>
        <button id="loveButton">Click for a Surprise</button>
    </div>

    <!-- JavaScript for displaying message and floating hearts -->
    <script>
        // Function to display the love message, main heart, and floating hearts
        function displayLoveMessage() {
            const message = "I love you PINEAPPLE 🍍 I always did and I always will.";
            const loveMessageElement = document.getElementById("loveMessage");
            const heartElement = document.getElementById("heart");

            // Set the text and display the elements
            loveMessageElement.textContent = message;
            loveMessageElement.style.display = "block";
            heartElement.style.display = "block";

            // Create floating hearts
            for (let i = 0; i < 20; i++) {
                const floatingHeart = document.createElement("div");
                floatingHeart.classList.add("floating-heart");
                floatingHeart.textContent = "❤️";
                
                // Random position and delay for each floating heart
                floatingHeart.style.left = `${Math.random() * 100}vw`;
                floatingHeart.style.animationDelay = `${Math.random() * 5}s`;
                
                document.body.appendChild(floatingHeart);

                // Remove heart from DOM after animation completes
                floatingHeart.addEventListener("animationend", () => {
                    floatingHeart.remove();
                });
            }
        }

        // Attach event listener after content loads
        document.addEventListener("DOMContentLoaded", function() {
            document.getElementById("loveButton").addEventListener("click", displayLoveMessage);
        });
    </script>
</body>
</html>
