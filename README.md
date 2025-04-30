<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SOLUN - Recuerdos y Decoración para Eventos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
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

        .linea-decorativa {
            height: 4px;
            width: 100%;
            background: linear-gradient(90deg, var(--color-primario), var(--color-destacado), var(--color-secundario));
            position: fixed;
            top: 0;
            z-index: 1000;
        }

        body {
            background-color: var(--fondo-body);
            color: var(--color-texto);
            padding-top: 4px;
        }

        /* Encabezado con búsqueda */
        .encabezado-principal {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 25px;
            background-color: var(--color-terciario);
            position: fixed;
            top: 4px;
            left: 0;
            right: 0;
            z-index: 999;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            border-bottom: 1px solid var(--borde-decorativo);
        }

        .titulo-encabezado h1 {
            font-size: 1.5rem;
            color: var(--color-primario);
            white-space: nowrap;
        }

        .busqueda-contenedor {
            width: 300px;
            display: flex;
            margin-left: 20px;
        }

        .busqueda-contenedor input {
            width: 100%;
            padding: 8px 15px;
            border: 1px solid var(--borde-decorativo);
            border-radius: 20px 0 0 20px;
            outline: none;
            background-color: rgba(255,255,255,0.7);
        }

        .busqueda-contenedor button {
            padding: 8px 15px;
            background-color: var(--color-primario);
            color: white;
            border: none;
            border-radius: 0 20px 20px 0;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .busqueda-contenedor button:hover {
            background-color: var(--color-destacado);
        }

        /* Contenedor principal */
        .contenedor-general {
            display: flex;
            margin-top: 70px; /* Compensa encabezado */
        }

        /* Menú lateral (ahora se desplaza) */
        .menu-lateral {
            width: 220px;
            background-color: var(--color-secundario);
            padding: 20px 15px;
            border-right: 1px solid var(--borde-decorativo);
            position: sticky;
            top: 70px; /* Se pega después del encabezado */
            align-self: flex-start;
            height: calc(100vh - 70px);
            overflow-y: auto;
        }

        .logo-container {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 1px dashed var(--color-primario);
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: var(--color-primario);
            letter-spacing: 2px;
            margin-bottom: 5px;
        }

        .eslogan {
            font-size: 0.8rem;
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
            font-size: 0.9rem;
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

        .contacto-menu {
            margin-top: 25px;
            padding-top: 15px;
            border-top: 1px dashed var(--color-primario);
        }

        .contacto-item {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
            font-size: 0.85rem;
        }

        .contacto-item i {
            margin-right: 10px;
            color: var(--color-destacado);
            width: 20px;
            text-align: center;
        }

        .redes-sociales {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }

        .redes-sociales a {
            color: var(--color-primario);
            font-size: 1.2rem;
            transition: transform 0.3s ease;
        }

        .redes-sociales a:hover {
            transform: scale(1.2);
            color: var(--color-destacado);
        }

        /* Contenido principal */
        .contenido-principal {
            flex: 1;
            padding: 25px;
        }

        .seccion-bienvenida {
            background-color: var(--color-terciario);
            color: var(--color-texto);
            padding: 30px;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 8px;
            border: 1px solid var(--borde-decorativo);
        }

        .seccion-bienvenida h2 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--color-primario);
        }

        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }

        .producto {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            border: 1px solid var(--borde-decorativo);
        }

        .producto:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .producto img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-bottom: 1px solid var(--borde-decorativo);
        }

        .producto-info {
            padding: 18px;
        }

        .producto h3 {
            margin-bottom: 10px;
            color: var(--color-primario);
        }

        .producto p {
            color: var(--color-destacado);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .precio {
            font-weight: bold;
            color: var(--color-primario);
            font-size: 1.1rem;
        }

        .pie-pagina {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            background-color: var(--color-secundario);
            color: var(--color-texto);
            border-radius: 8px;
            border: 1px solid var(--borde-decorativo);
            font-size: 0.9rem;
        }

        @media (max-width: 992px) {
            .contenedor-general {
                flex-direction: column;
            }
            
            .menu-lateral {
                width: 100%;
                position: relative;
                top: 0;
                height: auto;
            }
            
            .encabezado-principal {
                flex-direction: column;
                padding: 15px;
            }
            
            .busqueda-contenedor {
                width: 100%;
                margin: 15px 0 0 0;
            }
            
            .contenido-principal {
                margin-top: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Línea decorativa superior -->
    <div class="linea-decorativa"></div>

    <!-- Encabezado con búsqueda -->
    <header class="encabezado-principal">
        <div class="titulo-encabezado">
            <h1>SOLUN</h1>
        </div>
        <div class="busqueda-contenedor">
            <input type="text" placeholder="Buscar productos...">
            <button><i class="fas fa-search"></i></button>
        </div>
    </header>

    <!-- Contenedor principal -->
    <div class="contenedor-general">
        <!-- Menú lateral -->
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

            <div class="redes-sociales">
                <a href="#" target="_blank"><i class="fab fa-facebook"></i></a>
                <a href="#" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="#" target="_blank"><i class="fab fa-whatsapp"></i></a>
            </div>
        </nav>

        <!-- Contenido principal -->
        <main class="contenido-principal">
            <section class="seccion-bienvenida" id="inicio">
                <h2>Bienvenidos a SOLUN</h2>
                <p>Creaciones artesanales que hacen memorable cada evento</p>
            </section>

            <section id="recuerdos">
                <h2>Nuestros Productos Destacados</h2>
                <div class="seccion-productos">
                    <div class="producto">
                        <img src="https://via.placeholder.com/300x200?text=Vela+Aromática" alt="Vela aromática">
                        <div class="producto-info">
                            <h3>Vela de Lavanda</h3>
                            <p>Aroma relajante para espacios íntimos</p>
                            <p class="precio">$18.000</p>
                        </div>
                    </div>
                    <div class="producto">
                        <img src="https://via.placeholder.com/300x200?text=Centro+de+Mesa" alt="Centro de mesa">
                        <div class="producto-info">
                            <h3>Centro de Mesa Floral</h3>
                            <p>Combinación de velas y flores naturales</p>
                            <p class="precio">$25.000</p>
                        </div>
                    </div>
                </div>
            </section>

            <footer class="pie-pagina">
                <p>© 2023 SOLUN - Recuerdos y Decoración para Eventos | Todos los derechos reservados</p>
            </footer>
        </main>
    </div>

    <script>
        // Función de búsqueda mejorada
        const realizarBusqueda = () => {
            const termino = document.querySelector('.busqueda-contenedor input').value.trim();
            if (termino) {
                const productos = document.querySelectorAll('.producto');
                let encontrados = 0;
                
                productos.forEach(producto => {
                    const textoProducto = producto.textContent.toLowerCase();
                    if (textoProducto.includes(termino.toLowerCase())) {
                        producto.style.display = 'block';
                        encontrados++;
                        producto.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
                    } else {
                        producto.style.display = 'none';
                    }
                });
                
                if (encontrados === 0) {
                    alert(`No se encontraron productos para "${termino}"`);
                }
            } else {
                document.querySelectorAll('.producto').forEach(p => p.style.display = 'block');
            }
        };

        document.querySelector('.busqueda-contenedor button').addEventListener('click', realizarBusqueda);
        document.querySelector('.busqueda-contenedor input').addEventListener('keypress', (e) => {
            if (e.key === 'Enter') realizarBusqueda();
        });

        // Resaltar elemento de menú activo
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
