# Temperaturen
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <title>Temperaturumrechnung</title>
</head>
<body>
    <h1>Temperaturumrechnung</h1>
    
    <h2>Celsius zu Kelvin</h2>
    <input type="number" id="celsiusInput" placeholder="Grad Celsius">
    <button onclick="convertCelsiusToKelvin()">Umwandeln</button>
    <p id="kelvinResult"></p>
    
    <h2>Kelvin zu Celsius</h2>
    <input type="number" id="kelvinInput" placeholder="Kelvin">
    <button onclick="convertKelvinToCelsius()">Umwandeln</button>
    <p id="celsiusResult"></p>
    
    <script>
        // Funktion zur Umwandlung von Celsius in Kelvin
        function celsiusToKelvin(celsius) {
            return celsius + 273.15;
        }

        // Funktion zur Umwandlung von Kelvin in Celsius
        function kelvinToCelsius(kelvin) {
            return kelvin - 273.15;
        }

        // Funktion zur Umwandlung von Celsius zu Kelvin und Anzeige des Ergebnisses
        function convertCelsiusToKelvin() {
            let celsius = parseFloat(document.getElementById('celsiusInput').value);
            let kelvin = celsiusToKelvin(celsius);
            document.getElementById('kelvinResult').innerText = `${celsius} Grad Celsius sind ${kelvin} Kelvin`;
        }

        // Funktion zur Umwandlung von Kelvin zu Celsius und Anzeige des Ergebnisses
        function convertKelvinToCelsius() {
            let kelvin = parseFloat(document.getElementById('kelvinInput').value);
            let celsius = kelvinToCelsius(kelvin);
            document.getElementById('celsiusResult').innerText = `${kelvin} Kelvin sind ${celsius} Grad Celsius`;
        }
    </script>
</body>
</html>
