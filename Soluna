<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="SOLUN - Artesanías en velas, decoración y recuerdos para eventos. Productos únicos y personalizados para bodas, cumpleaños y ocasiones especiales.">
    <meta name="keywords" content="velas artesanales, decoración eventos, recuerdos para bodas, centros de mesa, regalos personalizados">
    <title>SOLUN - Recuerdos y Decoración Artesanal para Eventos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css">
    <style>
        :root {
            --color-primario: #8B5A2B;
            --color-secundario: #D2B48C;
            --color-terciario: #F5DEB3;
            --color-destacado: #A0522D;
            --color-texto: #5C4033;
            --borde-decorativo: #CD853F;
            --fondo-body: #FFF8DC;
            --sombra: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transicion: all 0.3s ease;
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
            line-height: 1.6;
        }

        /* Encabezado mejorado */
        .encabezado-principal {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background-color: var(--color-terciario);
            position: fixed;
            top: 4px;
            left: 0;
            right: 0;
            z-index: 999;
            box-shadow: var(--sombra);
            border-bottom: 1px solid var(--borde-decorativo);
        }

        .titulo-encabezado h1 {
            font-size: 1.8rem;
            color: var(--color-primario);
            white-space: nowrap;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .busqueda-contenedor {
            width: 300px;
            display: flex;
            margin-left: 20px;
            position: relative;
        }

        .busqueda-contenedor input {
            width: 100%;
            padding: 10px 20px;
            border: 1px solid var(--borde-decorativo);
            border-radius: 30px;
            outline: none;
            background-color: rgba(255,255,255,0.8);
            transition: var(--transicion);
            font-size: 0.9rem;
        }

        .busqueda-contenedor input:focus {
            box-shadow: 0 0 0 2px var(--color-destacado);
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
            font-size: 1rem;
            transition: var(--transicion);
        }

        .busqueda-contenedor button:hover {
            color: var(--color-destacado);
        }

        .carrito-icono {
            position: relative;
            margin-left: 20px;
            font-size: 1.3rem;
            color: var(--color-primario);
            cursor: pointer;
            transition: var(--transicion);
        }

        .carrito-icono:hover {
            color: var(--color-destacado);
        }

        .carrito-contador {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--color-destacado);
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 0.7rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Contenedor principal */
        .contenedor-general {
            display: flex;
            margin-top: 80px; /* Compensa encabezado */
        }

        /* Menú lateral mejorado */
        .menu-lateral {
            width: 250px;
            background-color: var(--color-secundario);
            padding: 25px 20px;
            border-right: 1px solid var(--borde-decorativo);
            position: sticky;
            top: 80px;
            align-self: flex-start;
            height: calc(100vh - 80px);
            overflow-y: auto;
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
            font-weight: bold;
            color: var(--color-primario);
            letter-spacing: 2px;
            margin-bottom: 5px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .eslogan {
            font-size: 0.85rem;
            color: var(--color-destacado);
            font-style: italic;
            line-height: 1.4;
        }

        .menu-lateral ul {
            list-style: none;
            margin-bottom: 30px;
        }

        .menu-lateral li {
            margin-bottom: 15px;
        }

        .menu-lateral a {
            color: var(--color-texto);
            text-decoration: none;
            font-size: 0.95rem;
            transition: var(--transicion);
            display: block;
            padding: 10px 15px;
            border-radius: 15px;
            background-color: rgba(255, 255, 255, 0.3);
            position: relative;
            overflow: hidden;
        }

        .menu-lateral a::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: var(--transicion);
        }

        .menu-lateral a:hover {
            background-color: var(--color-terciario);
            transform: translateX(8px);
            box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
        }

        .menu-lateral a:hover::before {
            left: 100%;
        }

        .menu-lateral i {
            margin-right: 10px;
            width: 20px;
            text-align: center;
        }

        .contacto-menu {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px dashed var(--color-primario);
        }

        .contacto-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 0.9rem;
            transition: var(--transicion);
        }

        .contacto-item:hover {
            transform: translateX(5px);
        }

        .contacto-item i {
            margin-right: 12px;
            color: var(--color-destacado);
            font-size: 1rem;
        }

        .redes-sociales {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 25px;
        }

        .redes-sociales a {
            color: var(--color-primario);
            font-size: 1.3rem;
            transition: var(--transicion);
            display: inline-block;
        }

        .redes-sociales a:hover {
            transform: translateY(-3px) scale(1.1);
            color: var(--color-destacado);
        }

        /* Contenido principal mejorado */
        .contenido-principal {
            flex: 1;
            padding: 30px 5%;
        }

        .seccion-bienvenida {
            background: linear-gradient(135deg, var(--color-terciario), var(--color-secundario));
            color: var(--color-texto);
            padding: 40px;
            text-align: center;
            margin-bottom: 40px;
            border-radius: 10px;
            border: 1px solid var(--borde-decorativo);
            box-shadow: var(--sombra);
            position: relative;
            overflow: hidden;
        }

        .seccion-bienvenida::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            animation: rotate 15s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .seccion-bienvenida h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
            color: var(--color-primario);
            position: relative;
        }

        .seccion-bienvenida p {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto;
            position: relative;
        }

        .seccion-bienvenida .btn-destacado {
            display: inline-block;
            margin-top: 20px;
            padding: 12px 25px;
            background-color: var(--color-primario);
            color: white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: var(--transicion);
            position: relative;
            overflow: hidden;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .seccion-bienvenida .btn-destacado:hover {
            background-color: var(--color-destacado);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        .seccion-bienvenida .btn-destacado::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            transform: translateX(-100%);
            transition: 0.6s;
        }

        .seccion-bienvenida .btn-destacado:hover::after {
            transform: translateX(100%);
        }

        .seccion-titulo {
            font-size: 1.8rem;
            color: var(--color-primario);
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--borde-decorativo);
            position: relative;
        }

        .seccion-titulo::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100px;
            height: 2px;
            background-color: var(--color-destacado);
        }

        .seccion-productos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .producto {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--sombra);
            transition: var(--transicion);
            border: 1px solid var(--borde-decorativo);
            position: relative;
        }

        .producto:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .producto-imagen {
            width: 100%;
            height: 250px;
            position: relative;
            overflow: hidden;
        }

        .producto img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-bottom: 1px solid var(--borde-decorativo);
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
            z-index: 1;
        }

        .producto-acciones {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: rgba(0,0,0,0.7);
            display: flex;
            justify-content: center;
            padding: 15px 0;
            transform: translateY(100%);
            transition: var(--transicion);
        }

        .producto:hover .producto-acciones {
            transform: translateY(0);
        }

        .producto-acciones button {
            background-color: var(--color-terciario);
            color: var(--color-texto);
            border: none;
            padding: 8px 15px;
            margin: 0 5px;
            border-radius: 20px;
            cursor: pointer;
            transition: var(--transicion);
            display: flex;
            align-items: center;
        }

        .producto-acciones button:hover {
            background-color: var(--color-primario);
            color: white;
        }

        .producto-acciones i {
            margin-right: 5px;
        }

        .producto-info {
            padding: 20px;
        }

        .producto h3 {
            margin-bottom: 12px;
            color: var(--color-primario);
            font-size: 1.2rem;
        }

        .producto p {
            color: var(--color-destacado);
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .producto-precio {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .precio {
            font-weight: bold;
            color: var(--color-primario);
            font-size: 1.2rem;
        }

        .precio-oferta {
            text-decoration: line-through;
            color: #999;
            font-size: 0.9rem;
            margin-right: 10px;
        }

        .btn-carrito {
            background-color: var(--color-secundario);
            color: var(--color-texto);
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            transition: var(--transicion);
            display: flex;
            align-items: center;
        }

        .btn-carrito:hover {
            background-color: var(--color-primario);
            color: white;
        }

        /* Galería de testimonios */
        .testimonios {
            margin: 50px 0;
        }

        .testimonios-contenedor {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }

        .testimonio {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: var(--sombra);
            border: 1px solid var(--borde-decorativo);
        }

        .testimonio-texto {
            font-style: italic;
            margin-bottom: 15px;
            position: relative;
        }

        .testimonio-texto::before,
        .testimonio-texto::after {
            content: '"';
            font-size: 2rem;
            color: var(--color-secundario);
            opacity: 0.5;
            position: absolute;
        }

        .testimonio-texto::before {
            top: -10px;
            left: -10px;
        }

        .testimonio-texto::after {
            bottom: -20px;
            right: -10px;
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

        .testimonio-info h4 {
            color: var(--color-primario);
            margin-bottom: 5px;
        }

        .testimonio-info p {
            color: var(--color-destacado);
            font-size: 0.8rem;
        }

        /* Carrito de compras */
        .carrito-modal {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            width: 350px;
            height: 100%;
            background-color: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            z-index: 1001;
            overflow-y: auto;
            transform: translateX(100%);
            transition: transform 0.3s ease;
        }

        .carrito-modal.activo {
            transform: translateX(0);
            display: block;
        }

        .carrito-cabecera {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            background-color: var(--color-terciario);
            border-bottom: 1px solid var(--borde-decorativo);
        }

        .carrito-cabecera h3 {
            color: var(--color-primario);
            margin: 0;
        }

        .cerrar-carrito {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--color-primario);
        }

        .carrito-contenido {
            padding: 20px;
        }

        .carrito-item {
            display: flex;
            margin-bottom: 20px;
            padding-bottom: 20px;
            border-bottom: 1px dashed var(--borde-decorativo);
        }

        .carrito-item-img {
            width: 70px;
            height: 70px;
            object-fit: cover;
            border-radius: 5px;
            margin-right: 15px;
            border: 1px solid var(--borde-decorativo);
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
            color: var(--color-destacado);
            margin-bottom: 5px;
        }

        .carrito-item-cantidad {
            display: flex;
            align-items: center;
        }

        .carrito-item-cantidad button {
            background-color: var(--color-secundario);
            border: none;
            width: 25px;
            height: 25px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .carrito-item-cantidad span {
            margin: 0 10px;
        }

        .carrito-total {
            padding: 20px;
            border-top: 1px solid var(--borde-decorativo);
            text-align: right;
            font-weight: bold;
            color: var(--color-primario);
            font-size: 1.1rem;
        }

        .carrito-botones {
            display: flex;
            justify-content: space-between;
            padding: 0 20px 20px;
        }

        .carrito-boton {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: var(--transicion);
        }

        .carrito-vaciar {
            background-color: #f5f5f5;
            color: #666;
        }

        .carrito-comprar {
            background-color: var(--color-primario);
            color: white;
        }

        .carrito-boton:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Pie de página mejorado */
        .pie-pagina {
            background: linear-gradient(to right, var(--color-primario), var(--color-destacado));
            color: white;
            padding: 40px 5%;
            margin-top: 50px;
            text-align: center;
            border-radius: 10px 10px 0 0;
        }

        .pie-contenedor {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            text-align: left;
            max-width: 1200px;
            margin: 0 auto;
        }

        .pie-columna h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .pie-columna h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--color-terciario);
        }

        .pie-columna ul {
            list-style: none;
        }

        .pie-columna li {
            margin-bottom: 10px;
        }

        .pie-columna a {
            color: var(--color-terciario);
            text-decoration: none;
            transition: var(--transicion);
            display: inline-block;
        }

        .pie-columna a:hover {
            color: white;
            transform: translateX(5px);
        }

        .pie-columna i {
            margin-right: 8px;
            width: 20px;
            text-align: center;
        }

        .pie-copyright {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.2);
            font-size: 0.9rem;
        }

        /* Overlay para el carrito */
        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0,0,0,0.5);
            z-index: 1000;
        }

        .overlay.activo {
            display: block;
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }

        /* Botón flotante de WhatsApp */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            text-align: center;
            font-size: 1.8rem;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transicion);
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 15px rgba(0,0,0,0.3);
        }

        /* Formulario de contacto */
        .formulario-contacto {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--sombra);
            border: 1px solid var(--borde-decorativo);
            max-width: 800px;
            margin: 40px auto;
        }

        .form-grupo {
            margin-bottom: 20px;
        }

        .form-grupo label {
            display: block;
            margin-bottom: 8px;
            color: var(--color-primario);
            font-weight: bold;
        }

        .form-grupo input,
        .form-grupo textarea,
        .form-grupo select {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--borde-decorativo);
            border-radius: 5px;
            font-size: 1rem;
            transition: var(--transicion);
        }

        .form-grupo input:focus,
        .form-grupo textarea:focus,
        .form-grupo select:focus {
            outline: none;
            border-color: var(--color-primario);
            box-shadow: 0 0 0 2px rgba(139, 90, 43, 0.2);
        }

        .form-grupo textarea {
            min-height: 150px;
            resize: vertical;
        }

        .form-submit {
            background-color: var(--color-primario);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: var(--transicion);
            display: inline-block;
        }

        .form-submit:hover {
            background-color: var(--color-destacado);
            transform: translateY(-2px);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .contenedor-general {
                flex-direction: column;
            }
            
            .menu-lateral {
                width: 100%;
                position: relative;
                top: 0;
                height: auto;
                padding: 20px;
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
                padding: 20px;
            }

            .carrito-modal {
                width: 100%;
            }
        }

        @media (max-width: 768px) {
            .seccion-productos {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }

            .seccion-bienvenida {
                padding: 30px 20px;
            }

            .seccion-bienvenida h2 {
                font-size: 1.8rem;
            }

            .testimonios-contenedor {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .producto-acciones {
                position: static;
                transform: none;
                background-color: var(--color-terciario);
                justify-content: space-around;
                padding: 10px 0;
            }

            .producto:hover {
                transform: none;
            }

            .whatsapp-float {
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
                bottom: 20px;
                right: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Línea decorativa superior -->
    <div class="linea-decorativa"></div>

    <!-- Encabezado con búsqueda y carrito -->
    <header class="encabezado-principal">
        <div class="titulo-encabezado">
            <h1>SOLUN</h1>
        </div>
        <div class="busqueda-contenedor">
            <input type="text" placeholder="Buscar productos...">
            <button><i class="fas fa-search"></i></button>
        </div>
        <div class="carrito-icono" id="carrito-icono">
            <i class="fas fa-shopping-cart"></i>
            <span class="carrito-contador">0</span>
        </div>
    </header>

    <!-- Contenedor principal -->
    <div class="contenedor-general">
        <!-- Menú lateral -->
        <nav class="menu-lateral">
            <div class="logo-container">
                <div class="logo">SOLUN</div>
                <div class="eslogan">Artesanías en velas y decoración para tus eventos especiales</div>
            </div>
            
            <ul>
                <li><a href="#inicio"><i class="fas fa-home"></i> Inicio</a></li>
                <li><a href="#productos"><i class="fas fa-fire"></i> Nuestros Productos</a></li>
                <li><a href="#testimonios"><i class="fas fa-star"></i> Testimonios</a></li>
                <li><a href="#contacto"><i class="fas fa-envelope"></i> Contacto</a></li>
                <li><a href="#nosotros"><i class="fas fa-info-circle"></i> Sobre Nosotros</a></li>
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
                <div class="contacto-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Guadalajara, Jalisco</span>
                </div>
            </div>

            <div class="redes-sociales">
                <a href="#" target="_blank" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" target="_blank" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                <a href="#" target="_blank" aria-label="Pinterest"><i class="fab fa-pinterest"></i></a>
            </div>
        </nav>

        <!-- Contenido principal -->
        <main class="contenido-principal">
            <section class="seccion-bienvenida" id="inicio">
                <h2>Bienvenidos a SOLUN</h2>
                <p>Creaciones artesanales únicas que transforman tus eventos en momentos inolvidables. Especialistas en velas aromáticas, decoración floral y recuerdos personalizados.</p>
                <button class="btn-destacado">Ver Catálogo Completo</button>
            </section>

            <section id="productos">
                <h2 class="seccion-titulo">Nuestros Productos Destacados</h2>
                <div class="seccion-productos">
                    <!-- Producto 1 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <span class="producto-badge">Nuevo</span>
                            <img src="https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Vela aromática de lavanda">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="1"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="1"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Vela de Lavanda</h3>
                            <p>Aroma relajante para espacios íntimos, elaborada con cera de soja y esencia natural.</p>
                            <div class="producto-precio">
                                <span class="precio">$18.000</span>
                                <button class="btn-carrito" data-id="1"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>

                    <!-- Producto 2 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <span class="producto-badge">Más vendido</span>
                            <img src="https://images.unsplash.com/photo-1513151233558-d860c5398176?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Centro de mesa floral">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="2"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="2"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Centro de Mesa Floral</h3>
                            <p>Combinación de velas y flores naturales para decoración de bodas y eventos.</p>
                            <div class="producto-precio">
                                <span class="precio">$25.000</span>
                                <button class="btn-carrito" data-id="2"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>

                    <!-- Producto 3 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <img src="https://images.unsplash.com/photo-1499209974431-9dddcece7f88?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Ramo de novia">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="3"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="3"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Ramo de Novia Clásico</h3>
                            <p>Elegante ramo con rosas blancas y detalles de encaje para el día de tu boda.</p>
                            <div class="producto-precio">
                                <span class="precio-oferta">$35.000</span>
                                <span class="precio">$28.000</span>
                                <button class="btn-carrito" data-id="3"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>

                    <!-- Producto 4 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <span class="producto-badge">Oferta</span>
                            <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Recuerdo de boda">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="4"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="4"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Recuerdo de Boda</h3>
                            <p>Mini velas personalizadas con nombres de los novios y fecha de la boda.</p>
                            <div class="producto-precio">
                                <span class="precio-oferta">$12.000</span>
                                <span class="precio">$9.500</span>
                                <button class="btn-carrito" data-id="4"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>

                    <!-- Producto 5 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <img src="https://images.unsplash.com/photo-1594223274511-4c1a2898a846?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Juego de velas">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="5"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="5"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Juego de Velas Aromáticas</h3>
                            <p>Set de 3 velas con diferentes aromas: vainilla, canela y naranja.</p>
                            <div class="producto-precio">
                                <span class="precio">$22.000</span>
                                <button class="btn-carrito" data-id="5"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>

                    <!-- Producto 6 -->
                    <div class="producto">
                        <div class="producto-imagen">
                            <span class="producto-badge">Personalizable</span>
                            <img src="https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Caja de recuerdos">
                            <div class="producto-acciones">
                                <button class="btn-ver" data-id="6"><i class="fas fa-eye"></i> Ver</button>
                                <button class="btn-carrito" data-id="6"><i class="fas fa-cart-plus"></i> Añadir</button>
                            </div>
                        </div>
                        <div class="producto-info">
                            <h3>Caja de Recuerdos Premium</h3>
                            <p>Elegante caja con velas, fotos y detalles personalizados para invitados especiales.</p>
                            <div class="producto-precio">
                                <span class="precio">$32.000</span>
                                <button class="btn-carrito" data-id="6"><i class="fas fa-cart-plus"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Sección de testimonios -->
            <section class="testimonios" id="testimonios">
                <h2 class="seccion-titulo">Lo que dicen nuestros clientes</h2>
                <div class="testimonios-contenedor">
                    <div class="testimonio">
                        <div class="testimonio-texto">
                            Las velas aromáticas de SOLUN transformaron completamente la atmósfera de mi boda. El aroma era perfecto y todos mis invitados preguntaban dónde las había comprado.
                        </div>
                        <div class="testimonio-autor">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="María González">
                            <div class="testimonio-info">
                                <h4>María González</h4>
                                <p>Boda en Guadalajara</p>
                            </div>
                        </div>
                    </div>

                    <div class="testimonio">
                        <div class="testimonio-texto">
                            El centro de mesa que encargué superó todas mis expectativas. La calidad de las flores y la combinación con las velas fue exactamente lo que quería para mi aniversario.
                        </div>
                        <div class="testimonio-autor">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Carlos Mendoza">
                            <div class="testimonio-info">
                                <h4>Carlos Mendoza</h4>
                                <p>25° Aniversario</p>
                            </div>
                        </div>
                    </div>

                    <div class="testimonio">
                        <div class="testimonio-texto">
                            Los recuerdos personalizados para los invitados de mi boda fueron un éxito absoluto. SOLUN captó perfectamente el estilo que quería y la atención al cliente fue excepcional.
                        </div>
                        <div class="testimonio-autor">
                            <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Ana Torres">
                            <div class="testimonio-info">
                                <h4>Ana Torres</h4>
                                <p>Boda en Tlaquepaque</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Sección de contacto -->
            <section class="formulario-contacto" id="contacto">
                <h2 class="seccion-titulo">Contáctanos</h2>
                <form id="contacto-form">
                    <div class="form-grupo">
                        <label for="nombre">Nombre completo</label>
                        <input type="text" id="nombre" name="nombre" required>
                    </div>

                    <div class="form-grupo">
                        <label for="email">Correo electrónico</label>
                        <input type="email" id="email" name="email" required>
                    </div>

                    <div class="form-grupo">
                        <label for="telefono">Teléfono</label>
                        <input type="tel" id="telefono" name="telefono">
                    </div>

                    <div class="form-grupo">
                        <label for="evento">Tipo de evento</label>
                        <select id="evento" name="evento">
                            <option value="">Selecciona una opción</option>
                            <option value="boda">Boda</option>
                            <option value="cumpleanos">Cumpleaños</option>
                            <option value="aniversario">Aniversario</option>
                            <option value="baby-shower">Baby Shower</option>
                            <option value="otro">Otro</option>
                        </select>
                    </div>

                    <div class="form-grupo">
                        <label for="mensaje">Mensaje</label>
                        <textarea id="mensaje" name="mensaje" required></textarea>
                    </div>

                    <button type="submit" class="form-submit">Enviar Mensaje</button>
                </form>
            </section>

            <!-- Pie de página -->
            <footer class="pie-pagina">
                <div class="pie-contenedor">
                    <div class="pie-columna">
                        <h3>SOLUN</h3>
                        <p>Artesanías en velas y decoración para eventos especiales. Creando momentos memorables desde 2018.</p>
                        <div class="redes-sociales">
                            <a href="#" target="_blank" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
                            <a href="#" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                            <a href="#" target="_blank" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                        </div>
                    </div>

                    <div class="pie-columna">
                        <h3>Enlaces rápidos</h3>
                        <ul>
                            <li><a href="#inicio"><i class="fas fa-chevron-right"></i> Inicio</a></li>
                            <li><a href="#productos"><i class="fas fa-chevron-right"></i> Productos</a></li>
                            <li><a href="#testimonios"><i class="fas fa-chevron-right"></i> Testimonios</a></li>
                            <li><a href="#contacto"><i class="fas fa-chevron-right"></i> Contacto</a></li>
                            <li><a href="#nosotros"><i class="fas fa-chevron-right"></i> Sobre nosotros</a></li>
                        </ul>
                    </div>

                    <div class="pie-columna">
                        <h3>Contacto</h3>
                        <ul>
                            <li><a href="tel:+523351069229"><i class="fas fa-phone"></i> 335 106 9229</a></li>
                            <li><a href="mailto:solunaclientes@gmail.com"><i class="fas fa-envelope"></i> solunaclientes@gmail.com</a></li>
                            <li><i class="fas fa-map-marker-alt"></i> Guadalajara, Jalisco, México</li>
                            <li><i class="fas fa-clock"></i> Lunes a Sábado: 10am - 7pm</li>
                        </ul>
                    </div>
                </div>

                <div class="pie-copyright">
                    <p>&copy; 2023 SOLUN - Recuerdos y Decoración para Eventos | Todos los derechos reservados</p>
                </div>
            </footer>
        </main>
    </div>

    <!-- Carrito de compras -->
    <div class="overlay" id="overlay"></div>
    <div class="carrito-modal" id="carrito-modal">
        <div class="carrito-cabecera">
            <h3>Tu Carrito</h3>
            <button class="cerrar-carrito" id="cerrar-carrito">&times;</button>
        </div>
        <div class="carrito-contenido" id="carrito-contenido">
            <!-- Los productos del carrito se añadirán aquí dinámicamente -->
            <p class="carrito-vacio">Tu carrito está vacío</p>
        </div>
        <div class="carrito-total" id="carrito-total">
            Total: $0
        </div>
        <div class="carrito-botones">
            <button class="carrito-boton carrito-vaciar" id="vaciar-carrito">Vaciar Carrito</button>
            <button class="carrito-boton carrito-comprar" id="comprar-carrito">Finalizar Compra</button>
        </div>
    </div>

    <!-- Botón flotante de WhatsApp -->
    <a href="https://wa.me/523351069229" class="whatsapp-float" target="_blank" aria-label="Contactar por WhatsApp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Lightbox para imágenes de productos (se añade dinámicamente) -->
    <div id="producto-lightbox" class="lightbox">
        <span class="lightbox-close">&times;</span>
        <div class="lightbox-content">
            <img id="lightbox-imagen" src="" alt="">
            <div class="lightbox-info">
                <h3 id="lightbox-titulo"></h3>
                <p id="lightbox-descripcion"></p>
                <div class="lightbox-precio" id="lightbox-precio"></div>
                <button class="btn-carrito" id="lightbox-comprar">Añadir al carrito</button>
            </div>
        </div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/js/lightbox.min.js"></script>
    <script>
        // Carrito de compras
        const carrito = [];
        const carritoIcono = document.getElementById('carrito-icono');
        const carritoModal = document.getElementById('carrito-modal');
        const overlay = document.getElementById('overlay');
        const cerrarCarrito = document.getElementById('cerrar-carrito');
        const carritoContenido = document.getElementById('carrito-contenido');
        const carritoTotal = document.getElementById('carrito-total');
        const vaciarCarritoBtn = document.getElementById('vaciar-carrito');
        const comprarCarritoBtn = document.getElementById('comprar-carrito');
        const contadorCarrito = document.querySelector('.carrito-contador');

        // Productos disponibles
        const productos = [
            {
                id: 1,
                nombre: "Vela de Lavanda",
                descripcion: "Aroma relajante para espacios íntimos, elaborada con cera de soja y esencia natural.",
                precio: 18000,
                imagen: "https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            },
            {
                id: 2,
                nombre: "Centro de Mesa Floral",
                descripcion: "Combinación de velas y flores naturales para decoración de bodas y eventos.",
                precio: 25000,
                imagen: "https://images.unsplash.com/photo-1513151233558-d860c5398176?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            },
            {
                id: 3,
                nombre: "Ramo de Novia Clásico",
                descripcion: "Elegante ramo con rosas blancas y detalles de encaje para el día de tu boda.",
                precio: 28000,
                precioOriginal: 35000,
                imagen: "https://images.unsplash.com/photo-1499209974431-9dddcece7f88?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            },
            {
                id: 4,
                nombre: "Recuerdo de Boda",
                descripcion: "Mini velas personalizadas con nombres de los novios y fecha de la boda.",
                precio: 9500,
                precioOriginal: 12000,
                imagen: "https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            },
            {
                id: 5,
                nombre: "Juego de Velas Aromáticas",
                descripcion: "Set de 3 velas con diferentes aromas: vainilla, canela y naranja.",
                precio: 22000,
                imagen: "https://images.unsplash.com/photo-1594223274511-4c1a2898a846?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            },
            {
                id: 6,
                nombre: "Caja de Recuerdos Premium",
                descripcion: "Elegante caja con velas, fotos y detalles personalizados para invitados especiales.",
                precio: 32000,
                imagen: "https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
            }
        ];

        // Abrir carrito
        carritoIcono.addEventListener('click', () => {
            carritoModal.classList.add('activo');
            overlay.classList.add('activo');
            document.body.style.overflow = 'hidden';
        });

        // Cerrar carrito
        cerrarCarrito.addEventListener('click', () => {
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });

        overlay.addEventListener('click', () => {
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });

        // Añadir producto al carrito
        document.querySelectorAll('.btn-carrito').forEach(btn => {
            btn.addEventListener('click', (e) => {
                const id = parseInt(e.target.getAttribute('data-id') || e.target.closest('.btn-carrito').getAttribute('data-id'));
                const producto = productos.find(p => p.id === id);
                
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
                
                // Animación del icono del carrito
                const icono = e.target.closest('.btn-carrito').querySelector('i') || e.target;
                icono.classList.remove('fa-cart-plus');
                icono.classList.add('fa-check');
                
                setTimeout(() => {
                    icono.classList.remove('fa-check');
                    icono.classList.add('fa-cart-plus');
                }, 1000);
            });
        });

        // Actualizar carrito
        function actualizarCarrito() {
            carritoContenido.innerHTML = '';
            
            if (carrito.length === 0) {
                carritoContenido.innerHTML = '<p class="carrito-vacio">Tu carrito está vacío</p>';
                carritoTotal.textContent = 'Total: $0';
                contadorCarrito.textContent = '0';
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
                
                carritoContenido.insertAdjacentHTML('beforeend', itemHTML);
            });
            
            // Actualizar total y contador
            carritoTotal.textContent = `Total: $${total.toLocaleString()}`;
            contadorCarrito.textContent = carrito.reduce((sum, item) => sum + item.cantidad, 0);
            
            // Añadir eventos a los botones de cantidad
            document.querySelectorAll('.btn-disminuir').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.closest('.carrito-item').getAttribute('data-id'));
                    const item = carrito.find(item => item.id === id);
                    
                    if (item.cantidad > 1) {
                        item.cantidad--;
                    } else {
                        const index = carrito.findIndex(item => item.id === id);
                        carrito.splice(index, 1);
                    }
                    
                    actualizarCarrito();
                });
            });
            
            document.querySelectorAll('.btn-aumentar').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.closest('.carrito-item').getAttribute('data-id'));
                    const item = carrito.find(item => item.id === id);
                    item.cantidad++;
                    actualizarCarrito();
                });
            });
        }

        // Vaciar carrito
        vaciarCarritoBtn.addEventListener('click', () => {
            carrito.length = 0;
            actualizarCarrito();
        });

        // Finalizar compra
        comprarCarritoBtn.addEventListener('click', () => {
            if (carrito.length === 0) {
                alert('Tu carrito está vacío');
                return;
            }
            
            // Aquí normalmente se enviaría a una pasarela de pago
            alert(`Compra realizada por un total de $${carrito.reduce((total, item) => total + (item.precio * item.cantidad), 0).toLocaleString()}`);
            carrito.length = 0;
            actualizarCarrito();
            carritoModal.classList.remove('activo');
            overlay.classList.remove('activo');
            document.body.style.overflow = '';
        });

        // Función de búsqueda mejorada
        const realizarBusqueda = () => {
            const termino = document.querySelector('.busqueda-contenedor input').value.trim();
            if (termino) {
                const productosDOM = document.querySelectorAll('.producto');
                let encontrados = 0;
                
                productosDOM.forEach(producto => {
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

        // Lightbox para productos
        document.querySelectorAll('.btn-ver').forEach(btn => {
            btn.addEventListener('click', (e) => {
                const id = parseInt(e.target.getAttribute('data-id') || e.target.closest('.btn-ver').getAttribute('data-id'));
                const producto = productos.find(p => p.id === id);
                
                // Configurar lightbox
                const lightbox = document.getElementById('producto-lightbox');
                const imagen = document.getElementById('lightbox-imagen');
                const titulo = document.getElementById('lightbox-titulo');
                const descripcion = document.getElementById('lightbox-descripcion');
                const precio = document.getElementById('lightbox-precio');
                const btnComprar = document.getElementById('lightbox-comprar');
                
                imagen.src = producto.imagen;
                imagen.alt = producto.nombre;
                titulo.textContent = producto.nombre;
                descripcion.textContent = producto.descripcion;
                
                if (producto.precioOriginal) {
                    precio.innerHTML = `<span class="precio-oferta">$${producto.precioOriginal.toLocaleString()}</span> <span class="precio">$${producto.precio.toLocaleString()}</span>`;
                } else {
                    precio.innerHTML = `<span class="precio">$${producto.precio.toLocaleString()}</span>`;
                }
                
                btnComprar.setAttribute('data-id', producto.id);
                
                // Mostrar lightbox
                lightbox.style.display = 'block';
                
                // Cerrar lightbox
                document.querySelector('.lightbox-close').addEventListener('click', () => {
                    lightbox.style.display = 'none';
                });
                
                window.addEventListener('click', (e) => {
                    if (e.target === lightbox) {
                        lightbox.style.display = 'none';
                    }
                });
            });
        });

        // Añadir al carrito desde lightbox
        document.getElementById('lightbox-comprar').addEventListener('click', (e) => {
            const id = parseInt(e.target.getAttribute('data-id'));
            const producto = productos.find(p => p.id === id);
            
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
            document.getElementById('producto-lightbox').style.display = 'none';
            
            // Animación del icono del carrito
            const icono = carritoIcono.querySelector('i');
            icono.classList.remove('fa-shopping-cart');
            icono.classList.add('fa-check');
            
            setTimeout(() => {
                icono.classList.remove('fa-check');
                icono.classList.add('fa-shopping-cart');
            }, 1000);
        });

        // Formulario de contacto
        document.getElementById('contacto-form').addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Aquí normalmente se enviaría el formulario a un servidor
            alert('Gracias por tu mensaje. Nos pondremos en contacto contigo pronto.');
            e.target.reset();
        });

        // Scroll suave para enlaces
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
