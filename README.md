<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Analog Clock 3D UI/UX</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            perspective: 1000px;
            background-color: #f0f0f0;
        }

        .clock {
            width: 300px;
            height: 300px;
            position: relative;
            transform-style: preserve-3d;
            animation: rotateClock 60s linear infinite;
        }

        .clock .clock-face {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background-color: #f5f5dc; /* Cream color */
            position: absolute;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            transform: translateZ(-20px); /* Depth */
        }

        .clock .hour, .clock .minute, .clock .second {
            position: absolute;
            width: 50%;
            background-color: brown;
            top: 50%;
            transform-origin: 100%;
            transform: translateY(-50%) translateZ(10px); /* Depth */
        }

        .clock .hour {
            height: 6px;
        }

        .clock .minute {
            height: 4px;
        }

        .clock .second {
            height: 2px;
            background-color: red; /* Typically, the second hand is a different color */
        }

        @keyframes rotateClock {
            from {
                transform: rotateY(0);
            }
            to {
                transform: rotateY(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="clock">
        <div class="clock-face"></div>
        <div class="hour"></div>
        <div class="minute"></div>
        <div class="second"></div>
    </div>
</body>
</html>
