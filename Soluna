<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Soluna - Velas y Decoraciones</title>
    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        /* Estilos generales */
        body {
            display: flex;
            background-color: #f9f5f0; /* Color crema claro */
            color: #5a4a42; /* Color marrón oscuro */
        }

        /* Menú lateral */
        .menu-lateral {
            width: 250px;
            height: 100vh;
            background-color: #8b7355; /* Color madera claro */
            padding: 20px;
            position: fixed;
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.1);
        }

        .menu-lateral h2 {
            color: #fff;
            text-align: center;
            margin-bottom: 30px;
            font-size: 1.5rem;
            border-bottom: 1px solid #fff;
            padding-bottom: 10px;
        }

        .menu-lateral ul {
            list-style: none;
        }

        .menu-lateral li {
            margin-bottom: 15px;
        }

        .menu-lateral a {
            color: #fff;
            text-decoration: none;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            display: block;
            padding: 8px;
            border-radius: 4px;
        }

        .menu-lateral a:hover {
            background-color: #a08669; /* Color madera más oscuro */
            transform: translateX(5px);
        }

        /* Contenido principal */
        .contenido-principal {
            margin-left: 250px; /* Igual al ancho del menú */
            width: calc(100% - 250px);
            padding: 20px;
        }

        /* Encabezado */
        .encabezado {
            background-color: #d4a373; /* Color terracota */
            color: white;
            padding: 20px;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .encabezado h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .encabezado p {
            font-size: 1.2rem;
            font-style: italic;
        }

        /* Secciones de productos */
        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .producto {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .producto:hover {
            transform: translateY(-5px);
        }

        .producto img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .producto-info {
            padding: 15px;
        }

        .producto h3 {
            margin-bottom: 10px;
            color: #5a4a42;
        }

        .producto p {
            color: #8b7355;
            margin-bottom: 15px;
        }

        .precio {
            font-weight: bold;
            color: #d4a373;
            font-size: 1.2rem;
        }

        /* Pie de página */
        .pie-pagina {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            background-color: #8b7355;
            color: white;
            border-radius: 8px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            body {
                flex-direction: column;
            }
            .menu-lateral {
                width: 100%;
                height: auto;
                position: relative;
            }
            .contenido-principal {
                margin-left: 0;
                width: 100%;
            }
        }
    </style>
</head>
<body>
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
            <h1>Soluna - Velas y Decoraciones Artesanales</h1>
            <p>Ilumina tus momentos especiales con nuestras creaciones únicas</p>
        </header>

        <!-- Sección de Velas -->
        <section id="velas">
            <h2>Nuestras Velas</h2>
            <div class="seccion-productos">
                <div class="producto">
                    <img src="https://via.placeholder.com/300x200?text=Vela+Aromática" alt="Vela aromática">
                    <div class="producto-info">
                        <h3>Vela Aromática</h3>
                        <p>Fragancia relajante de lavanda</p>
                        <p class="precio">$15.000</p>
                    </div>
                </div>
                <div class="producto">
                    <img src="https://via.placeholder.com/300x200?text=Vela+Decorativa" alt="Vela decorativa">
                    <div class="producto-info">
                        <h3>Vela Decorativa</h3>
                        <p>Diseño elegante para tu hogar</p>
                        <p class="precio">$12.000</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Sección de Decoraciones -->
        <section id="decoraciones">
            <h2>Decoraciones</h2>
            <div class="seccion-productos">
                <div class="producto">
                    <img src="https://via.placeholder.com/300x200?text=Centro+de+Mesa" alt="Centro de mesa">
                    <div class="producto-info">
                        <h3>Centro de Mesa</h3>
                        <p>Combinación de velas y flores secas</p>
                        <p class="precio">$25.000</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Pie de página -->
        <footer class="pie-pagina">
            <p>© 2023 Soluna - Velas y Decoraciones | Todos los derechos reservados</p>
        </footer>
    </main>

    <script>
        // Puedes añadir funcionalidad JavaScript aquí
        document.addEventListener('DOMContentLoaded', function() {
            console.log('Página cargada correctamente');
            // Ejemplo: Podrías añadir un carrito de compras aquí
        });
    </script>
</body>
</html>
