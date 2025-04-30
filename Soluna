<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SOLUN - Recuerdos y Decoración para Eventos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Paleta de colores */
        :root {
            --color-primario: #8B5A2B;
            --color-secundario: #D2B48C;
            --color-terciario: #F5DEB3;
            --color-destacado: #A0522D;
            --color-texto: #5C4033;
            --borde-decorativo: #CD853F;
            --fondo-body: #FFF8DC;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Georgia', serif;
        }

        /* Línea decorativa superior */
        .linea-decorativa {
            height: 6px;
            width: 100%;
            background: linear-gradient(90deg, var(--color-primario), var(--color-destacado), var(--color-secundario));
            position: fixed;
            top: 0;
            z-index: 1000;
        }

        /* Barra de búsqueda */
        .barra-busqueda {
            position: fixed;
            top: 6px;
            left: 0;
            right: 0;
            background-color: var(--color-secundario);
            padding: 10px 20px;
            display: flex;
            justify-content: center;
            z-index: 999;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .busqueda-contenedor {
            width: 60%;
            display: flex;
        }

        .busqueda-contenedor input {
            width: 100%;
            padding: 8px 15px;
            border: 1px solid var(--borde-decorativo);
            border-radius: 20px 0 0 20px;
            outline: none;
        }

        .busqueda-contenedor button {
            padding: 8px 15px;
            background-color: var(--color-primario);
            color: white;
            border: none;
            border-radius: 0 20px 20px 0;
            cursor: pointer;
        }

        body {
            display: flex;
            background-color: var(--fondo-body);
            color: var(--color-texto);
            padding-top: 56px; /* Compensa línea + barra búsqueda */
        }

        /* Menú lateral ampliado */
        .menu-lateral {
            width: 220px; /* Más ancho */
            height: 100vh;
            background-color: var(--color-secundario);
            padding: 20px 15px;
            position: fixed;
            margin-top: 50px; /* Compensa búsqueda */
            border-right: 1px solid var(--borde-decorativo);
            overflow-y: auto;
        }

        .logo-container {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px dashed var(--color-primario);
        }

        .logo {
            font-size: 2.2rem; /* Más grande */
            font-weight: bold;
            color: var(--color-primario);
            letter-spacing: 3px;
            margin-bottom: 5px;
        }

        .eslogan {
            font-size: 0.85rem;
            color: var(--color-destacado);
            font-style: italic;
        }

        .menu-lateral ul {
            list-style: none;
            margin-bottom: 30px;
        }

        .menu-lateral li {
            margin-bottom: 12px;
        }

        .menu-lateral a {
            color: var(--color-texto);
            text-decoration: none;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            display: block;
            padding: 8px 12px;
            border-radius: 15px;
            background-color: rgba(255, 255, 255, 0.3);
        }

        .menu-lateral a:hover {
            background-color: var(--color-terciario);
            transform: translateX(5px);
        }

        /* Sección de contacto */
        .contacto-menu {
            margin-top: 25px;
            padding-top: 15px;
            border-top: 1px dashed var(--color-primario);
        }

        .contacto-item {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
            font-size: 0.9rem;
        }

        .contacto-item i {
            margin-right: 10px;
            color: var(--color-destacado);
            width: 20px;
            text-align: center;
        }

        /* Redes sociales */
        .redes-sociales {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }

        .redes-sociales a {
            color: var(--color-primario);
            font-size: 1.3rem;
            transition: transform 0.3s ease;
        }

        .redes-sociales a:hover {
            transform: scale(1.2);
            color: var(--color-destacado);
        }

        /* Contenido principal */
        .contenido-principal {
            margin-left: 220px;
            width: calc(100% - 220px);
            padding: 25px;
            margin-top: 50px; /* Compensa búsqueda */
        }

        /* Resto de estilos (encabezado, productos, pie) */
        .encabezado {
            background-color: var(--color-terciario);
            color: var(--color-texto);
            padding: 25px;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 8px;
            border: 1px solid var(--borde-decorativo);
        }

        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .producto {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            border: 1px solid var(--borde-decorativo);
        }

        .pie-pagina {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            background-color: var(--color-secundario);
            color: var(--color-texto);
            border-radius: 8px;
            border: 1px solid var(--borde-decorativo);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .menu-lateral {
                width: 100%;
                position: relative;
                margin-top: 0;
                height: auto;
            }
            .contenido-principal {
                margin-left: 0;
                width: 100%;
                margin-top: 20px;
            }
            .barra-busqueda {
                position: relative;
                top: 0;
            }
            body {
                padding-top: 0;
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Línea decorativa superior -->
    <div class="linea-decorativa"></div>

    <!-- Barra de búsqueda -->
    <div class="barra-busqueda">
        <div class="busqueda-contenedor">
            <input type="text" placeholder="Buscar productos...">
            <button><i class="fas fa-search"></i></button>
        </div>
    </div>

    <!-- Menú lateral ampliado -->
    <nav class="menu-lateral">
        <div class="logo-container">
            <div class="logo">SOLUN</div>
            <div class="eslogan">Recuerdos y decoración para eventos</div>
        </div>
        
        <ul>
            <li><a href="#inicio"><i class="fas fa-home"></i> Inicio</a></li>
            <li><a href="#velas"><i class="fas fa-fire"></i> Velas</a></li>
            <li><a href="#decoraciones"><i class="fas fa-palette"></i> Decoraciones</a></li>
            <li><a href="#ramos"><i class="fas fa-spa"></i> Ramos</a></li>
            <li><a href="#recuerdos"><i class="fas fa-gift"></i> Recuerdos</a></li>
        </ul>

        <!-- Información de contacto -->
        <div class="contacto-menu">
            <div class="contacto-item">
                <i class="fas fa-phone"></i>
                <span>335 106 9229</span>
            </div>
            <div class="contacto-item">
                <i class="fas fa-envelope"></i>
                <span>solunaclientes@gmail.com</span>
            </div>
        </div>

        <!-- Redes sociales -->
        <div class="redes-sociales">
            <a href="#" target="_blank"><i class="fab fa-facebook"></i></a>
            <a href="#" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="#" target="_blank"><i class="fab fa-whatsapp"></i></a>
        </div>
    </nav>

    <!-- Contenido principal -->
    <main class="contenido-principal">
        <header class="encabezado" id="inicio">
            <h1>Bienvenidos a SOLUN</h1>
            <p>Creaciones artesanales que hacen memorable cada evento</p>
        </header>

        <section id="recuerdos">
            <h2>Nuestros Productos Destacados</h2>
            <div class="seccion-productos">
                <div class="producto">
                    <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=80" alt="Recuerdo de boda">
                    <div class="producto-info">
                        <h3>Miniatura de Boda</h3>
                        <p>Detalle elegante para invitados</p>
                        <p class="precio">$12.000</p>
                    </div>
                </div>
                <div class="producto">
                    <img src="https://images.unsplash.com/photo-1513151233558-d860c5398176?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=300&q=80" alt="Detalle de bautizo">
                    <div class="producto-info">
                        <h3>Caja de Bautizo</h3>
                        <p>Recuerdo personalizado</p>
                        <p class="precio">$15.000</p>
                    </div>
                </div>
            </div>
        </section>

        <footer class="pie-pagina">
            <p>© 2023 SOLUN - Recuerdos y Decoración para Eventos | Todos los derechos reservados</p>
        </footer>
    </main>

    <script>
        // Función de búsqueda básica
        document.querySelector('.busqueda-contenedor button').addEventListener('click', function() {
            const termino = document.querySelector('.busqueda-contenedor input').value;
            if (termino) {
                alert(`Buscando: "${termino}"`);
                // Aquí podrías implementar la lógica real de búsqueda
            }
        });

        // Permitir búsqueda al presionar Enter
        document.querySelector('.busqueda-contenedor input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                document.querySelector('.busqueda-contenedor button').click();
            }
        });

        // Interactividad del menú
        document.querySelectorAll('.menu-lateral a').forEach(link => {
            link.addEventListener('click', (e) => {
                document.querySelectorAll('.menu-lateral a').forEach(item => {
                    item.style.backgroundColor = 'rgba(255,255,255,0.3)';
                });
                e.target.style.backgroundColor = 'var(--color-terciario)';
            });
        });
    </script>
</body>
</html>
