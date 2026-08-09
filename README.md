<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>For Bukki 🦋</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            overflow: hidden;
            font-family: Arial, sans-serif;

            background:
                linear-gradient(
                    rgba(255, 170, 200, 0.25),
                    rgba(170, 210, 255, 0.25)
                ),
                linear-gradient(135deg, #ffd6e7, #c9e9ff);

            display: flex;
            justify-content: center;
            align-items: center;

            color: #5b365d;
        }

        /* Main Card */

        .container {
            width: 90%;
            max-width: 430px;

            text-align: center;

            padding: 35px 20px;

            border-radius: 30px;

            background: rgba(255, 255, 255, 0.55);

            backdrop-filter: blur(12px);

            box-shadow:
                0 15px 40px rgba(80, 50, 90, 0.2);

            animation: appear 1.5s ease;

            z-index: 10;
        }

        /* Butterfly */

        .butterfly {
            font-size: 70px;

            animation:
                butterflyMove 3s infinite ease-in-out,
                flutter 0.8s infinite alternate;
        }

        h1 {
            font-size: 43px;

            margin: 10px 0;

            color: #a84d88;

            animation: glow 2s infinite alternate;
        }

        .subtitle {
            font-size: 18px;

            line-height: 1.7;

            margin: 15px 0 25px;
        }

        button {
            border: none;

            padding: 14px 28px;

            border-radius: 30px;

            font-size: 17px;

            cursor: pointer;

            color: white;

            background: linear-gradient(
                45deg,
                #c76db4,
                #8c70d8
            );

            font-weight: bold;

            box-shadow: 0 5px 15px rgba(120, 70, 140, 0.3);

            transition: 0.3s;
        }

        button:hover {
            transform: scale(1.08);
        }

        #message {
            display: none;

            margin-top: 25px;

            font-size: 18px;

            line-height: 1.8;

            animation: fadeIn 1s ease;
        }

        /* Flying Birds & Butterflies */

        .flying {
            position: fixed;

            bottom: -50px;

            font-size: 30px;

            pointer-events: none;

            z-index: 2;

            animation: fly linear forwards;
        }

        /* Clouds */

        .cloud {
            position: fixed;

            font-size: 60px;

            opacity: 0.35;

            animation: cloudMove 25s linear infinite;
        }

        .cloud1 {
            top: 10%;
            left: -100px;
        }

        .cloud2 {
            top: 25%;
            left: -200px;

            animation-delay: 8s;
        }

        /* Animations */

        @keyframes appear {
            from {
                opacity: 0;

                transform:
                    translateY(50px)
                    scale(0.9);
            }

            to {
                opacity: 1;

                transform:
                    translateY(0)
                    scale(1);
            }
        }

        @keyframes butterflyMove {

            0%, 100% {
                transform:
                    translateX(-10px)
                    rotate(-5deg);
            }

            50% {
                transform:
                    translateX(10px)
                    rotate(5deg);
            }
        }

        @keyframes flutter {

            from {
                transform: rotate(-5deg);
            }

            to {
                transform: rotate(5deg);
            }
        }

        @keyframes glow {

            from {
                text-shadow:
                    0 0 5px #ffffff;
            }

            to {
                text-shadow:
                    0 0 20px #e7a7d5;
            }
        }

        @keyframes fadeIn {

            from {
                opacity: 0;

                transform:
                    translateY(15px);
            }

            to {
                opacity: 1;

                transform:
                    translateY(0);
            }
        }

        @keyframes fly {

            0% {
                transform:
                    translateY(0)
                    translateX(0)
                    rotate(0deg);

                opacity: 0;
            }

            10% {
                opacity: 1;
            }

            50% {
                transform:
                    translateY(-50vh)
                    translateX(80px)
                    rotate(10deg);
            }

            100% {
                transform:
                    translateY(-115vh)
                    translateX(-100px)
                    rotate(-15deg);

                opacity: 0;
            }
        }

        @keyframes cloudMove {

            from {
                transform: translateX(0);
            }

            to {
                transform: translateX(120vw);
            }
        }

        /* Mobile */

        @media (max-width: 480px) {

            .container {
                width: 92%;

                padding: 30px 18px;
            }

            h1 {
                font-size: 36px;
            }

            .butterfly {
                font-size: 60px;
            }

            .subtitle {
                font-size: 16px;
            }

            #message {
                font-size: 16px;
            }
        }
    </style>
</head>

<body>

    <!-- Animated Clouds -->

    <div class="cloud cloud1">☁️</div>
    <div class="cloud cloud2">☁️</div>


    <!-- Main Content -->

    <div class="container">

        <div class="butterfly">
            🦋
        </div>

        <h1>
            Hey Bukki! 🌸
        </h1>

        <p class="subtitle">

            ANUSHREE D/O Ganapathi NAik and Rathna... ✨

            <br><br>

            Some people make ordinary
            moments feel special. 😊

        </p>

        <button onclick="showMessage()">
            Tap Here ✨
        </button>

        <div id="message">

            <p>

                Bukki 🌷

                <br><br>

                Like butterflies in a garden,
                some people simply make
                everything around them
                more beautiful. 🦋

                <br><br>

                And you're one of those people. ✨

                <br><br>

                <strong>
                    Stay as wonderful as you are. 🌸
                </strong>

            </p>

        </div>

    </div>


    <script>

        function showMessage() {

            document.getElementById("message")
                .style.display = "block";

            // Create birds and butterflies

            for (let i = 0; i < 20; i++) {

                setTimeout(createFlyingObject, i * 150);

            }

        }


        function createFlyingObject() {

            const object =
                document.createElement("div");

            object.className = "flying";

            const objects = [
                "🦋",
                "🦋",
                "🐦",
                "🐦",
                "🦋",
                "🕊️"
            ];

            object.innerHTML =
                objects[
                    Math.floor(
                        Math.random() *
                        objects.length
                    )
                ];

            object.style.left =
                Math.random() * 100 + "vw";

            object.style.animationDuration =
                (5 + Math.random() * 5) + "s";

            object.style.fontSize =
                (25 + Math.random() * 25) + "px";

            document.body.appendChild(object);

            setTimeout(() => {

                object.remove();

            }, 10000);

        }


        // Continuous flying birds and butterflies

        setInterval(
            createFlyingObject,
            1200
        );

    </script>

</body>
</html>
