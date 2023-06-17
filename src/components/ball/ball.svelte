<script>
    import { onMount } from 'svelte';
  
    let balls = [];
  
    onMount(() => {
      const numBalls = 10;
  
      // Generate random initial positions and velocities for the balls
      for (let i = 0; i < numBalls; i++) {
        balls.push({
          x: Math.random() * window.innerWidth,
          y: Math.random() * window.innerHeight,
          vx: Math.random() * 4.5 - 1.5, // Random velocity between -2.5 and 2.5
          vy: Math.random() * 4.5 - 1.5,
          radius: Math.random() * 30 + 10, // Random radius between 10 and 40
        });
      }
  
      // Update ball positions
      const update = () => {
        balls.forEach((ball) => {
          ball.x += ball.vx;
          ball.y += ball.vy;
  
          // Check for collision with window boundaries
          if (ball.x + ball.radius > window.innerWidth || ball.x - ball.radius < 0) {
            ball.vx *= -1; // Reverse the x velocity
          }
  
          if (ball.y + ball.radius > window.innerHeight || ball.y - ball.radius < 0) {
            ball.vy *= -1; // Reverse the y velocity
          }
        });
  
        // Trigger Svelte's reactive update
        balls = [...balls];
  
        requestAnimationFrame(update);
      };
  
      // Start the animation
      requestAnimationFrame(update);
    });
  </script>
  
  <style>
    .ball {
      position: absolute;
      width: 50px;
      height: 50px;
      pointer-events: none;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/d/d3/Soccerball.svg'); /* Replace with your soccer ball image URL */
      background-size: cover;
    }
  </style>
  
  <div>
    {#each balls as ball, i (ball.x)}
      <div
        class="ball"
        style="
          left: {ball.x - ball.radius}px;
          bottom: {(ball.y - ball.radius)/3.5}px;
        "
      ></div>
    {/each}
  </div>
  