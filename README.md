<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>เราก็ครบ 1เดือนแล้วนะ ชั้นมีเรื่องที่อยากจะขอแบบจริงๆจังๆสักที</title>
  <style>
    body {
      font-family: Arial, sans-serif;
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
  </style>
</head>
<body>
  <!-- หน้าแรก -->
  <div id="page1">
    <h1>เราก็ครบ 1 เดือนแล้วนะ<br>ชั้นมีเรื่องที่อยากจะขอแบบจริงๆจังๆสักที</h1>
    <button class="next" id="nextButton">ถัดไป</button>
  </div>

  <!-- หน้าที่สอง -->
  <div id="page2" class="hidden">
    <h1>เป็นแฟนกันนะ</h1>
    <div class="buttons">
      <button class="yes" id="yesButton">Yes</button>
      <button class="no" id="noButton">No</button>
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
        "<h1>เย้! ทรายกดแล้วววววววววววววววว! เป็นแฟนกับเค้าครบ1เดือนแล้วนะคะ ❤️</h1><img src='your-cat-image.png' alt='Cat' width='200'>";
    });
  </script>
</body>
</html>
