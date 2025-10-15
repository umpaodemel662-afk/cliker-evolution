<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Clicker com Evoluções</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    button {
      padding: 10px 20px;
      font-size: 18px;
    }
    .stats {
      margin-top: 20px;
      font-size: 20px;
    }
  </style>
</head>
<body>
  <h1>Clicker com Evoluções</h1>
  <button onclick="clicar()">Clique aqui!</button>
  <button onclick="evoluir()">Evoluir</button>

  <div class="stats">
    <p>Clicks: <span id="clicks">0</span></p>
    <p>Evolução: <span id="evolucao">0</span> / 10</p>
    <p>Clicks por clique: <span id="clickPower">1</span></p>
  </div>

  <script>
    let clicks = 0;
    let evolucao = 0;
    let clickPower = 1;

    function clicar() {
      clicks += clickPower;
      atualizar();
    }

    function evoluir() {
      if (evolucao < 10) {
        evolucao++;
        clickPower++;
        atualizar();
      } else {
        alert("Você já atingiu o nível máximo de evolução!");
      }
    }

    function atualizar() {
      document.getElementById("clicks").textContent = clicks;
      document.getElementById("evolucao").textContent = evolucao;
      document.getElementById("clickPower").textContent = clickPower;
    }
  </script>
</body>
</html>

