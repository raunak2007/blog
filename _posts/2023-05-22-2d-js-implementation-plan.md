---
title: Plan of 2D Animations
toc: true
categories: [week34, tri3]
image: /images/javascript.png
badges: true
comments: true
author: Raunak Mondal
description: Plan of 2D Animations
---
## Integration of 2D Animation Concepts for Projectile Motion of a Red Ball

To create a 2D animation of projectile motion for a red ball using JavaScript and HTML, I will guide you through the following steps:

1. **HTML Structure**: Let's start by setting up the basic HTML structure of the page.

\`\`\`html
<!DOCTYPE html>
<html>
<head>
    <title>Projectile Motion Animation</title>
    <style>
        #canvas {
            position: relative;
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <div id="canvas"></div>

    <script src="script.js"></script>
</body>
</html>
\`\`\`

2. **JavaScript**: Now, let's create a JavaScript file (e.g., \`script.js\`) and include it in the HTML file using the \`<script>\` tag.

\`\`\`javascript
// Define variables for ball properties
var canvas = document.getElementById("canvas");
var context = canvas.getContext("2d");
var x = 50; // Initial x position
var y = canvas.height - 50; // Initial y position
var vx = 5; // Initial x velocity
var vy = 0; // Initial y velocity
var gravity = 0.2; // Gravity value
var isJumping = false; // Track if the ball is jumping

// Function to draw the ball
function drawBall() {
    context.clearRect(0, 0, canvas.width, canvas.height);
    context.beginPath();
    context.arc(x, y, 20, 0, 2 * Math.PI, false);
    context.fillStyle = "red";
    context.fill();
    context.closePath();
}

// Function to update the ball's position
function updateBall() {
    vy += gravity; // Apply gravity
    x += vx; // Update x position
    y += vy; // Update y position

    // Check if the ball hits the ground
    if (y + 20 > canvas.height) {
        y = canvas.height - 20;
        vy *= -0.8; // Reverse and reduce y velocity for bounce effect
        isJumping = false;
    }

    drawBall(); // Draw the ball at the updated position
}

// Keyboard event listener
document.addEventListener("keydown", function(event) {
    if (event.key === " " && !isJumping) { // Spacebar to jump
        vy = -8; // Set initial y velocity for the jump
        isJumping = true;
    }
});

// Animation loop
function animate() {
    requestAnimationFrame(animate);
    updateBall();
}

// Start the animation
animate();
\`\`\`

3. **CSS Styling**: We can also add CSS styles to the \`<style>\` tag or an external CSS file to define the appearance of the canvas.

\`\`\`css
#canvas {
    position: relative;
    border: 1px solid black;
}
\`\`\`

4. **Testing**: You can now open the HTML file in a web browser, and you should see a canvas element with a red ball. Press the spacebar to make the ball jump, and observe the projectile motion.

By following these steps, you will be able to integrate 2D animation concepts into a \`<script>\` tag inside an HTML file to display the projectile motion of a red ball using keyboard actions.

