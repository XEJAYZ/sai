<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ครบ 1 เดือนแล้วนะ 💖</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      text-align: center;
      background-color: #ffdde1;
      color: #d63384;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    h1 {
      font-size: 2rem;
      padding: 0 20px;
    }
    .buttons {
      margin-top: 20px;
    }
    button {
      font-size: 1.5rem;
      padding: 10px 20px;
      margin: 10px;
      border: none;
      cursor: pointer;
      transition: 0.3s;
      border-radius: 10px;
    }
    .yes {
      background-color: #28a745;
      color: white;
    }
    .no {
      background-color: #dc3545;
      color: white;
    }
    .next {
      background-color: #007bff;
      color: white;
    }
    .hidden {
      display: none;
    }
    img {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <!-- หน้าแรก -->
  <div id="page1">
    <h1>🎉 เราครบ 1 เดือนแล้วนะ 💕<br>ชั้นมีเรื่องอยากจะขอจริงๆ สักทีนะคะ 😊</h1>
    <button class="next" id="nextButton">ต่อเลยนะคะ 💌</button>
  </div>

  <!-- หน้าที่สอง -->
  <div id="page2" class="hidden">
    <h1>💘 เป็นแฟนกับเจได้ไหมครับ<br>เจอยู่โดยไม่มีทรายไม่ได้เลย 🥺</h1>
    <div class="buttons">
      <button class="yes" id="yesButton">Yes 💗</button>
      <button class="no" id="noButton">No 😢</button>
    </div>
  </div>

  <script>
    const nextButton = document.getElementById("nextButton");
    const page1 = document.getElementById("page1");
    const page2 = document.getElementById("page2");
    const yesButton = document.getElementById("yesButton");
    const noButton = document.getElementById("noButton");

    let yesSize = 1.5;

    nextButton.addEventListener("click", () => {
      page1.classList.add("hidden");
      page2.classList.remove("hidden");
    });

    noButton.addEventListener("click", function () {
      yesSize += 0.5;
      yesButton.style.fontSize = yesSize + "rem";
    });

    yesButton.addEventListener("click", function () {
      document.body.innerHTML =
        "<h1>💖 เย้! ทรายตอบตกลงแล้วววววว! 💖<br>เราครบ 1 เดือนแล้วนะคะ ขอบคุณที่อยู่ด้วยกันเสมอ เจจะดูแลทรายให้ดีที่สุดเลยนะคะ 🥰</h1><img src='your-cat-image.png' alt='Cat' width='200'>";
    });
  </script>
</body>
</html>
