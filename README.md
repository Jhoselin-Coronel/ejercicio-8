
<html>
<head>
  <title>Convergencia de la serie</title>
</head>
<body>
  <h1>Demostración de convergencia de la serie</h1>

  <h2>Resultados</h2>
  <p>Suma para n = 50: <span id="sum_a"></span></p>
  <p>Suma para n = 500: <span id="sum_b"></span></p>
  <p>Suma para n = 5000: <span id="sum_c"></span></p>
  <p>Valor de ln(2): <span id="ln2"></span></p>

  <script>
    // a) n = 50
    let n = Array.from({length: 51}, (_, i) => i);
    let series_a = n.map(i => 1 / ((2*i+1) * (2*i+2)));
    let sum_a = series_a.reduce((acc, val) => acc + val, 0);
    document.getElementById('sum_a').textContent = sum_a.toFixed(6);

    // b) n = 500
    n = Array.from({length: 501}, (_, i) => i);
    let series_b = n.map(i => 1 / ((2*i+1) * (2*i+2)));
    let sum_b = series_b.reduce((acc, val) => acc + val, 0);
    document.getElementById('sum_b').textContent = sum_b.toFixed(6);

    // c) n = 5000
    n = Array.from({length: 5001}, (_, i) => i);
    let series_c = n.map(i => 1 / ((2*i+1) * (2*i+2)));
    let sum_c = series_c.reduce((acc, val) => acc + val, 0);
    document.getElementById('sum_c').textContent = sum_c.toFixed(6);

    document.getElementById('ln2').textContent = Math.log(2).toFixed(6);
  </script>
</body>
</html>
