<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ครบ 1 เดือนแล้วนะ 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Kanit', sans-serif;
      text-align: center;
      background: linear-gradient(to bottom, #ffe6eb, #ffcce0);
      color: #c2185b;
      margin: 0;
      padding: 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }

    h1 {
      font-size: 1.4rem;
      padding: 0 20px;
      line-height: 1.8;
      font-weight: 600;
    }

    p {
      font-size: 1.2rem;
      max-width: 600px;
      line-height: 1.6;
      margin: 10px auto;
      color: #8e2c50;
    }

    .buttons {
      margin-top: 30px;
    }

    button {
      font-size: 1.5rem;
      padding: 12px 28px;
      margin: 10px;
      border: none;
      cursor: pointer;
      transition: 0.3s ease;
      border-radius: 12px;
      font-family: 'Kanit', sans-serif;
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
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>
  <!-- หน้าแรก -->
  <div id="page1">
    <h1>🎉 เราครบ 1 เดือนแล้วนะคะทราย 💕<br>เจมีเรื่องอยากจะบอก 🥺</h1>
    <button class="next" id="nextButton">ต่อเลยนะคะ 💌</button>
  </div>

  <!-- หน้าที่สอง -->
  <div id="page2" class="hidden">
    <h1>📝 ทุกครั้งที่เบบี๋เป็นตัวเอง เจได้เห็นคนที่น่ารักที่สุดในโลกกกก 💖<br>การกระทำเปิ่นๆ ความซุ่มซ่าม แม้กระทั่งตอนงอแงตุ๊บป่องๆ มันทำให้เจรู้ว่า...</h1>
    <p>...เจอยากจะเป็นคนที่ทรายพึ่งพาได้ในทุกเรื่องเลย ไม่ว่าเวลานี้หรืออนาคตอันใกล้ 💞</p>
    <button class="next" id="toQuestion">ต่ออีกนิดนะคะ</button>
  </div>

  <!-- หน้าที่สาม -->
  <div id="page3" class="hidden">
    <h1>💘 เป็นแฟนกับเจได้ไหมครับ 🥺<br>เจมีความสุขมากๆ ที่ได้ใช้เวลากับทราย 💖</h1>
    <div class="buttons">
      <button class="yes" id="yesButton">Yes 💗</button>
      <button class="no" id="noButton">No 😢</button>
    </div>
  </div>

  <script>
    const nextButton = document.getElementById("nextButton");
    const toQuestion = document.getElementById("toQuestion");
    const page1 = document.getElementById("page1");
    const page2 = document.getElementById("page2");
    const page3 = document.getElementById("page3");
    const yesButton = document.getElementById("yesButton");
    const noButton = document.getElementById("noButton");

    let yesSize = 1.5;

    nextButton.addEventListener("click", () => {
      page1.classList.add("hidden");
      page2.classList.remove("hidden");
    });

    toQuestion.addEventListener("click", () => {
      page2.classList.add("hidden");
      page3.classList.remove("hidden");
    });

    noButton.addEventListener("click", function () {
      yesSize += 0.4;
      yesButton.style.fontSize = yesSize + "rem";
    });

    yesButton.addEventListener("click", function () {
      document.body.innerHTML =
        "<h1>💖 เย้! ทรายกดแล้วววววว! เปลี่ยนใจไม่ได้แล้วนะครับ 💖<br>เราคบกันมา 1 เดือนแล้ว ขอบคุณที่อยู่ด้วยกันนะเบบี๋ 🥰</h1><img src='your-cat-image.png' alt='Cat' width='200'>";
    });
  </script>
</body>
</html>