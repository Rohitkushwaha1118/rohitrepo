<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <title>श्रद्धांजलि निमंत्रण</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      background: url('https://www.transparenttextures.com/patterns/beige-paper.png');
      font-family: 'Georgia', serif;
      margin: 0;
      padding: 0;
      color: #3e2f2f;
    }

    .container {
      max-width: 800px;
      margin: 30px auto;
      text-align: center;
    }

    input[type="text"] {
      padding: 10px;
      width: 300px;
      font-size: 18px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      font-size: 18px;
      margin-left: 10px;
      background-color: #8b0000;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .card {
      display: none;
      margin-top: 30px;
      background-color: #fffaf5;
      border: 2px solid #bfa67a;
      padding: 40px;
      border-radius: 16px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      position: relative;
    }

    .card::before {
      content: "";
      position: absolute;
      top: -20px;
      left: -20px;
      right: -20px;
      bottom: -20px;
      border: 3px double #bfa67a;
      border-radius: 20px;
      z-index: -1;
    }

    .om {
      font-size: 60px;
      color: #b30000;
      margin-bottom: 10px;
    }

    h1 {
      font-size: 28px;
      color: #8b0000;
      margin-bottom: 10px;
      font-weight: bold;
    }

    h2 {
      font-size: 24px;
      margin: 10px 0;
      color: #4b2e2e;
    }

    .line {
      border-top: 2px dashed #bfa67a;
      margin: 20px 0;
    }

    .details, .family {
      font-size: 18px;
      line-height: 1.8;
      padding: 0 10px;
    }

    .highlight {
      color: #8b0000;
      font-weight: bold;
    }

    .footer {
      margin-top: 30px;
      font-style: italic;
      color: #555;
    }

    .guest-name {
      font-size: 20px;
      margin-top: 10px;
      margin-bottom: 20px;
      color: #5a2d2d;
    }
  </style>
</head>
<body>

  <div class="container">
    <h2>अतिथि का नाम दर्ज करें:</h2>
    <input type="text" id="nameInput" placeholder="Example: Rohit Kushwaha">
    <button onclick="generateCard()">कार्ड दिखाएँ</button>

    <div class="card" id="card">
      <div class="om"> " ॐ शान्तिः "</div>
      <h1>श्रद्धांजलि सभा में सादर आमंत्रण</h1>

      <div class="guest-name">
        🙏 प्रिय आदरणीय&nbsp<b><span id="guestName">अतिथि</span></b>&nbspजी,
      </div>
      
      <div class="line"></div>
      
      <h2>स्व. श्रीमती राधिका देवी</h2>
      <p>(पति स्व. श्री रामनाथ सिंह, निवासी – मथौली)</p>
      
      <div class="details">
        <p>दिनांक <span class="highlight">14 जून 2025</span> को वे इस नश्वर संसार को त्याग कर परमात्मा में विलीन हो गईं।</p>
        <p>उनकी आत्मा की शांति हेतु श्रद्धांजलि सभा का आयोजन किया गया है।</p>

        <p><span class="highlight">📅 दिनांक:</span> 28 जून 2025 (शनिवार)</p>
        <p><span class="highlight">📍 स्थान:</span> मथौली गाँव, बसाव कला, बक्सर</p>
      </div>

      <div class="line"></div>

      <div class="family">
        <p>शोक संतप्त परिवार:</p>
        <p>श्री गुप्तेश्वर सिंह&nbsp;&nbsp;&amp;&nbsp;&nbsp;श्री संतोष सिंह (पुत्र)</p>
        <p>एवं सम्पूर्ण <b>कुशवाहा</b> परिवार</p>
      </div>

      <div class="footer">
        <p>आपकी उपस्थिति हमारे लिए संबल एवं दिवंगत आत्मा के लिए सच्ची श्रद्धांजलि होगी।</p>
      </div>
    </div>
  </div>

  <script>
    function generateCard() {
      const name = document.getElementById("nameInput").value.trim();
      if (name === "") {
        alert("कृपया नाम दर्ज करें।");
        return;
      }

      document.getElementById("guestName").innerText = name;
      document.getElementById("card").style.display = "block";
    }
  </script>

</body>
</html>
