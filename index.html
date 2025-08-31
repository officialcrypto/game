<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Flappy Box</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(to bottom, #87CEEB, #4facfe);
      font-family: Arial, sans-serif;
    }

    .game {
      width: 400px;
      height: 600px;
      background: #cce7ff;
      overflow: hidden;
      position: relative;
      border: 3px solid #222;
      border-radius: 15px;
    }

    #player {
      width: 40px;
      height: 40px;
      background: gold;
      border-radius: 50%;
      position: absolute;
      left: 50px;
      top: 250px;
    }

    .pipe {
      position: absolute;
      width: 60px;
      background: linear-gradient(to bottom, #28a745, #218838);
    }

    .pipe.top {
      top: 0;
    }

    .pipe.bottom {
      bottom: 0;
    }

    #score {
      position: absolute;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 24px;
      font-weight: bold;
      color: #fff;
      text-shadow: 2px 2px 3px rgba(0,0,0,0.5);
    }
  </style>
</head>
<body>
  <div class="game">
    <div id="score">0</div>
    <div id="player"></div>
  </div>

  <script>
    const game = document.querySelector(".game");
    const player = document.getElementById("player");
    const scoreDisplay = document.getElementById("score");

    let playerY = 250;
    let gravity = 2;
    let isGameOver = false;
    let score = 0;

    document.addEventListener("keydown", () => {
      if (!isGameOver) {
        playerY -= 50; // jump
      }
    });

    function createPipe() {
      if (isGameOver) return;

      let pipeHeight = Math.floor(Math.random() * 200) + 100;
      let gap = 150;

      let topPipe = document.createElement("div");
      topPipe.classList.add("pipe", "top");
      topPipe.style.height = pipeHeight + "px";
      topPipe.style.right = "-60px";

      let bottomPipe = document.createElement("div");
      bottomPipe.classList.add("pipe", "bottom");
      bottomPipe.style.height = 600 - pipeHeight - gap + "px";
      bottomPipe.style.right = "-60px";

      game.appendChild(topPipe);
      game.appendChild(bottomPipe);

      let moveInterval = setInterval(() => {
        if (isGameOver) {
          clearInterval(moveInterval);
          return;
        }

        let topRight = parseInt(window.getComputedStyle(topPipe).getPropertyValue("right"));
        if (topRight > 400) {
          game.removeChild(topPipe);
          game.removeChild(bottomPipe);
          clearInterval(moveInterval);
        } else {
          topPipe.style.right = topRight + 2 + "px";
          bottomPipe.style.right = topRight + 2 + "px";

          // collision detection
          let playerRect = player.getBoundingClientRect();
          let topRect = topPipe.getBoundingClientRect();
          let bottomRect = bottomPipe.getBoundingClientRect();

          if (
            (playerRect.right > topRect.left &&
             playerRect.left < topRect.right &&
             playerRect.top < topRect.bottom) ||
            (playerRect.right > bottomRect.left &&
             playerRect.left < bottomRect.right &&
             playerRect.bottom > bottomRect.top)
          ) {
            gameOver();
          }

          // scoring
          if (topRight === 200) {
            score++;
            scoreDisplay.textContent = score;
          }
        }
      }, 20);
    }

    function gameOver() {
      isGameOver = true;
      alert("Game Over! Score: " + score);
      window.location.reload();
    }

    function gameLoop() {
      if (isGameOver) return;

      playerY += gravity;
      if (playerY < 0) playerY = 0;
      if (playerY > 560) {
        gameOver();
      }
      player.style.top = playerY + "px";
      requestAnimationFrame(gameLoop);
    }

    setInterval(createPipe, 2000);
    gameLoop();
  </script>
</body>
</html>

