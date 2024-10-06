# Calculator
<!DOCTYPE html>
<html>
  <head>
    <title>Calculator</title>
  </head>
  <body>
    <h1>Calculator</h1>
    
    <input type="number" id="num1" placeholder="Enter first number">
    <input type="number" id="num2" placeholder="Enter second number">
    
    <select id="operation">
      <option value="addition">Addition</option>
      <option value="subtraction">Subtraction</option>
      <option value="multiplication">Multiplication</option>
      <option value="division">Division</option>
    </select> 

    <button onclick="calculate()">Calculate</button>
    
    <h2 id="result"></h2> 

    <script>
      function calculate() {
        const num1 = parseFloat(document.getElementById('num1').value);
        const num2 = parseFloat(document.getElementById('num2').value);
        const operation = document.getElementById('operation').value;
        let result;

        
        switch (operation) {
          case 'addition':
            result = num1 + num2;
            break;
          case 'subtraction':
            result = num1 - num2;
            break;
          case 'multiplication':
            result = num1 * num2;
            break;
          case 'division':
            result = num2 !== 0 ? num1 / num2 : 'Cannot divide by zero.';
            break;
        }

        
        document.getElementById('result').innerText = `Result: ${result}`;
      }
    </script>
  </body>
</html>
