
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Testing</title>
    <style>
        /* General body styles */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #ADD8E6; /* Light blue background */
        }

        /* Container for the main message */
        .confession-container {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        h1 {
            font-size: 3rem;
            color: #ff6f61; /* Soft red */
            margin-bottom: 20px;
        }

        p {
            font-size: 1.5rem;
            color: #555;
            width: 80%;
            max-width: 800px;
            margin: 20px auto;
            line-height: 1.6;
        }

        /* Button styles */
        .love-button {
            background-color: #ff6f61;
            color: white;
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            margin-top: 20px;
            transition: background-color 0.3s ease;
        }

        .love-button:hover {
            background-color: #ff4c41;
        }

        /* Heart animation */
        .heart {
            font-size: 4rem;
            color: #ff4c41;
            animation: heartbeat 1.5s ease-in-out infinite;
        }

        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }

        /* Reveal message with fade-in effect */
        #reveal-message {
            opacity: 0;
            margin-top: 40px;
            transition: opacity 2s ease-in;
        }

        #reveal-message.visible {
            opacity: 1;
        }

        /* Final message container with delayed fade-in */
        .final-message {
            font-size: 2rem;
            color: #ff6f61;
            margin-top: 40px;
            opacity: 0;
            transition: opacity 2s ease-in;
        }

        .final-message.visible {
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="confession-container">
        <h1>Try lang ito</h1>

        <!-- Reveal button -->
        <button class="love-button" onclick="revealMessage()">Click (Wala itong virus trust me)</button>
        
        <!-- Hidden message to be revealed -->
        <div id="reveal-message">
            <p>
                Told ya
                ![rikiroll](https://github.com/user-attachments/assets/009037a9-b5c7-4ef2-8128-85de410bae32)
            </p>
          
            <div class="final-message">Will you go out with me?</div>
        </div>
    </div>

    <script>
        function revealMessage() {
            // Slowly fade in the hidden message
            var revealDiv = document.getElementById('reveal-message');
            revealDiv.classList.add('visible');

            // Show the final message after a short delay
            setTimeout(function() {
                document.querySelector('.final-message').classList.add('visible');
            }, 2000);
        }
    </script>
</body>
</html>
