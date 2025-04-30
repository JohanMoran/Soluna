<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SOLUN - Decoración y Recuerdos para Eventos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --color-primario: #C8A2C8;  /* Lila pastel */
            --color-secundario: #FFD1DC; /* Rosa claro */
            --color-terciario: #E0F7FA;  /* Azul muy claro */
            --color-destacado: #B5EAD7;  /* Verde menta */
            --color-texto: #6D6875;      /* Gris morado */
            --borde-decorativo: #FFB7B2; /* Coral claro */
            --fondo-body: #FAF9F6;       /* Blanco hueso */
            --sombra: 0 4px 8px rgba(0, 0, 0, 0.05);
            --transicion: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Quicksand', sans-serif;
        }

        body {
            background-color: var(--fondo-body);
            color: var(--color-texto);
            line-height: 1.6;
        }

        /* Línea decorativa */
        .linea-decorativa {
            height: 5px;
            width: 100%;
            background: linear-gradient(90deg, var(--color-primario), var(--color-destacado), var(--color-secundario));
            position: fixed;
            top: 0;
            z-index: 1000;
        }

        /* Encabezado */
        .encabezado-principal {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            background-color: white;
            position: fixed;
            top: 5px;
            left: 0;
            right: 0;
            z-index: 999;
            box-shadow: var(--sombra);
        }

        .titulo-encabezado h1 {
            font-size: 1.8rem;
            color: var(--color-primario);
        }

        .busqueda-contenedor {
            width: 300px;
            position: relative;
        }

        .busqueda-contenedor input {
            width: 100%;
            padding: 10px 20px;
            border: 1px solid var(--borde-decorativo);
            border-radius: 30px;
            outline: none;
            background-color: rgba(255,255,255,0.8);
        }

        .busqueda-contenedor button {
            position: absolute;
            right: 10px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: var(--color-primario);
            cursor: pointer;
        }

        .carrito-icono {
            font-size: 1.5rem;
            color: var(--color-primario);
            cursor: pointer;
            position: relative;
        }

        .carrito-contador {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--color-destacado);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* MENÚ LATERAL (ANCHO AUMENTADO A 320px) */
        .menu-lateral {
            width: 320px;
            background-color: var(--color-secundario);
            padding: 30px 25px;
            position: fixed;
            top: 65px;
            left: 0;
            height: calc(100vh - 65px);
            overflow-y: auto;
            z-index: 900;
            transition: var(--transicion);
        }

        .logo-container {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px dashed var(--color-primario);
        }

        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--color-primario);
            margin-bottom: 10px;
        }

        .eslogan {
            font-size: 1rem;
            color: var(--color-texto);
            opacity: 0.8;
        }

        .menu-lateral ul {
            list-style: none;
            margin: 40px 0;
        }

        .menu-lateral li {
            margin-bottom: 15px;
        }

        .menu-lateral a {
            display: block;
            padding: 12px 20px;
            color: var(--color-texto);
            text-decoration: none;
            border-radius: 8px;
            transition: var(--transicion);
            font-size: 1.1rem;
            background-color: rgba(255,255,255,0.4);
        }

        .menu-lateral a:hover {
            background-color: white;
            transform: translateX(5px);
            box-shadow: var(--sombra);
        }

        .menu-lateral i {
            margin-right: 12px;
            width: 20px;
            text-align: center;
            color: var(--color-primario);
        }

        .contacto-menu {
            margin-top: 30px;
        }

        .contacto-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .redes-sociales {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .redes-sociales a {
            color: var(--color-primario);
            font-size: 1.3rem;
            transition: var(--transicion);
        }

        .redes-sociales a:hover {
            transform: translateY(-3px);
        }

        /* CONTENIDO PRINCIPAL */
        .contenido-principal {
            margin-left: 320px; /* Ajustado al ancho del menú */
            padding: 30px 5%;
            margin-top: 65px;
        }

        /* Sección de bienvenida */
        .seccion-bienvenida {
            background: linear-gradient(135deg, var(--color-terciario), white);
            padding: 40px;
            border-radius: 12px;
            text-align: center;
            margin-bottom: 40px;
            box-shadow: var(--sombra);
        }

        .seccion-bienvenida h2 {
            font-size: 2.2rem;
            color: var(--color-primario);
            margin-bottom: 15px;
        }

        .seccion-bienvenida p {
            max-width: 700px;
            margin: 0 auto 20px;
        }

        .btn-destacado {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--color-primario);
            color: white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: var(--transicion);
        }

        .btn-destacado:hover {
            background-color: var(--color-destacado);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
        }

        /* Productos */
        .seccion-titulo {
            font-size: 1.8rem;
            color: var(--color-primario);
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--borde-decorativo);
        }

        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .producto {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--sombra);
            transition: var(--transicion);
        }

        .producto:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .producto-imagen {
            height: 220px;
            overflow: hidden;
        }

        .producto img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transicion);
        }

        .producto:hover img {
            transform: scale(1.05);
        }

        .producto-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--color-destacado);
            color: white;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        .producto-info {
            padding: 20px;
        }

        .producto h3 {
            color: var(--color-primario);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .producto p {
            color: var(--color-texto);
            margin-bottom: 15px;
            opacity: 0.8;
        }

        .producto-precio {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .precio {
            font-weight: bold;
            color: var(--color-primario);
            font-size: 1.2rem;
        }

        .btn-carrito {
            background-color: var(--color-secundario);
            color: var(--color-texto);
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            transition: var(--transicion);
        }

        .btn-carrito:hover {
            background-color: var(--color-primario);
            color: white;
        }

        /* Testimonios */
        .testimonios-contenedor {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .testimonio {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: var(--sombra);
        }

        .testimonio-texto {
            font-style: italic;
            margin-bottom: 15px;
            position: relative;
        }

        .testimonio-autor {
            display: flex;
            align-items: center;
        }

        .testimonio-autor img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
            border: 2px solid var(--borde-decorativo);
        }

        /* Pie de página */
        .pie-pagina {
            background: linear-gradient(to right, var(--color-primario), var(--color-destacado));
            color: white;
            padding: 40px 5%;
            margin-top: 50px;
            border-radius: 12px 12px 0 0;
        }

        .pie-contenedor {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .pie-columna h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid rgba(255,255,255,0.3);
        }

        .pie-columna a {
            color: white;
            text-decoration: none;
            display: block;
            margin-bottom: 10px;
            transition: var(--transicion);
        }

        .pie-columna a:hover {
            transform: translateX(5px);
        }

        .pie-copyright {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.3);
        }

        /* WhatsApp flotante */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            z-index: 100;
            transition: var(--transicion);
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
        }

        /* Responsive */
        @media (max-width: 1200px) {
            .menu-lateral {
                width: 280px;
            }
            .contenido-principal {
                margin-left: 280px;
            }
        }

        @media (max-width: 992px) {
            .menu-lateral {
                width: 100%;
                position: relative;
                top: auto;
                height: auto;
            }
            .contenido-principal {
                margin-left: 0;
                margin-top: 20px;
            }
            .encabezado-principal {
                flex-direction: column;
                gap: 15px;
                padding: 15px;
            }
            .busqueda-contenedor {
                width: 100%;
            }
        }

        @media (max-width: 768px) {
            .seccion-productos {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <div class="linea-decorativa"></div>

    <header class="encabezado-principal">
        <div class="titulo-encabezado">
            <h1>SOLUN</h1>
        </div>
        <div class="busqueda-contenedor">
            <input type="text" placeholder="Buscar productos...">
            <button><i class="fas fa-search"></i></button>
        </div>
        <div class="carrito-icono">
            <i class="fas fa-shopping-cart"></i>
            <span class="carrito-contador">0</span>
        </div>
    </header>

    <nav class="menu-lateral">
        <div class="logo-container">
            <div class="logo">SOLUN</div>
            <div class="eslogan">Decoración y recuerdos para tus momentos especiales</div>
        </div>
        
        <ul>
            <li><a href="#inicio"><i class="fas fa-home"></i> Inicio</a></li>
            <li><a href="#productos"><i class="fas fa-gift"></i> Productos</a></li>
            <li><a href="#galeria"><i class="fas fa-images"></i> Galería</a></li>
            <li><a href="#testimonios"><i class="fas fa-star"></i> Testimonios</a></li>
            <li><a href="#contacto"><i class="fas fa-envelope"></i> Contacto</a></li>
        </ul>

        <div class="contacto-menu">
            <div class="contacto-item">
                <i class="fas fa-phone"></i> 335 106 9229
            </div>
            <div class="contacto-item">
                <i class="fas fa-envelope"></i> solunaclientes@gmail.com
            </div>
            <div class="contacto-item">
                <i class="fas fa-map-marker-alt"></i> Guadalajara, Jalisco
            </div>
        </div>

        <div class="redes-sociales">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-whatsapp"></i></a>
        </div>
    </nav>

    <main class="contenido-principal">
        <section class="seccion-bienvenida" id="inicio">
            <h2>Bienvenidos a SOLUN</h2>
            <p>Creaciones artesanales únicas que transforman tus eventos en momentos inolvidables. Especialistas en velas aromáticas, decoración floral y recuerdos personalizados.</p>
            <a href="#productos" class="btn-destacado">Ver Catálogo</a>
        </section>

        <section id="productos">
            <h2 class="seccion-titulo">Nuestros Productos</h2>
            <div class="seccion-productos">
                <!-- Producto 1 -->
                <div class="producto">
                    <div class="producto-imagen">
                        <span class="producto-badge">Nuevo</span>
                        <img src="https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Vela aromática">
                    </div>
                    <div class="producto-info">
                        <h3>Vela de Lavanda</h3>
                        <p>Aroma relajante para espacios íntimos, elaborada con cera de soja y esencia natural.</p>
                        <div class="producto-precio">
                            <span class="precio">$18.000</span>
                            <button class="btn-carrito"><i class="fas fa-cart-plus"></i></button>
                        </div>
                    </div>
                </div>

                <!-- Producto 2 -->
                <div class="producto">
                    <div class="producto-imagen">
                        <span class="producto-badge">Más vendido</span>
                        <img src="https://images.unsplash.com/photo-1513151233558-d860c5398176?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Centro de mesa">
                    </div>
                    <div class="producto-info">
                        <h3>Centro de Mesa Floral</h3>
                        <p>Combinación de velas y flores naturales para decoración de bodas y eventos.</p>
                        <div class="producto-precio">
                            <span class="precio">$25.000</span>
                            <button class="btn-carrito"><i class="fas fa-cart-plus"></i></button>
                        </div>
                    </div>
                </div>

                <!-- Producto 3 -->
                <div class="producto">
                    <div class="producto-imagen">
                        <img src="https://images.unsplash.com/photo-1499209974431-9dddcece7f88?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Ramo de novia">
                    </div>
                    <div class="producto-info">
                        <h3>Ramo de Novia Clásico</h3>
                        <p>Elegante ramo con rosas blancas y detalles de encaje para el día de tu boda.</p>
                        <div class="producto-precio">
                            <span class="precio">$28.000</span>
                            <button class="btn-carrito"><i class="fas fa-cart-plus"></i></button>
                        </div>
                    </div>
                </div>

                <!-- Producto 4 -->
                <div class="producto">
                    <div class="producto-imagen">
                        <span class="producto-badge">Oferta</span>
                        <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Recuerdo de boda">
                    </div>
                    <div class="producto-info">
                        <h3>Recuerdo de Boda</h3>
                        <p>Mini velas personalizadas con nombres de los novios y fecha de la boda.</p>
                        <div class="producto-precio">
                            <span class="precio">$9.500</span>
                            <button class="btn-carrito"><i class="fas fa-cart-plus"></i></button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="testimonios">
            <h2 class="seccion-titulo">Testimonios</h2>
            <div class="testimonios-contenedor">
                <div class="testimonio">
                    <div class="testimonio-texto">
                        "Las velas aromáticas de SOLUN transformaron completamente la atmósfera de mi boda. El aroma era perfecto y todos mis invitados preguntaban dónde las había comprado."
                    </div>
                    <div class="testimonio-autor">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="María González">
                        <div>
                            <h4>María González</h4>
                            <p>Boda en Guadalajara</p>
                        </div>
                    </div>
                </div>

                <div class="testimonio">
                    <div class="testimonio-texto">
                        "El centro de mesa que encargué superó todas mis expectativas. La calidad de las flores y la combinación con las velas fue exactamente lo que quería para mi aniversario."
                    </div>
                    <div class="testimonio-autor">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Carlos Mendoza">
                        <div>
                            <h4>Carlos Mendoza</h4>
                            <p>25° Aniversario</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <footer class="pie-pagina">
            <div class="pie-contenedor">
                <div class="pie-columna">
                    <h3>SOLUN</h3>
                    <p>Artesanías en velas y decoración para eventos especiales. Creando momentos memorables desde 2018.</p>
                </div>

                <div class="pie-columna">
                    <h3>Enlaces</h3>
                    <a href="#inicio">Inicio</a>
                    <a href="#productos">Productos</a>
                    <a href="#testimonios">Testimonios</a>
                    <a href="#contacto">Contacto</a>
                </div>

                <div class="pie-columna">
                    <h3>Contacto</h3>
                    <a href="tel:+523351069229"><i class="fas fa-phone"></i> 335 106 9229</a>
                    <a href="mailto:solunaclientes@gmail.com"><i class="fas fa-envelope"></i> solunaclientes@gmail.com</a>
                    <a href="#"><i class="fas fa-map-marker-alt"></i> Guadalajara, Jalisco</a>
                </div>
            </div>

            <div class="pie-copyright">
                <p>&copy; 2023 SOLUN - Todos los derechos reservados</p>
            </div>
        </footer>
    </main>

    <a href="https://wa.me/523351069229" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Función de búsqueda
        document.querySelector('.busqueda-contenedor button').addEventListener('click', buscarProductos);
        document.querySelector('.busqueda-contenedor input').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') buscarProductos();
        });

        function buscarProductos() {
            const termino = document.querySelector('.busqueda-contenedor input').value.toLowerCase();
            const productos = document.querySelectorAll('.producto');
            let encontrados = 0;

            productos.forEach(producto => {
                const texto = producto.textContent.toLowerCase();
                if (texto.includes(termino)) {
                    producto.style.display = 'block';
                    encontrados++;
                } else {
                    producto.style.display = 'none';
                }
            });

            if (encontrados === 0) {
                alert('No se encontraron productos con ese nombre');
            }
        }

        // Carrito de compras (funcionalidad básica)
        let carrito = [];
        const contadorCarrito = document.querySelector('.carrito-contador');

        document.querySelectorAll('.btn-carrito').forEach(btn => {
            btn.addEventListener('click', function() {
                const producto = this.closest('.producto');
                const nombre = producto.querySelector('h3').textContent;
                const precio = producto.querySelector('.precio').textContent;
                
                carrito.push({ nombre, precio });
                contadorCarrito.textContent = carrito.length;
                
                // Animación
                this.innerHTML = '<i class="fas fa-check"></i>';
                setTimeout(() => {
                    this.innerHTML = '<i class="fas fa-cart-plus"></i>';
                }, 1000);
            });
        });
    </script>
</body>
</html>
