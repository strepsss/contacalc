<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Divisão da Conta de Água</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .input-group {
            margin-bottom: 10px;
        }
        .input-group label {
            display: block;
            margin-bottom: 5px;
        }
        .input-group input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 3px;
            box-sizing: border-box;
        }
        .result {
            margin-top: 20px;
            font-weight: bold;
        }
        footer {
            margin-top: 20px;
            text-align: center;
            font-size: 12px;
            color: #666;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Divisão da Conta de Água</h2>
        <div class="input-group">
            <label for="valorContaAgua">Valor da Conta de Água (R$):</label>
            <input type="number" id="valorContaAgua" required>
        </div>
        <div class="input-group">
            <label for="diasMes">Quantidade total de Dias do Mês:</label>
            <input type="number" id="diasMes" required>
        </div>
        <div class="input-group">
            <label for="diasUtilizados">Quantidade de Dias em que a Água foi Utilizada:</label>
            <input type="number" id="diasUtilizados" required>
        </div>
        <div class="input-group">
            <label for="numPessoas">Número de Pessoas na Casa:</label>
            <input type="number" id="numPessoas" required>
        </div>
        <button onclick="calcular()">Calcular</button>
        <div id="resultado" class="result"></div>
    </div>

    <footer>
        &copy; 2023 - Criado por Fellipe Hélio. Todos os direitos reservados. A reprodução deste algoritmo é proibida.
    </footer>

    <script>
        function calcular() {
            // Aviso de proibição de reprodução
            console.warn("A reprodução deste algoritmo é proibida.");

            var valorContaAgua = parseFloat(document.getElementById("valorContaAgua").value);
            var diasMes = parseInt(document.getElementById("diasMes").value);
            var diasUtilizados = parseInt(document.getElementById("diasUtilizados").value);
            var numPessoas = parseInt(document.getElementById("numPessoas").value);

            var valorDiario = valorContaAgua / diasMes;
            var valorUtilizado = valorDiario * diasUtilizados;
            var valorPorPessoa = valorUtilizado / numPessoas;

            document.getElementById("resultado").innerText = "Cada pessoa deve pagar: R$ " + valorPorPessoa.toFixed(2);
        }
    </script>
</body>
</html>
