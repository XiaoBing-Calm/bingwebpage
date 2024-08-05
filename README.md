<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>静</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #000;
            overflow: hidden;
            font-family: 'Arial', sans-serif;
        }

        .glitch {
            position: relative;
            color: #00ffea;
            font-size: 10vw;
            font-weight: bold;
            text-transform: uppercase;
            animation: glitch 1s infinite;
        }

        .glitch::before,
        .glitch::after {
            content: "静";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: inherit;
        }

        .glitch::before {
            left: 2px;
            text-shadow: -2px 0 red;
            clip: rect(44px, 450px, 56px, 0);
            animation: glitch 2s infinite linear alternate-reverse;
        }

        .glitch::after {
            left: -2px;
            text-shadow: -2px 0 blue;
            clip: rect(85px, 450px, 140px, 0);
            animation: glitch 1.5s infinite linear alternate-reverse;
        }

        @keyframes glitch {
            0% {
                text-shadow: 2px 2px #00ffea, -2px -2px #00ffea;
            }
            25% {
                text-shadow: -2px -2px #00ffea, 2px 2px #00ffea;
            }
            50% {
                text-shadow: 2px -2px #00ffea, -2px 2px #00ffea;
            }
            75% {
                text-shadow: -2px 2px #00ffea, 2px -2px #00ffea;
            }
            100% {
                text-shadow: 2px 2px #00ffea, -2px -2px #00ffea;
            }
        }
    </style>
</head>
<body>
    <div class="glitch">静</div>
</body>
</html>
