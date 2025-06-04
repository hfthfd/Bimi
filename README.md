# Bimi<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Billin Zadania</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f9f9f9;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }
    .card {
      background: white;
      border-radius: 10px;
      padding: 20px;
      margin-bottom: 15px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .card h3 {
      margin-top: 0;
    }
    button {
      background: #3b82f6;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:disabled {
      background: #9ca3af;
    }
    #points {
      font-weight: bold;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <h1>🎉 Program nagród Billin</h1>
  <div id="points">Twoje punkty: <span id="pointsValue">0</span></div>

  <div class="card">
    <h3>📝 Zostaw recenzję aplikacji Billin w Google Play</h3>
    <p>Po wykonaniu zadania kliknij przycisk poniżej.</p>
    <button onclick="completeTask(this, 10)">Wykonane ✅ (+10 pkt)</button>
  </div>

  <div class="card">
    <h3>📣 Udostępnij Billin na Instagramie</h3>
    <p>Opublikuj story z linkiem lub screenem aplikacji.</p>
    <button onclick="completeTask(this, 15)">Wykonane ✅ (+15 pkt)</button>
  </div>

  <div class="card">
    <h3>👫 Poleć aplikację znajomym</h3>
    <p>Wyślij link do aplikacji co najmniej 3 osobom.</p>
    <button onclick="completeTask(this, 20)">Wykonane ✅ (+20 pkt)</button>
  </div>

  <script>
    let points = 0;

    function completeTask(button, reward) {
      if (!button.disabled) {
        points += reward;
        document.getElementById("pointsValue").innerText = points;
        button.disabled = true;
        button.innerText = "Zaliczone! ✅";
      }
    }
  </script>
</body>
</html>
