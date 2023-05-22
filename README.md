# calculator
# HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="styles4.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" readonly>
        <div class="keypad">
            <button onclick="appendToResult('7')">7</button>
            <button onclick="appendToResult('8')">8</button>
            <button onclick="appendToResult('9')">9</button>
            <button onclick="clearResult()">C</button>
            <button onclick="appendToResult('4')">4</button>
            <button onclick="appendToResult('5')">5</button>
            <button onclick="appendToResult('6')">6</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendToResult('1')">1</button>
            <button onclick="appendToResult('2')">2</button>
            <button onclick="appendToResult('3')">3</button>
            <button onclick="appendToResult('+')">+</button>
            <button onclick="appendToResult('0')">0</button>
            <button onclick="appendToResult('.')">.</button>
            <button onclick="appendToResult('-')">-</button>
            <button onclick="appendToResult('*')">*</button>
            <button onclick="appendToResult('/')">/</button>
        </div>
    </div>

    <script src="script4.js"></script>
</body>
</html>

# css
body, button, input {
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.calculator {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    padding: 20px;
    max-width: 400px;
    width: 100%;
}

input {
    border: none;
    background-color: #f5f5f5;
    padding: 10px;
    width: 100%;
    margin-bottom: 10px;
    font-size: 20px;
}

.keypad {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 10px;
}

button {
    background-color: #333;
    color: #fff;
    padding: 10px;
    border: none;
    text-align: center;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}

# JAVASCRIPT
function appendToResult(value) {
    document.getElementById("result").value += value;
}

function clearResult() {
    document.getElementById("result").value = "";
}

function calculateResult() {
    var result = eval(document.getElementById("result").value);
    document.getElementById("result").value = result;
}


