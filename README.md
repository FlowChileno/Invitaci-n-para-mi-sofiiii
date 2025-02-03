# Invitaci-n-para-mi-sofiiii
Te amo mucho 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación de San Valentín</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="carta-container">
        <div class="carta">💌 Carta Cerrada 💌</div>
        <div class="mensaje">Soficita mía, ¿quieres ser mi San Valentín? 💘</div>
    </div>

    <div class="botones">
        <button class="abrir" onclick="abrirCarta()">Abrir</button>
        <button class="reiniciar" onclick="cerrarCarta()">Reiniciar</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #ffdde1;
    flex-direction: column;
    font-family: 'Arial', sans-serif;
}

.carta-container {
    position: relative;
    width: 300px;
    height: 200px;
    cursor: pointer;
}

.carta {
    width: 100%;
    height: 100%;
    background: #ff4d6d;
    position: absolute;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 20px;
    color: white;
    font-weight: bold;
    text-align: center;
    border-radius: 10px;
    transition: transform 0.5s ease-in-out;
}

.mensaje {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 20px;
    font-weight: bold;
    color: #ff4d6d;
    display: none;
}

.botones {
    margin-top: 20px;
}

button {
    padding: 10px 15px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
}

.abrir {
    background-color: #ff4d6d;
    color: white;
}

.reiniciar {
    background-color: #ccc;
    color: black;
}
function abrirCarta() {
    document.querySelector('.carta').style.transform = 'rotateX(180deg)';
    document.querySelector('.carta').style.display = 'none';
    document.querySelector('.mensaje').style.display = 'block';
}

function cerrarCarta() {
    document.querySelector('.carta').style.transform = 'rotateX(0deg)';
    document.querySelector('.carta').style.display = 'flex';
    document.querySelector('.mensaje').style.display = 'none';
}
