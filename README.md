# Microscopio-
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>El Microscopio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        header {
            background: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
        }
        section {
            background: white;
            padding: 20px;
            margin-top: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
        }
        h2 {
            color: #2c3e50;
        }
        .actividad {
            margin-top: 20px;
            padding: 15px;
            background: #ecf0f1;
            border-radius: 10px;
        }
        .pregunta {
            margin-bottom: 10px;
        }
        button {
            padding: 10px 15px;
            background: #27ae60;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #2ecc71;
        }
        #resultado {
            margin-top: 15px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <header>
        <h1>El Microscopio</h1>
    </header>

    <section>
        <h2>¿Qué es un microscopio?</h2>
        <p>
            El microscopio es un instrumento que permite observar objetos demasiado pequeños
            para ser vistos a simple vista. Funciona mediante un sistema de lentes que amplifican la imagen.
        </p>
    </section>

    <section>
        <h2>Partes principales del microscopio</h2>
        <ul>
            <li><b>Ocular:</b> lente por donde observamos.</li>
            <li><b>Objetivos:</b> lentes que amplifican la imagen.</li>
            <li><b>Platina:</b> superficie donde se coloca la muestra.</li>
            <li><b>Tornillos de enfoque:</b> permiten ajustar la nitidez.</li>
            <li><b>Fuente de luz:</b> ilumina la muestra.</li>
        </ul>
    </section>

    <section class="actividad">
        <h2>Actividad Interactiva</h2>
        <p><b>Instrucciones:</b> Selecciona la respuesta correcta y presiona "Comprobar".</p>

        <div class="pregunta">
            <label>1. ¿Qué parte del microscopio usamos para mirar la muestra?</label><br>
            <select id="p1">
                <option value="">--Selecciona--</option>
                <option value="incorrecto">Platina</option>
                <option value="correcto">Ocular</option>
                <option value="incorrecto">Fuente de luz</option>
            </select>
        </div>

        <div class="pregunta">
            <label>2. ¿Qué elemento permite ajustar la nitidez?</label><br>
            <select id="p2">
                <option value="">--Selecciona--</option>
                <option value="correcto">Tornillos de enfoque</option>
                <option value="incorrecto">Objetivos</option>
                <option value="incorrecto">Platina</option>
            </select>
        </div>

        <button onclick="comprobar()">Comprobar</button>

        <p id="resultado"></p>
    </section>

    <script>
        function comprobar() {
            const p1 = document.getElementById("p1").value;
            const p2 = document.getElementById("p2").value;
            let correctas = 0;

            if (p1 === "correcto") correctas++;
            if (p2 === "correcto") correctas++;

            document.getElementById("resultado").innerText =
                "Respuestas correctas: " + correctas + " / 2";
        }
    </script>

</body>
</html>
