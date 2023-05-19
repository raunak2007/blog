---
title: Better Python 2D Iteration and Animations
toc: true
categories: [week34, tri3]
image: /images/javascript.png
badges: true
comments: true
author: Raunak Mondal
description: Working with 2D elements and working with animations
---
<head>
    <title>Projectile Motion Simulation</title>
    <style>
        canvas {
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <canvas id="canvas" width="800" height="400"></canvas>

    <script>
        // Get the canvas element and its context
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');

        // Set the initial position and velocity of the projectile
        let x = 50;
        let y = canvas.height / 2;
        let velocityX = 5;
        let velocityY = 0;
        const gravity = 0.2;

        // Keyboard event listeners
        document.addEventListener('keydown', function(event) {
            if (event.keyCode === 32) { // Space key
                velocityY = -7; // Adjust the vertical velocity to simulate a jump
            }
        });

        // Animation loop
        function draw(color) {
            // Clear the canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Update the position and velocity
            x += velocityX;
            y += velocityY;
            velocityY += gravity;

            // Draw the projectile
            ctx.beginPath();
            ctx.arc(x, y, 10, 0, 2 * Math.PI);
            ctx.fillStyle = color;
            ctx.fill();

            // Check for collision with the ground
            if (y > canvas.height - 10) {
                y = canvas.height - 10;
                velocityY = 0;
            }

            // Request the next animation frame
            requestAnimationFrame(draw);
        }

        // Start the animation loop
        draw('red');
    </script>
</body>

