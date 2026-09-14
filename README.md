<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tarjeta Virtual - Gonzalo Moretti</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }
       .tarjeta {
            background: white;
            border-radius: 20px;
            padding: 30px;
            max-width: 400px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            text-align: center;
        }
       .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: #667eea;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px;
            color: white;
            font-weight: bold;
        }
        h1 { color: #667eea; margin: 10px 0; }
       .dato { margin: 8px 0; font-size: 16px; }
        h3 { color: #764ba2; margin-top: 20px; margin-bottom: 10px; }
        ul { text-align: left; list-style: none; padding: 0; }
        li { padding: 5px 0; }
        li:before { content: "✓ "; color: #667eea; font-weight: bold; }
        button {
            background: #667eea;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 15px;
        }
        button:hover { background: #764ba2; }
        #frase { margin-top: 15px; font-style: italic; color: #555; }
    </style>
</head>
<body>
    <div class="tarjeta">
        <div class="avatar">GM</div>
        <h1>Gonzalo Moretti</h1>
        <div class="dato"><b>Ciudad:</b> Godoy, Santa Fe</div>
        <div class="dato"><b>Edad:</b> 50 años</div>
        <div class="dato"><b>Nacimiento:</b> 08/11/1975</div>

        <h3>Mis 4 Habilidades</h3>
        <ul>
            <li>Resolución de problemas</li>
            <li>Aprender cosas nuevas rápido</li>
            <li>Buena memoria para los nombres</li>
            <li>Paciencia para enseñar</li>
        </ul>

        <h3>3 Películas Favoritas</h3>
        <ul>
            <li>El Padrino</li>
            <li>Volver al Futuro</li>
            <li>Forrest Gump</li>
        </ul>

        <h3>3 Discos Favoritos</h3>
        <ul>
            <li>Soda Stereo - Canción Animal</li>
            <li>Los Redondos - Oktubre</li>
            <li>Queen - A Night at the Opera</li>
        </ul>

        <button onclick="mostrarFrase()">Tocame para una frase</button>
        <div id="frase"></div>
    </div>

    <script>
        // FUNCION DINAMICA PROPIA
        function mostrarFrase() {
            const frases = [
                "El que persevera, alcanza.",
                "Nunca es tarde para aprender algo nuevo.",
                "Cada día es una nueva oportunidad."
            ];
            const random = Math.floor(Math.random() * frases.length);
            document.getElementById("frase").innerText = frases[random];
        }
    </script>
</body>
</html>
