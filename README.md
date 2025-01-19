<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For Sabiha</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom, #ff9a9e, #fecfef);
      overflow: hidden;
    }
    .container {
      width: 100vw;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      transition: transform 1s ease-in-out;
    }
    .slide {
      width: 100vw;
      height: 100vh;
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }
    .slide.active {
      display: flex;
    }
    h1 {
      font-size: 2.5rem;
      color: #ff4d6d;
    }
    p {
      font-size: 1.5rem;
      color: #555;
      margin: 20px 0;
    }
    .heart {
      position: relative;
      width: 100px;
      height: 90px;
      cursor: pointer;
      margin: 20px 0;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 150px;
      background: #ff4d6d;
      border-radius: 50%;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
    }
    .heart::after {
      left: 0;
    }
    .heart:hover::before,
    .heart:hover::after {
      background: #ff99aa;
    }
    .btn {
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #ff4d6d;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.3s ease;
    }
    .btn:hover {
      background-color: #ff6f80;
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Slide 1 -->
    <div class="slide active" id="slide1">
      <h1>Welcome, Sabiha!</h1>
      <p>This journey is specially made for you ❤️</p>
      <p><b>Next Step:</b> Click the heart to proceed!</p>
      <div class="heart" onclick="nextSlide(1)"></div>
    </div>

    <!-- Slide 2 -->
    <div class="slide" id="slide2">
      <h1>Shayari for You ❤️</h1>
      <p>"चुपके से दिल में उतर जाओ,<br> सांसों में खुशबू बनकर बस जाओ।"</p>
      <p><b>Next Step:</b> Click the heart to see the next message!</p>
      <div class="heart" onclick="nextSlide(2)"></div>
    </div>

    <!-- Slide 3 -->
    <div class="slide" id="slide3">
      <h1>Just for You, Sabiha!</h1>
      <p>“तुमसे मिलना मेरी तकदीर थी,<br> लेकिन तुमसे बात करना मेरी ख्वाहिश है।”</p>
      <p><b>Next Step:</b> Click the heart to go to the final request!</p>
      <div class="heart" onclick="nextSlide(3)"></div>
    </div>

    <!-- Slide 4 -->
    <div class="slide" id="slide4">
      <h1>बात करो, सबीहा ❤️</h1>
      <p>“आपकी चुप्पी मेरे दिल को तोड़ रही है।<br> कृपया बात कीजिए, मुझे खुशी मिलेगी।”</p>
      <p>End of the journey! Please say yes to talk!</p>
    </div>
  </div>

  <script>
    function nextSlide(currentSlide) {
      document.getElementById(`slide${currentSlide}`).classList.remove('active');
      const next = document.getElementById(`slide${currentSlide + 1}`);
      if (next) {
        next.classList.add('active');
      }
    }
  </script>
</body>
</html>
