<!DOCTYPE html>
<html>
<head>
    <title>Chaos Land</title>
    <style>
        /* Full-page chaos */
        body, html {
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: black;
            color: white;
            font-family: 'Courier New', monospace;
        }

        /* Flashing text */
        h1 {
            font-size: 5em;
            animation: flash 1s infinite alternate;
        }

        p {
            font-size: 2em;
            animation: colorShift 3s infinite alternate;
        }

        /* Keyframes for animation */
        @keyframes flash {
            0% { color: red; }
            50% { color: yellow; }
            100% { color: blue; }
        }

        @keyframes colorShift {
            0% { color: green; }
            50% { color: purple; }
            100% { color: cyan; }
        }

        /* Moving background */
        #background {
            position: fixed;
            top: 0;
            left: 0;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, red, blue, green, yellow, purple);
            animation: spin 20s linear infinite;
            z-index: -1;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div id="background"></div>
    <h1>Welcome to Chaos Land!</h1>
    <p>Embrace the surreal.</p>

    <script>
        // Randomly generate colorful squares
        function createChaos() {
            const chaos = document.createElement('div');
            chaos.style.position = 'absolute';
            chaos.style.width = '50px';
            chaos.style.height = '50px';
            chaos.style.backgroundColor = '#' + Math.floor(Math.random()*16777215).toString(16);
            chaos.style.top = Math.random() * window.innerHeight + 'px';
            chaos.style.left = Math.random() * window.innerWidth + 'px';
            chaos.style.borderRadius = '50%';
            document.body.appendChild(chaos);

            // Remove after animation
            setTimeout(() => chaos.remove(), 5000);
        }

        // Generate chaos continuously
        setInterval(createChaos, 100);
    </script>
</body>
</html># Agcampbell-
My personal website .
