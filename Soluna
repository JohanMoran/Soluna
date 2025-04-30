<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Soluna</title>
    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            color: #333;
        }

        /* Portada */
        .portada {
            height: 100vh;
            background: linear-gradient(135deg, #6e8efb, #a777e3);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            transition: all 0.5s ease;
            position: relative;
            z-index: 1;
        }

        .contenido-portada h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .contenido-portada p {
            font-size: 1.2rem;
        }

        /* Navbar */
        .navbar {
            position: fixed;
            top: -60px; /* Inicialmente oculto */
            width: 100%;
            height: 60px;
            background: #2d3436;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 20px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            z-index: 100;
        }

        .navbar.visible {
            transform: translateY(60px); /* Lo hace visible */
        }

        .logo-pequeno img {
            height: 40px;
        }

        .menu {
            display: flex;
            list-style: none;
        }

        .menu li {
            margin-left: 20px;
        }

        .menu a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        /* Contenido */
        .contenido {
            padding: 40px 20px;
            background: white;
            min-height: 100vh;
        }

        .contenido section {
            margin-bottom: 40px;
        }

        /* Efecto al hacer scroll */
        .portada.contraida {
            height: 60px;
            position: fixed;
            top: 0;
            width: 100%;
            background: #2d3436;
            overflow: hidden;
        }

        .portada.contraida .contenido-portada {
            opacity: 0;
            transition: opacity 0.3s ease;
        }
    </style>
</head>
<body>
    <!-- Portada inicial -->
    <header class="portada" id="portada">
        <div class="contenido-portada">
            <h1>Soluna</h1>
            <p>Bienvenidos a mi sitio web</p>
        </div>
    </header>

    <!-- Barra superior (navbar) -->
    <nav class="navbar" id="navbar">
        <div class="logo-pequeno">
            <img src="logo.png" alt="Logo Soluna" width="40">
        </div>
        <ul class="menu">
            <li><a href="#">Inicio</a></li>
            <li><a href="#">Servicios</a></li>
            <li><a href="#">Contacto</a></li>
        </ul>
    </nav>

    <!-- Contenido principal -->
    <main class="contenido">
        <section>
            <h2>Sección 1</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam in dui mauris.</p>
        </section>
        <section>
            <h2>Sección 2</h2>
            <p>Vivamus luctus urna sed urna ultricies ac tempor dui sagittis.</p>
        </section>
    </main>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const portada = document.getElementById('portada');
            const navbar = document.getElementById('navbar');
            const alturaPortada = portada.offsetHeight;

            window.addEventListener('scroll', function() {
                const scrollActual = window.scrollY;

                if (scrollActual > alturaPortada * 0.2) {
                    portada.classList.add('contraida');
                    navbar.classList.add('visible');
                } else {
                    portada.classList.remove('contraida');
                    navbar.classList.remove('visible');
                }
            });
        });
    </script>
</body>
</html>
