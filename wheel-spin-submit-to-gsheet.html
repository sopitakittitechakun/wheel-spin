
<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <title>กงล้อลุ้นโชค 10/20</title>
  <style>
    body {
      font-family: sans-serif;
      background: #fff3e0;
      text-align: center;
    }

    #wheel-container {
      position: relative;
      width: 300px;
      margin: 30px auto;
    }

    #wheel {
      width: 100%;
      transition: transform 4s ease-out;
    }

    #arrow {
      width: 0;
      height: 0;
      border-left: 20px solid transparent;
      border-right: 20px solid transparent;
      border-bottom: 30px solid red;
      position: absolute;
      top: -30px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 10;
    }

    #spinBtn {
      margin-top: 20px;
      padding: 12px 30px;
      font-size: 18px;
      background: #f4511e;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    #result {
      margin-top: 20px;
      font-size: 24px;
      color: #d84315;
    }

    input[type="tel"] {
      padding: 10px;
      font-size: 18px;
      width: 220px;
      margin-top: 10px;
      border: 2px solid #ff7043;
      border-radius: 8px;
    }
  </style>
</head>
<body>

<h1>📲 กรอกเบอร์ ลุ้นรางวัล 10 หรือ 20 บาท!</h1>

<input type="tel" id="phoneInput" placeholder="กรอกเบอร์โทร" maxlength="10"><br>
<button id="spinBtn" disabled>หมุนเลย!</button>

<div id="wheel-container">
  <div id="arrow"></div>
  <canvas id="wheel" width="300" height="300"></canvas>
</div>

<div id="result"></div>

<script>
  const canvas = document.getElementById("wheel");
  const ctx = canvas.getContext("2d");
  const prizes = ["10", "20"];
  const anglePerSlice = 360 / prizes.length;

  function drawWheel() {
    for (let i = 0; i < prizes.length; i++) {
      let angle = (anglePerSlice * i) * Math.PI / 180;
      ctx.beginPath();
      ctx.moveTo(150, 150);
      ctx.arc(150, 150, 140, angle, angle + anglePerSlice * Math.PI / 180);
      ctx.fillStyle = i % 2 === 0 ? "#fdd835" : "#ffb74d";
      ctx.fill();
      ctx.save();
      ctx.translate(150, 150);
      ctx.rotate(angle + (anglePerSlice * Math.PI / 180) / 2);
      ctx.textAlign = "right";
      ctx.fillStyle = "#000";
      ctx.font = "bold 24px sans-serif";
      ctx.fillText(prizes[i], 130, 10);
      ctx.restore();
    }
  }

  drawWheel();

  let currentRotation = 0;
  const spinBtn = document.getElementById("spinBtn");
  const phoneInput = document.getElementById("phoneInput");

  phoneInput.addEventListener("input", () => {
    spinBtn.disabled = !(phoneInput.value.length >= 9);
  });

  function sendToGoogleSheet(phone, prize) {
    fetch("https://script.google.com/macros/s/AKfycbx0nHaNcDqSMV9yyQL_x2BCSeOsZHR82M5FpW21DeVyvEfcsSrGCw0r4FMGQrKAKF28WQ/exec", {
      method: "POST",
      body: JSON.stringify({ phone: phone, reward: prize }),
      headers: {
        "Content-Type": "application/json"
      }
    })
    .then(res => console.log("✅ บันทึกไป Google Sheet แล้ว"))
    .catch(err => console.error("❌ เกิดข้อผิดพลาด:", err))
  }
  spinBtn.onclick = function () {
    const phone = phoneInput.value;
    if (!phone || phone.length < 9) {
      alert("กรุณากรอกเบอร์ให้ถูกต้อง");
      return;
    }

    const randomIndex = Math.floor(Math.random() * prizes.length);
    const baseRotation = 360 * 5;
    const targetRotation = 360 - (randomIndex * anglePerSlice + anglePerSlice / 2);
    const totalRotation = baseRotation + targetRotation;
    currentRotation += totalRotation;

    canvas.style.transform = `rotate(${currentRotation}deg)`;

    spinBtn.disabled = true;
    setTimeout(() => {
      const prize = prizes[randomIndex];
      document.getElementById("result").textContent =
        `🎉 เบอร์ ${phone} ได้รับ ${prize} บาท!`;
      sendToGoogleSheet(phone, prize);
      spinBtn.disabled = false;
    }, 4200);
  };
</script>

</body>
</html>
