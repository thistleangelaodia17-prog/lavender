# lavender
optional
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Pulsating Glitter Heart</title>
  <style>
    body {
      background-color: black;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }

    .heart {
      position: relative;
      width: 100px;
      height: 90px;
      background: darkviolet;
      transform: rotate(-45deg);
      animation: pulse 1s infinite alternate, glitter 0.2s infinite;
      box-shadow: 0 0 10px violet, 0 0 20px purple;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 90px;
      background: inherit;
      border-radius: 50%;
    }

    .heart::before {
      top: -50px;
      left: 0;
    }

    .heart::after {
      left: 50px;
      top: 0;
    }

    @keyframes pulse {
      0% {
        transform: scale(1) rotate(-45deg);
        background: #4B0082;
        box-shadow: 0 0 10px #8A2BE2;
      }
      100% {
        transform: scale(1.2) rotate(-45deg);
        background: #DA70D6;
        box-shadow: 0 0 20px #D8BFD8;
      }
    }

    @keyframes glitter {
      0%, 100% {
        filter: brightness(1.2);
      }
      50% {
        filter: brightness(1.5);
      }
    }
  </style>
</head>
<body>
  <div class="heart"></div>
  <audio autoplay loop>
    <source src="the-one-that-got-away.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
</body>
</html>
