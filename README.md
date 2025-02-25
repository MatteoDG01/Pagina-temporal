<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estamos trabajando para mejorar tu experiencia Ergosistem</title>
    <style>
        body {
            font-family: Inter Semibold, sans-serif;
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f4f4f4;
            overflow: hidden;
        }

        /* Contenedor del logo */
        .logo-container {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            text-align: center;
            z-index: 2;
            opacity: 0;
            animation: sweepDown 1.5s ease-in-out forwards;
        }

        /* Estilo del logo */
        .logo-container img {
            max-width: 100px;
        }

        /* Animación de barrido desde arriba */
        @keyframes sweepDown {
            0% {
                opacity: 0;
                transform: translate(-50%, -100%);
            }
            100% {
                opacity: 1;
                transform: translate(-50%, 20px);
            }
        }

        /* Contenedor del GIF */
        .gif-container {
            width: 400px;
            height: 400px;
            margin-bottom: 20px;
            position: relative;
        }

        /* Estilo del GIF */
        .gif-container img.gif {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        /* Contenedor del texto */
        .text-container {
            position: relative;
            font-size: 2.5em;
            font-weight: bold;
            color: black;
        }

        /* Rectángulo azul marino que cubre el texto */
        .text-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #002366;
            clip-path: polygon(0 0, 0 100%, 0 100%, 0 0);
            animation: coverText 3s ease-in-out forwards;
        }

        /* Texto que cambia de color */
        .text-container span {
            position: relative;
            z-index: 1;
            mix-blend-mode: difference;
            color: white;
        }

        /* Animación del rectángulo */
        @keyframes coverText {
            0% {
                clip-path: polygon(0 0, 0 100%, 0 100%, 0 0);
            }
            100% {
                clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
            }
        }

        /* Estilos para los enlaces de redes sociales */
        .social-links {
            display: flex;
            gap: 20px; /* Espacio entre los enlaces */
        }

        .social-links a {
            display: flex;
            align-items: center;
            text-decoration: none;
            color: #333;
            font-size: 1.2em;
            padding: 10px 20px;
            border-radius: 5px;
            transition: background-color 0.3s ease, color 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        /* Efecto hover para los enlaces */
        .social-links a:hover {
            background-color: #002366; /* Azul marino */
            color: white;
        }

        /* Efecto mix-blend-mode en hover */
        .social-links a:hover img {
            mix-blend-mode: difference;
        }

        /* Estilo de los logos de redes sociales */
        .social-links a img {
            width: 50px; /* Tamaño de los logos */
            height: auto;
            margin-right: 10px; /* Espacio entre el logo y el texto */
            transition: filter 0.3s ease;
        }

        /* Ajustes adicionales para el resto de la página */
        p {
            font-size: 1.2em;
            margin-bottom: 30px;
            opacity: 0;
            animation: fadeIn 1.5s ease-in-out 1.5s forwards;
        }

        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <!-- Contenedor del logo -->
    <div class="logo-container">
        <img src="logo.png" alt="Logo" class="logo"> <!-- Cambia la ruta del logo -->
    </div>

    <!-- Contenedor del GIF -->
    <div class="gif-container">
        <img src="constructor.gif" alt="Constructor trabajando" class="gif"> <!-- Cambia la ruta del GIF -->
    </div>

    <!-- Texto con efecto de cambio de color -->
    <div class="text-container">
        <span>Estamos trabajando en algo increíble</span>
    </div>

    <!-- Texto y enlaces -->
    <p>Trabajamos en mejorar tu experiencia web con nuestras soluciones innovadoras. ¡Ya Volvemos!</p>
    <div class="social-links">
        <a href="https://www.linkedin.com/company/ergosistem/" target="_blank">
            <img src="linkedin-icon.png" alt="LinkedIn"> <!-- Cambia la ruta del logo de LinkedIn -->
            LinkedIn
        </a>
        <a href="https://facebook.com/ErgosistemPeru" target="_blank">
            <img src="facebook-icon.png" alt="Facebook"> <!-- Cambia la ruta del logo de Facebook -->
            Facebook
        </a>       
    </div>
</body>
</html>
