<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Soluna - Velas y Decoraciones</title>
    <style>
        /* Reset y variables de color */
        :root {
            --pastel-rosa: #ffd6e0;
            --pastel-lavanda: #e6e6fa;
            --pastel-menta: #c1f0c1;
            --pastel-beige: #f5f5dc;
            --pastel-azul: #d4f1f9;
            --pastel-lila: #e9d8f2;
            --borde-decorativo: #d8bfd8;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        /* Línea decorativa superior */
        .linea-decorativa {
            height: 8px;
            width: 100%;
            background: linear-gradient(90deg, 
                var(--pastel-rosa), 
                var(--pastel-lavanda), 
                var(--pastel-menta),
                var(--pastel-azul),
                var(--pastel-lila));
            position: fixed;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        body {
            display: flex;
            background-color: var(--pastel-beige);
            color: #6d6875;
            padding-top: 8px; /* Para la línea decorativa */
        }

        /* Menú lateral (más delgado) */
        .menu-lateral {
            width: 180px; /* Reducido de 250px */
            height: 100vh;
            background-color: var(--pastel-lavanda);
            padding: 20px 15px;
            position: fixed;
            box-shadow: 2px 0 10px rgba(0,0,0,0.05);
            margin-top: 8px; /* Compensa la línea decorativa */
        }

        .menu-lateral h2 {
            color: #6d6875;
            text-align: center;
            margin-bottom: 25px;
            font-size: 1.3rem;
            border-bottom: 1px dashed var(--pastel-lila);
            padding-bottom: 10px;
        }

        .menu-lateral ul {
            list-style: none;
        }

        .menu-lateral li {
            margin-bottom: 12px;
        }

        .menu-lateral a {
            color: #6d6875;
            text-decoration: none;
            font-size: 1rem;
            transition: all 0.3s ease;
            display: block;
            padding: 8px 10px;
            border-radius: 15px;
            background-color: rgba(255,255,255,0.5);
        }

        .menu-lateral a:hover {
            background-color: var(--pastel-rosa);
            transform: translateX(5px);
        }

        /* Contenido principal (ocupa espacio liberado) */
        .contenido-principal {
            margin-left: 180px; /* Igual al nuevo ancho del menú */
            width: calc(100% - 180px);
            padding: 25px;
            margin-top: 8px; /* Compensa la línea decorativa */
        }

        /* Encabezado */
        .encabezado {
            background-color: var(--pastel-lila);
            color: #6d6875;
            padding: 20px;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
            border: 1px solid var(--borde-decorativo);
        }

        .encabezado h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            color: #5d536b;
        }

        /* Secciones de productos */
        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); /* Más espacio */
            gap: 25px;
            margin-top: 30px;
        }

        .producto {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 3px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
            border: 1px solid var(--borde-decorativo);
        }

        .producto:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .producto img {
            width: 100%;
            height: 220px; /* Más grande */
            object-fit: cover;
            border-bottom: 1px solid var(--borde-decorativo);
        }

        .producto-info {
            padding: 18px;
        }

        .producto h3 {
            margin-bottom: 10px;
            color: #5d536b;
        }

        .producto p {
            color: #8e7dbe;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .precio {
            font-weight: bold;
            color: #9d65c9;
            font-size: 1.2rem;
        }

        /* Pie de página */
        .pie-pagina {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            background-color: var(--pastel-lavanda);
            color: #6d6875;
            border-radius: 12px;
            border: 1px solid var(--borde-decorativo);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .menu-lateral {
                width: 100%;
                height: auto;
                position: relative;
                margin-top: 0;
            }
            .contenido-principal {
                margin-left: 0;
                width: 100%;
                margin-top: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Línea decorativa superior -->
    <div class="linea-decorativa"></div>

    <!-- Menú lateral -->
    <nav class="menu-lateral">
        <h2>Soluna</h2>
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#velas">Velas</a></li>
            <li><a href="#decoraciones">Decoraciones</a></li>
            <li><a href="#ramos">Ramos</a></li>
            <li><a href="#recuerdos">Recuerdos</a></li>
            <li><a href="#otros">Otros</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>

    <!-- Contenido principal -->
    <main class="contenido-principal">
        <!-- Encabezado -->
        <header class="encabezado" id="inicio">
            <h1>Soluna - Velas y Decoraciones</h1>
            <p>Creaciones artesanales con esencia natural</p>
        </header>

        <!-- Sección de Velas -->
        <section id="velas">
            <h2>Nuestras Velas</h2>
            <div class="seccion-productos">
                <div class="producto">
                    <img src="https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=80" alt="Vela aromática">
                    <div class="producto-info">
                        <h3>Vela de Lavanda</h3>
                        <p>Aroma relajante para espacios íntimos</p>
                        <p class="precio">$18.000</p>
                    </div>
                </div>
                <div class="producto">
                    <img src="https://images.unsplash.com/photo-1603394633869-5fc6e406f43b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=80" alt="Vela decorativa">
                    <div class="producto-info">
                        <h3>Vela Geométrica</h3>
                        <p>Diseño moderno para decoración</p>
                        <p class="precio">$22.000</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Pie de página -->
        <footer class="pie-pagina">
            <p>© 2023 Soluna | Velas artesanales y decoración con alma</p>
        </footer>
    </main>

    <script>
        // JavaScript para interactividad (ejemplo básico)
        document.querySelectorAll('.menu-lateral a').forEach(link => {
            link.addEventListener('click', (e) => {
                document.querySelectorAll('.menu-lateral a').forEach(item => {
                    item.style.backgroundColor = 'rgba(255,255,255,0.5)';
                });
                e.target.style.backgroundColor = 'var(--pastel-rosa)';
            });
        });
    </script>
</body>
</html>
