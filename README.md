<!DOCTYPE html>
<html>
<head>
  <title>My Calculator</title>
</head>
<body>
  <h1>My Calculator 🧮</h1>

  <input id="num1" type="number" placeholder="First number">
  <input id="num2" type="number" placeholder="Second number">

  <br><br>

  <button onclick="calculate('+')">+</button>
  <button onclick="calculate('-')">−</button>
  <button onclick="calculate('*')">×</button>
  <button onclick="calculate('/')">÷</button>

  <h2 id="result">Result: </h2>

  <script>
    function calculate(operator) {
      let a = Number(document.getElementById("num1").value);
      let b = Number(document.getElementById("num2").value);
      let answer;

      if (operator === '+') answer = a + b;
      if (operator === '-') answer = a - b;
      if (operator === '*') answer = a * b;
      if (operator === '/') {
        answer = b === 0 ? "Cannot divide by zero" : a / b;
      }

      document.getElementById("result").textContent = "Result: " + answer;
    }
  </script>
</body>
</html># my-first-calculator
