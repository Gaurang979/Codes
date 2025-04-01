<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: black;
        }
        .calculator {
            background: dodgerblue;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }
        input {
            width: 100%;
            height: 50px;
            font-size: 1.5em;
            text-align: right;
            margin-bottom: 10px;
            border: none;
            padding: 5px;
        }
        button {
            width: 23%;
            height: 50px;
            font-size: 1.2em;
            margin: 5px;
            border: none;
            cursor: pointer;
            background: black;
            color: white;
            border-radius: 5px;
        }
        button:hover {
            background: grey;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <br>
        <button onclick="clearDisplay()">C</button>
        <button onclick="appendValue('/')">/</button>
        <button onclick="appendValue('*')">*</button>
        <button onclick="appendValue('-')">-</button>
        <br>
        <button onclick="appendValue('7')">7</button>
        <button onclick="appendValue('8')">8</button>
        <button onclick="appendValue('9')">9</button>
        <button onclick="appendValue('+')">+</button>
        <br>
        <button onclick="appendValue('4')">4</button>
        <button onclick="appendValue('5')">5</button>
        <button onclick="appendValue('6')">6</button>
        <button onclick="calculateResult()">=</button>
        <br>
        <button onclick="appendValue('1')">1</button>
        <button onclick="appendValue('2')">2</button>
        <button onclick="appendValue('3')">3</button>
        <br>
        <button onclick="appendValue('0')">0</button>
        <button onclick="appendValue('.')">.</button>
    </div>
    <script>
        function appendValue(value) {
            document.getElementById("display").value += value;
        }
        function clearDisplay() {
            document.getElementById("display").value = "";
        }
        function calculateResult() {
            try {
                document.getElementById("display").value = eval(document.getElementById("display").value);
            } catch {
                document.getElementById("display").value = "Error";
            }
        }
    </script>
</body>
</html>
