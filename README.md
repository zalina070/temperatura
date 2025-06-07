# temperatura
<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <title>Конвертер температуры</title>
</head>

<body>
    <h2>🌡️ Конвертер температуры</h2>

    <label for="celsius">Температура в Цельсиях (°C):</label>
    <input type="number" id="celsius" placeholder="Например, 25">
    <button onclick="convertToF()">Преобразовать в Фаренгейты</button>

    <br><br>

    <label for="fahrenheit">Температура в Фаренгейтах (°F):</label>
    <input type="number" id="fahrenheit" placeholder="Например, 77">
    <button onclick="convertToC()">Преобразовать в Цельсии</button>

    <p id="result"></p>

    <script>
        function convertToF() {
            const celsius = parseFloat(document.getElementById('celsius').value);
            if (isNaN(celsius)) {
                document.getElementById('result').textContent = "Введите корректную температуру в °C.";
                return;
            }
            const fahrenheit = (celsius * 9 / 5) + 32;
            document.getElementById('result').textContent =
                `${celsius}\u00B0C - ${fahrenheit.toFixed(2)}\u00B0F`;
        }

        function convertToC() {
            const fahrenheit = parseFloat(document.getElementById('fahrenheit').value);
            if (isNaN(fahrenheit)) {
                document.getElementById('result').textContent = "Введите корректную температуру в °F.";
                return;
            }
            const celsius = (fahrenheit - 32) * 5 / 9;
            document.getElementById('result').textContent =
                `${fahrenheit}\u00B0F - ${celsius.toFixed(2)}\u00B0C`;
        }
    </script>
</body>

</html>
