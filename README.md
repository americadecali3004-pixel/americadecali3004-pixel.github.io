<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>América de Cali - El equipo de mis amores</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        /* Variables de color */
        :root {
            --rojo-america: #B30838;
            --blanco: #FFFFFF;
            --negro: #000000;
            --gris: #333333;
            --gris-claro: #F5F5F5;
        }

        body {
            background-color: var(--gris-claro);
            color: var(--gris);
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1574629810360-7efbbe195018?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            color: var(--blanco);
        }

        .logo {
            width: 200px;
            margin-bottom: 20px;
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        header p {
            font-size: 1.5rem;
            max-width: 800px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background: var(--rojo-america);
            color: var(--blanco);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background: var(--blanco);
            color: var(--rojo-america);
        }

        /* Navbar */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: var(--rojo-america);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 50px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        nav .logo-nav {
            height: 50px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            color: var(--blanco);
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        nav ul li a:hover {
            opacity: 0.8;
        }

        /* Secciones */
        section {
            padding: 80px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: var(--rojo-america);
            position: relative;
        }

        section h2::after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: var(--rojo-america);
            margin: 15px auto;
        }

        /* Historia */
        #historia {
            background-color: var(--blanco);
        }

        .historia-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }

        .historia-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }

        .historia-img {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }

        .historia-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        /* Plantilla */
        #plantilla {
            background-color: var(--gris-claro);
        }

        .jugadores {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }

        .jugador {
            background: var(--blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .jugador:hover {
            transform: translateY(-10px);
        }

        .jugador-img {
            height: 250px;
            overflow: hidden;
        }

        .jugador-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .jugador:hover .jugador-img img {
            transform: scale(1.1);
        }

        .jugador-info {
            padding: 20px;
            text-align: center;
        }

        .jugador-info h3 {
            color: var(--rojo-america);
            margin-bottom: 10px;
        }

        /* Palmarés */
        #palmares {
            background-color: var(--blanco);
        }

        .trofeos {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .trofeo {
            text-align: center;
            flex: 1;
            min-width: 200px;
        }

        .trofeo i {
            font-size: 3rem;
            color: var(--rojo-america);
            margin-bottom: 20px;
        }

        .trofeo h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        /* Estadio */
        #estadio {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1540747913346-19e32dc3e97e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: var(--blanco);
            text-align: center;
        }

        #estadio h2 {
            color: var(--blanco);
        }

        #estadio h2::after {
            background: var(--blanco);
        }

        /* Contacto */
        #contacto {
            background-color: var(--gris-claro);
        }

        .contacto-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .contacto-info, .contacto-form {
            flex: 1;
            min-width: 300px;
        }

        .contacto-info h3 {
            color: var(--rojo-america);
            margin-bottom: 20px;
        }

        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .info-item i {
            margin-right: 15px;
            color: var(--rojo-america);
            font-size: 1.2rem;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input, 
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .form-group textarea {
            height: 150px;
        }

        /* Footer */
        footer {
            background-color: var(--rojo-america);
            color: var(--blanco);
            text-align: center;
            padding: 30px 20px;
        }

        .social-links {
            margin-bottom: 20px;
        }

        .social-links a {
            color: var(--blanco);
            margin: 0 10px;
            font-size: 1.5rem;
            transition: opacity 0.3s ease;
        }

        .social-links a:hover {
            opacity: 0.8;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }

            header p {
                font-size: 1.2rem;
            }

            nav {
                padding: 15px 20px;
            }

            nav ul li {
                margin-left: 15px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>
<body>
    <!-- Navbar -->
    <nav>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/Escudo_del_Am%C3%A9rica_de_Cali.svg/1200px-Escudo_del_Am%C3%A9rica_de_Cali.svg.png" alt="Escudo América de Cali" class="logo-nav" height="50">
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#historia">Historia</a></li>
            <li><a href="#plantilla">Plantilla</a></li>
            <li><a href="#palmares">Palmarés</a></li>
            <li><a href="#estadio">Estadio</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>

    <!-- Header -->
    <header id="inicio">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/Escudo_del_Am%C3%A9rica_de_Cali.svg/1200px-Escudo_del_Am%C3%A9rica_de_Cali.svg.png" alt="Escudo América de Cali" class="logo">
        <h1>América de Cali</h1>
        <p>El equipo de mis amores, pasión de un pueblo que late al ritmo del rojo</p>
        <a href="#historia" class="btn">Conoce nuestra historia</a>
    </header>

    <!-- Sección Historia -->
    <section id="historia">
        <div class="container">
            <h2>Nuestra Historia</h2>
            <div class="historia-content">
                <div class="historia-text">
                    <p>El América de Cali es un club de fútbol profesional colombiano fundado el 13 de febrero de 1927 en la ciudad de Cali. Conocido como "Los Diablos Rojos", es uno de los equipos más populares y exitosos del fútbol colombiano.</p>
                    <p>El club ha sido campeón de la Categoría Primera A en 15 ocasiones, siendo el segundo equipo con más títulos en el país. Además, ha sido subcampeón de la Copa Libertadores en cuatro oportunidades (1985, 1986, 1987 y 1996).</p>
                    <p>El América representa la pasión, garra y corazón del Valle del Cauca y de toda Colombia, con una hinchada fiel que lo sigue en todas partes.</p>
                </div>
                <div class="historia-img">
                    <img src="https://images.unsplash.com/photo-1540747913346-19e32dc3e97e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Estadio América de Cali">
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Plantilla -->
    <section id="plantilla">
        <div class="container">
            <h2>Nuestra Plantilla</h2>
            <div class="jugadores">
                <div class="jugador">
                    <div class="jugador-img">
                        <img src="https://as01.epimg.net/colombia/imagenes/2021/07/08/futbol/1625757926_417106_1625758049_noticia_normal.jpg" alt="Jugador 1">
                    </div>
                    <div class="jugador-info">
                        <h3>Adrián Ramos</h3>
                        <p>Delantero</p>
                        <p>Número: 9</p>
                    </div>
                </div>
                <div class="jugador">
                    <div class="jugador-img">
                        <img src="https://caracoltv.brightspotcdn.com/dims4/default/3a2c0b1/2147483647/strip/true/crop/1000x562+0+0/resize/1000x563!/quality/90/?url=http%3A%2F%2Fcaracol-brightspot.s3.amazonaws.com%2F1c%2F0a%2F6e5a4e5c4d9c8c4c0c0c0c0c0c0c0c0%2Fdarlin.jpg" alt="Jugador 2">
                    </div>
                    <div class="jugador-info">
                        <h3>Darlin Leudo</h3>
                        <p>Volante</p>
                        <p>Número: 5</p>
                    </div>
                </div>
                <div class="jugador">
                    <div class="jugador-img">
                        <img src="https://www.futbolred.com/files/article_main/files/crop/uploads/2021/01/14/6000a0e6e0f3e.r_1610658145618.0-0-1200-598.jpeg" alt="Jugador 3">
                    </div>
                    <div class="jugador-info">
                        <h3>Joel Graterol</h3>
                        <p>Portero</p>
                        <p>Número: 1</p>
                    </div>
                </div>
                <div class="jugador">
                    <div class="jugador-img">
                        <img src="https://www.elpais.com.co/files/article_main/files/crop/uploads/2021/07/08/60e72c2b9a6b4.r_1625760164141.0-0-1200-600.jpeg" alt="Jugador 4">
                    </div>
                    <div class="jugador-info">
                        <h3>Luis Sánchez</h3>
                        <p>Defensa</p>
                        <p>Número: 3</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Palmarés -->
    <section id="palmares">
        <div class="container">
            <h2>Nuestro Palmarés</h2>
            <div class="trofeos">
                <div class="trofeo">
                    <i class="fas fa-trophy"></i>
                    <h3>15 Títulos</h3>
                    <p>Liga Colombiana</p>
                </div>
                <div class="trofeo">
                    <i class="fas fa-medal"></i>
                    <h3>4 Subcampeonatos</h3>
                    <p>Copa Libertadores</p>
                </div>
                <div class="trofeo">
                    <i class="fas fa-star"></i>
                    <h3>5 Títulos</h3>
                    <p>Copa Colombia</p>
                </div>
                <div class="trofeo">
                    <i class="fas fa-shield-alt"></i>
                    <h3>2 Títulos</h3>
                    <p>Superliga Colombiana</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Estadio -->
    <section id="estadio">
        <div class="container">
            <h2>Nuestro Estadio</h2>
            <p>El Estadio Pascual Guerrero, conocido como "El Monumental de Palmaseca", es nuestra fortaleza. Con capacidad para más de 33,000 espectadores, es uno de los estadios más emblemáticos de Colombia.</p>
            <p>Ubicado en la ciudad de Cali, ha sido testigo de grandes hazañas del equipo y de la selección colombiana.</p>
            <a href="#" class="btn">Visita Virtual</a>
        </div>
    </section>

    <!-- Sección Contacto -->
    <section id="contacto">
        <div class="container">
            <h2>Contacto</h2>
            <div class="contacto-container">
                <div class="contacto-info">
                    <h3>Información de Contacto</h3>
                    <div class="info-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <p>Estadio Pascual Guerrero, Cali, Colombia</p>
                    </div>
                    <div class="info-item">
                        <i class="fas fa-phone"></i>
                        <p>+57 2 555 1234</p>
                    </div>
                    <div class="info-item">
                        <i class="fas fa-envelope"></i>
                        <p>contacto@americadecali.co</p>
                    </div>
                    <div class="info-item">
                        <i class="fas fa-clock"></i>
                        <p>Lunes a Viernes: 9:00 AM - 6:00 PM</p>
                    </div>
                </div>
                <div class="contacto-form">
                    <form>
                        <div class="form-group">
                            <label for="nombre">Nombre</label>
                            <input type="text" id="nombre" name="nombre" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="asunto">Asunto</label>
                            <input type="text" id="asunto" name="asunto" required>
                        </div>
                        <div class="form-group">
                            <label for="mensaje">Mensaje</label>
                            <textarea id="mensaje" name="mensaje" required></textarea>
                        </div>
                        <button type="submit" class="btn">Enviar Mensaje</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
        <p>&copy; 2023 América de Cali. Todos los derechos reservados.</p>
        <p>El equipo de mis amores</p>
    </footer>
</body>
</html>
