<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>آلة حاسبة بسيطة</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        .calculator {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            background: white;
            box-shadow: 0px 0px 10px gray;
            border-radius: 10px;
        }
        input {
            width: 90%;
            height: 50px;
            font-size: 1.5em;
            text-align: right;
            margin-bottom: 10px;
        }
        button {
            width: 23%;
            height: 50px;
            font-size: 1.2em;
            margin: 5px;
            cursor: pointer;
        }
        .equal {
            width: 48%;
        }
        .clear {
            background: red;
            color: white;
        }
    </style>
</head>
<body>

    <div class="calculator">
        <input type="text" id="display" disabled>
        <br>
        <button onclick="clearDisplay()" class="clear">C</button>
        <button onclick="appendValue('7')">7</button>
        <button onclick="appendValue('8')">8</button>
        <button onclick="appendValue('9')">9</button>
        <button onclick="appendValue('/')">/</button>
        <br>
        <button onclick="appendValue('4')">4</button>
        <button onclick="appendValue('5')">5</button>
        <button onclick="appendValue('6')">6</button>
        <button onclick="appendValue('*')">×</button>
        <br>
        <button onclick="appendValue('1')">1</button>
        <button onclick="appendValue('2')">2</button>
        <button onclick="appendValue('3')">3</button>
        <button onclick="appendValue('-')">-</button>
        <br>
        <button onclick="appendValue('0')">0</button>
        <button onclick="appendValue('.')">.</button>
        <button onclick="calculateResult()" class="equal">=</button>
        <button onclick="appendValue('+')">+</button>
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
                document.getElementById("display").value = "خطأ";
            }
        }
    </script>

</body>
</html># -
