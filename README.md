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
      font-size: 1rem;
      padding: 0 10px;
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
    <h1>🎉 เราครบ 1 เดือนแล้วนะคะทราย 💕<br>ชั้นมีเรื่องอยากจะบอก 🥺 </h1>
    <button class="next" id="nextButton">ต่อเลยนะคะ 💌</button>
  </div>

  <!-- หน้าที่สอง (ข้อความที่คุณจะเขียนเอง) -->
  <div id="page2" class="hidden">
    <h1>📝  ทุกครั้งที่เบบี๋เป็นตัวเองชั้นได้เห็นคนที่น่ารักที่สุดในโลกกกกกเลย 💖<br>การกระทำเปิ่นๆ การพูด ความซุ่มซ่าม ทุกอย่างที่เป็นแก แม้กระทั้งตอนที่แกร้องงอแงตุ๊บป่องๆ มันทำให้ชั้นรู้ว่าควรพูดออกไป</h1>
    <p>ตอนนี้เป็นยังไงอีกในอนาคตอันใกล้นี้ ชั้นก็อยากจะเป็นคนที่แก สามารถพึ่งพาได้  </p>
    <button class="next" id="toQuestion">ต่ออีกนิดนะคะ </button>
  </div>

  <!-- หน้าที่สาม (คำขอเป็นแฟน) -->
  <div id="page3" class="hidden">
    <h1>💘 เป็นแฟนกับเจได้ไหมครับ<br>ชั้นมีความสุขมากๆที่ได้ใช้เวลากับแก 🥺</h1>
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
      yesSize += 0.5;
      yesButton.style.fontSize = yesSize + "rem";
    });

    yesButton.addEventListener("click", function () {
      document.body.innerHTML =
        "<h1>💖 เย้! เบบี๋กดแล้วววววว! เปลี่ยนใจไม่ได้แล้วนะครับ 💖<br>เราคบกันมา 1 เดือนแล้วนะคะ ขอบคุณที่อยู่ด้วยกันนะเบบี๋</h1><img src='your-cat-image.png' alt='Cat' width='200'>";
    });
  </script>
</body>
</html>
