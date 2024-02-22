<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic Drawing with Video</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        canvas {
            border: 1px solid black;
        }
        video {
            margin-top: 20px;
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <canvas id="myCanvas" width="400" height="400"></canvas>
    <video controls>
        <source src="path_to_your_video.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <script>
        const canvas = document.getElementById('myCanvas');
        const context = canvas.getContext('2d');

        context.fillStyle = 'red';
        context.fillRect(50, 50, 100, 100);

        context.strokeStyle = 'blue';
        context.lineWidth = 5;
        context.strokeRect(200, 200, 100, 100);

        context.beginPath();
        context.arc(300, 100, 50, 0, 2 * Math.PI);
        context.fillStyle = 'green';
        context.fill();
    </script>
</body>
</html>
