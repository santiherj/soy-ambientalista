<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Descarga Automática</title>
    <style>
        /* Importar la fuente Poppins */
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap');

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Poppins', sans-serif;
            text-align: center;
            flex-direction: column;
        }

        #message {
            font-size: 24px;
            margin-bottom: 20px;
        }

        #loadingGif {
            width: 100px;
            height: 100px;
        }
    </style>
</head>
<body>
    <div id="message">Descargando archivo...</div>
    <img id="loadingGif" src="https://cdn.pixabay.com/animation/2023/08/11/21/18/21-18-05-265_512.gif" alt="Cargando...">
    
    <script>
        // Crear un enlace de descarga
        var link = document.createElement('a');
        link.href = 'Dia del medio ambiente.ics'; // La URL del archivo a descargar
        link.download = 'Dia del medio ambiente.ics'; // El nombre del archivo a descargar

        // Simular un clic en el enlace
        link.click();

        // Mostrar el mensaje "Archivo descargado" después de 4 segundos
        setTimeout(function() {
            document.getElementById('message').innerText = 'Archivo descargado';

            // Ocultar el GIF de carga
            document.getElementById('loadingGif').style.display = 'none';

            // Mostrar un pop-up
            alert('Archivo descargado');

            // Cerrar la pestaña automáticamente después de 1 segundo
            setTimeout(function() {
                window.close();
            }, 1000);
        }, 4000);
    </script>
</body>
</html>
