exercicio do dia 22/04/26    
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <m\\eta charset="UTF-8">
    <title>Contador Interativo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1 id="numero">0</h1>

    <button id="incrementar">Incrementar</button>
    <button id="decrementar">Decrementar</button>
    <button id="zerar">Zerar</button>

    <script src="script.js"></script>
</body>
</html>

body {
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 50px;
}

h1 {
    font-size: 50px;
}

button {
    margin: 10px;
    padding: 10px 20px;
    font-size: 16px;
}


let contador = 0;

const numero = document.getElementById("numero");
const btnInc = document.getElementById("incrementar");
const btnDec = document.getElementById("decrementar");
const btnZerar = document.getElementById("zerar");

function atualizarTela() {
    numero.textContent = contador;

    if (contador > 0) {
        numero.style.color = "green";
    } else if (contador < 0) {
        numero.style.color = "red";
    } else {
        numero.style.color = "black";
    }
}

btnInc.addEventListener("click", () => {
    contador++;
    atualizarTela();
});

btnDec.addEventListener("click", () => {
    contador--;
    atualizarTela();
});

btnZerar.addEventListener("click", () => {
    contador = 0;
    atualizarTela();
});
