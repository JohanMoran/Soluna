<!DOCTYPE html>
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

        .resultados-busqueda {
            position: absolute;
            top: 100%;
            left: 0;
            right: 0;
            background: white;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            z-index: 1000;
            display: none;
            max-height: 300px;
            overflow-y: auto;
        }

        .resultado-item {
            padding: 10px 15px;
            border-bottom: 1px solid #eee;
            cursor: pointer;
            transition: var(--transicion);
        }

        .resultado-item:hover {
            background-color: var(--color-terciario);
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

        /* MENÚ LATERAL */
        .menu-lateral {
            width: 280px;
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
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--color-primario);
            margin-bottom: 10px;
        }

        .eslogan {
            font-size: 0.9rem;
            color: var(--color-texto);
            opacity: 0.8;
        }

        .menu-lateral ul {
            list-style: none;
            margin: 30px 0;
        }

        .menu-lateral li {
            margin-bottom: 12px;
        }

        .menu-lateral a {
            display: block;
            padding: 10px 15px;
            color: var(--color-texto);
            text-decoration: none;
            border-radius: 8px;
            transition: var(--transicion);
            font-size: 1rem;
            background-color: rgba(255,255,255,0.4);
        }

        .menu-lateral a:hover {
            background-color: white;
            transform: translateX(5px);
            box-shadow: var(--sombra);
        }

        .menu-lateral i {
            margin-right: 10px;
            width: 20px;
            text-align: center;
            color: var(--color-primario);
        }

        /* CONTENIDO PRINCIPAL */
        .contenido-principal {
            margin-left: 280px;
            padding: 30px 5%;
            margin-top: 65px;
        }

        /* Productos - AHORA MÁS PEQUEÑOS (3 POR FILA) */
        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .producto {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--sombra);
            transition: var(--transicion);
        }

        .producto:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.1);
        }

        .producto-imagen {
            height: 180px;
            overflow: hidden;
            position: relative;
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
            top: 10px;
            right: 10px;
            background-color: var(--color-destacado);
            color: white;
            padding: 4px 8px;
            border-radius: 15px;
            font-size: 0.7rem;
            font-weight: bold;
        }

        .producto-info {
            padding: 15px;
        }

        .producto h3 {
            color: var(--color-primario);
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .producto p {
            color: var(--color-texto);
            margin-bottom: 12px;
            font-size: 0.85rem;
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
            font-size: 1.1rem;
        }

        .btn-carrito {
            background-color: var(--color-secundario);
            color: var(--color-texto);
            border: none;
            padding: 6px 12px;
            border-radius: 15px;
            cursor: pointer;
            transition: var(--transicion);
            font-size: 0.8rem;
        }

        .btn-carrito:hover {
            background-color: var(--color-primario);
            color: white;
        }

        /* CARRITO MEJORADO */
        .carrito-modal {
            position: fixed;
            top: 0;
            right: -400px;
            width: 380px;
            height: 100vh;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            z-index: 1001;
            transition: var(--transicion);
            padding: 20px;
            overflow-y: auto;
        }

        .carrito-modal.activo {
            right: 0;
        }

        .carrito-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .carrito-header h3 {
            color: var(--color-primario);
            font-size: 1.3rem;
        }

        .cerrar-carrito {
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--color-texto);
            cursor: pointer;
        }

        .carrito-items {
            margin-bottom: 20px;
        }

        .carrito-item {
            display: flex;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px dashed #eee;
        }

        .carrito-item-img {
            width: 60px;
            height: 60px;
            object-fit: cover;
            border-radius: 8px;
            margin-right: 15px;
        }

        .carrito-item-info {
            flex: 1;
        }

        .carrito-item-titulo {
            font-size: 0.9rem;
            color: var(--color-primario);
            margin-bottom: 5px;
        }

        .carrito-item-precio {
            font-size: 0.9rem;
            color: var(--color-texto);
            margin-bottom: 5px;
        }

        .carrito-item-cantidad {
            display: flex;
            align-items: center;
        }

        .carrito-item-cantidad button {
            background: var(--color-terciario);
            border: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            cursor: pointer;
        }

        .carrito-item-cantidad span {
            margin: 0 10px;
        }

        .carrito-total {
            font-weight: bold;
            font-size: 1.1rem;
            text-align: right;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }

        .carrito-botones {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        .carrito-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            transition: var(--transicion);
        }

        .carrito-vaciar {
            background: #f5f5f5;
            color: #666;
        }

        .carrito-comprar {
            background: var(--color-primario);
            color: white;
        }

        .carrito-btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Overlay para el carrito */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.5);
            z-index: 1000;
            display: none;
        }

        .overlay.activo {
            display: block;
        }

        /* Responsive */
        @media (max-width: 1200px) {
            .menu-lateral {
                width: 250px;
            }
            .contenido-principal {
                margin-left: 250px;
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
            .seccion-productos {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            .carrito-modal {
                width: 100%;
                max-width: 380px;
            }
        }

        @media (max-width: 768px) {
            .encabezado-principal {
                flex-direction: column;
                gap: 15px;
                padding: 15px;
            }
            .busqueda-contenedor {
                width: 100%;
            }
            .seccion-productos {
                grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
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
            <input type="text" placeholder="Buscar productos..." id="input-busqueda">
            <button id="btn-buscar"><i class="fas fa-search"></i></button>
            <div class="resultados-busqueda" id="resultados-busqueda"></div>
        </div>
        <div class="carrito-icono" id="carrito-icono">
            <i class="fas fa-shopping-cart"></i>
            <span class="carrito-contador" id="carrito-contador">0</span>
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
            <div class="seccion-productos" id="contenedor-productos">
                <!-- Productos se cargan dinámicamente -->
            </div>
        </section>
    </main>

    <!-- Carrito de compras mejorado -->
    <div class="overlay" id="overlay"></div>
    <div class="carrito-modal" id="carrito-modal">
        <div class="carrito-header">
            <h3>Tu Carrito</h3>
            <button class="cerrar-carrito" id="cerrar-carrito">&times;</button>
        </div>
        <div class="carrito-items" id="carrito-items">
            <!-- Items del carrito se cargan aquí -->
            <p class="carrito-vacio">Tu carrito está vacío</p>
        </div>
        <div class="carrito-total" id="carrito-total">
            Total: $0
        </div>
        <div class="carrito-botones">
            <button class="carrito-btn carrito-vaciar" id="vaciar-carrito">Vaciar</button>
            <button class="carrito-btn carrito-comprar" id="comprar-carrito">Comprar</button>
        </div>
    </div>

    <script>
        // Base de datos de productos
        const productos = [
            {
                id: 1,
                nombre: "Vela de Lavanda",
                descripcion: "Aroma relajante para espacios íntimos",
                precio: 18000,
                imagen: "https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "velas"
            },
            {
                id: 2,
                nombre: "Centro de Mesa Floral",
                descripcion: "Combinación de velas y flores naturales",
                precio: 25000,
                imagen: "https://images.unsplash.com/photo-1513151233558-d860c5398176?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "decoracion"
            },
            {
                id: 3,
                nombre: "Ramo de Novia Clásico",
                descripcion: "Elegante ramo con rosas blancas",
                precio: 28000,
                imagen: "https://images.unsplash.com/photo-1499209974431-9dddcece7f88?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "ramos"
            },
            {
                id: 4,
                nombre: "Recuerdo de Boda",
                descripcion: "Mini velas personalizadas",
                precio: 9500,
                imagen: "https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "recuerdos"
            },
            {
                id: 5,
                nombre: "Juego de Velas Aromáticas",
                descripcion: "Set de 3 velas con diferentes aromas",
                precio: 22000,
                imagen: "https://images.unsplash.com/photo-1594223274511-4c1a2898a846?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "velas"
            },
            {
                id: 6,
                nombre: "Caja de Recuerdos Premium",
                descripcion: "Elegante caja con velas y fotos",
                precio: 32000,
                imagen: "https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                categoria: "recuerdos"
            }
        ];

        // Variables globales
        let carrito = [];
        const contenedorProductos = document.getElementById('contenedor-productos');
        const inputBusqueda = document.getElementById('input-busqueda');
        const resultadosBusqueda = document.getElementById('resultados-busqueda');
        const carritoIcono = document.getElementById('carrito-icono');
        const carritoModal = document.getElementById('carrito-modal');
        const overlay = document.getElementById('overlay');
        const cerrarCarrito = document.getElementById('cerrar-carrito');
        const carritoItems = document.getElementById('carrito-items');
        const carritoTotal = document.getElementById('carrito-total');
        const vaciarCarritoBtn = document.getElementById('vaciar-carrito');
        const comprarCarritoBtn = document.getElementById('comprar-carrito');
        const contadorCarrito = document.getElementById('carrito-contador');

        // Cargar productos al iniciar
        document.addEventListener('DOMContentLoaded', () => {
            renderizarProductos(productos);
            
            // Cargar carrito desde localStorage
            const carritoGuardado = localStorage.getItem('carrito');
            if (carritoGuardado) {
                carrito = JSON.parse(carritoGuardado);
                actualizarCarrito();
            }
        });

        // Renderizar productos
        function renderizarProductos(productos) {
            contenedorProductos.innerHTML = '';
            
            productos.forEach(producto => {
                const productoHTML = `
                    <div class="producto" data-id="${producto.id}">
                        <div class="producto-imagen">
                            <img src="${producto.imagen}" alt="${producto.nombre}">
                        </div>
                        <div class="producto-info">
                            <h3>${producto.nombre}</h3>
                            <p>${producto.descripcion}</p>
                            <div class="producto-precio">
                                <span class="precio">$${producto.precio.toLocaleString()}</span>
                                <button class="btn-carrito" data-id="${producto.id}">
                                    <i class="fas fa-cart-plus"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                `;
                contenedorProductos.insertAdjacentHTML('beforeend', productoHTML);
            });
            
            // Agregar eventos a los botones
            document.querySelectorAll('.btn-carrito').forEach(btn => {
                btn.addEventListener('click', agregarAlCarrito);
            });
        }

        // Búsqueda mejorada
        inputBusqueda.addEventListener('input', function() {
            const termino = this.value.trim().toLowerCase();
            
            if (termino.length > 0) {
                const resultados = productos.filter(producto => 
                    producto.nombre.toLowerCase().includes(termino) || 
                    producto.descripcion.toLowerCase().includes(termino) ||
                    producto.categoria.toLowerCase().includes(termino)
                );
                
                mostrarResultadosBusqueda(resultados);
            } else {
                resultadosBusqueda.style.display = 'none';
            }
        });

        function mostrarResultadosBusqueda(resultados) {
            if (resultados.length > 0) {
                resultadosBusqueda.innerHTML = '';
                
                resultados.forEach(producto => {
                    const resultadoHTML = `
                        <div class="resultado-item" data-id="${producto.id}">
                            <strong>${producto.nombre}</strong>
                            <p>${producto.descripcion}</p>
                            <small>$${producto.precio.toLocaleString()}</small>
                        </div>
                    `;
                    resultadosBusqueda.insertAdjacentHTML('beforeend', resultadoHTML);
                });
                
                resultadosBusqueda.style.display = 'block';
                
                // Agregar eventos a los resultados
                document.querySelectorAll('.resultado-item').forEach(item => {
                    item.addEventListener('click', function() {
                        const id = parseInt(this.getAttribute('data-id'));
                        const producto = productos.find(p => p.id === id);
                        if (producto) {
                            inputBusqueda.value = producto.nombre;
                            resultadosBusqueda.style.display = 'none';
                            
                            // Desplazar al producto
                            const productoElement = document.querySelector(`.producto[data-id="${id}"]`);
                            if (productoElement) {
                                productoElement.scrollIntoView({ behavior: 'smooth', block: 'center' });
                                productoElement.classList.add('destacado');
                                setTimeout(() => {
                                    productoElement.classList.remove('destacado');
                                }, 2000);
                            }
                        }
                    });
                });
            } else {
                resultadosBusqueda.innerHTML = '<div class="resultado-item">No se encontraron resultados</div>';
                resultadosBusqueda.style.display = 'block';
            }
        }

        // Cerrar resultados al hacer clic fuera
        document.addEventListener('click', function(e) {
            if (!inputBusqueda.contains(e.target) {
                resultadosBusqueda.style.display = 'none';
            }
        });

        // Carrito de compras mejorado
        function agregarAlCarrito(e) {
            const id = parseInt(e.currentTarget.getAttribute('data-id'));
            const producto = productos.find(p => p.id === id);
            
            if (producto) {
                const productoEnCarrito = carrito.find(item => item.id === id);
                
                if (productoEnCarrito) {
                    productoEnCarrito.cantidad++;
                } else {
                    carrito.push({
                        ...producto,
                        cantidad: 1
                    });
                }
                
                actualizarCarrito();
                
                // Animación de confirmación
                const icono = e.currentTarget.querySelector('i');
                icono.classList.remove('fa-cart-plus');
                icono.classList.add('fa-check');
                
                setTimeout(() => {
                    icono.classList.remove('fa-check');
                    icono.classList.add('fa-cart-plus');
                }, 1000);
            }
        }

        function actualizarCarrito() {
            // Guardar en localStorage
            localStorage.setItem('carrito', JSON.stringify(carrito));
            
            // Actualizar contador
            contadorCarrito.textContent = carrito.reduce((total, item) => total + item.cantidad, 0);
            
            // Actualizar modal del carrito
            carritoItems.innerHTML = '';
            
            if (carrito.length === 0) {
                carritoItems.innerHTML = '<p class="carrito-vacio">Tu carrito está vacío</p>';
                carritoTotal.textContent = 'Total: $0';
                return;
            }
            
            let total = 0;
            
            carrito.forEach(item => {
                const subtotal = item.precio * item.cantidad;
                total += subtotal;
                
                const itemHTML = `
                    <div class="carrito-item" data-id="${item.id}">
                        <img src="${item.imagen}" alt="${item.nombre}" class="carrito-item-img">
                        <div class="carrito-item-info">
                            <h4 class="carrito-item-titulo">${item.nombre}</h4>
                            <p class="carrito-item-precio">$${item.precio.toLocaleString()}</p>
                            <div class="carrito-item-cantidad">
                                <button class="btn-disminuir">-</button>
                                <span>${item.cantidad}</span>
                                <button class="btn-aumentar">+</button>
                            </div>
                        </div>
                    </div>
                `;
                carritoItems.insertAdjacentHTML('beforeend', itemHTML);
            });
            
            // Actualizar total
            carritoTotal.textContent = `Total: $${total.toLocaleString()}`;
            
            // Agregar eventos a los botones de cantidad
            document.querySelectorAll('.btn-disminuir').forEach(btn => {
                btn.addEventListener('click', function() {
                    const id = parseInt(this.closest('.carrito-item').getAttribute('data-id'));
                    const item = carrito.find(item => item.id === id);
                    
                    if (item.cantidad > 1) {
                        item.cantidad--;
                    } else {
                        carrito = carrito.filter(item => item.id !== id);
                    }
                    
                    actualizarCarrito();
                });
            });
            
            document.querySelectorAll('.btn-aumentar').forEach(btn => {
                btn.addEventListener('click', function() {
                    const id = parseInt(this.closest('.carrito-item').getAttribute('data-id'));
                    const item = carrito.find(item => item.id === id);
                    item.cantidad++;
                    actualizarCarrito();
                });
            });
        }

        // Abrir/cerrar carrito
        carritoIcono.addEventListener('click', function() {
            carritoModal.classList.add('activo');
            overlay.classList.add('activo');
            document.body.style.overflow = 'hidden';
        });

        cerrarCarrito.addEventListener('click', function() {
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });

        overlay.addEventListener('click', function() {
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });

        // Vaciar carrito
        vaciarCarritoBtn.addEventListener('click', function() {
            carrito = [];
            actualizarCarrito();
        });

        // Comprar
        comprarCarritoBtn.addEventListener('click', function() {
            if (carrito.length === 0) {
                alert('Tu carrito está vacío');
                return;
            }
            
            alert(`¡Compra realizada por $${carrito.reduce((total, item) => total + (item.precio * item.cantidad), 0).toLocaleString()}!\nGracias por tu compra.`);
            carrito = [];
            actualizarCarrito();
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });
    </script>
</body>
</html>
