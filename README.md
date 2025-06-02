# Starwars
Starwars history
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Starfield</title>
  <style>
    body {
      margin: 0;
      background: black;
      overflow: hidden;
    }

    .star {
      position: absolute;
      background: white;
      border-radius: 50%;
      width: 2px;
      height: 2px;
      animation: moveDown linear infinite;
    }

    @keyframes moveDown {
      0% {
        transform: translateY(0);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <script>
    const starCount = 200;

    for (let i = 0; i < starCount; i++) {
      const star = document.createElement('div');
      star.className = 'star';
      star.style.left = `${Math.random() * 100}vw`;
      star.style.top = `${Math.random() * -100}vh`;
      star.style.animationDuration = `${2 + Math.random() * 4}s`;
      star.style.opacity = Math.random();
      document.body.appendChild(star);
    }
  </script>
</body>
</html>
