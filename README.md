<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Línea de Tiempo Evolución Tecnología Educativa - Klisman Andrés Tejera Garrido</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px 0;
        }

        .header {
            text-align: center;
            color: white;
            margin-bottom: 60px;
            animation: fadeInDown 1s ease;
        }

        .header h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 10px;
            text-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }

        .author {
            font-size: clamp(1rem, 2.5vw, 1.3rem);
            font-weight: 300;
            opacity: 0.95;
            letter-spacing: 2px;
        }

        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background: linear-gradient(to bottom, #ff6b6b, #feca57, #48dbfb);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
            z-index: 1;
        }

        .container {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            margin-bottom: 40px;
            opacity: 0;
            animation: slideIn 0.8s ease forwards;
        }

        .container:nth-child(odd) { 
            left: 0;
            animation-delay: 0.2s;
        }

        .container:nth-child(even) { 
            left: 50%; 
            animation-delay: 0.4s;
        }

        .container::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -13px;
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            border: 4px solid white;
            top: 25px;
            border-radius: 50%;
            z-index: 3;
            box-shadow: 0 0 15px rgba(255,107,107,0.6);
        }

        .container:nth-child(even)::after {
            left: -13px;
        }

        .content {
            background: rgba(255,255,255,0.95);
            padding: 25px 30px;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
            margin: 0 20px;
            transition: all 0.4s ease;
            position: relative;
            z-index: 2;
        }

        .content:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.3);
        }

        .content::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #feca57, #48dbfb);
            border-radius: 15px 15px 0 0;
        }

        .icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin: 0 auto 20px;
            box-shadow: 0 8px 25px rgba(102,126,234,0.4);
        }

        .content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            color: #2c3e50;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .content .date {
            color: #667eea;
            font-weight: 600;
            font-size: 1rem;
            margin-bottom: 12px;
        }

        .content p {
            color: #555;
            line-height: 1.6;
            font-size: 0.95rem;
            margin-bottom: 10px;
        }

        .sources {
            font-size: 0.8rem;
            color: #888;
            font-style: italic;
        }

        .footer {
            text-align: center;
            margin-top: 80px;
            color: white;
            font-size: 0.9rem;
            opacity: 0.8;
            padding: 20px;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media screen and (max-width: 768px) {
            .timeline::after { left: 30px; }
            .container { 
                width: 100%; 
                left: 0 !important;
                padding-left: 70px;
                padding-right: 25px;
            }
            .container::after { left: 20px; right: auto; }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-graduation-cap"></i> Evolución Tecnológica Educativa</h1>
        <div class="author">
            Creado por Klisman Andrés Tejera Garrido <br>
            <strong>Código: 2025164031</strong>
        </div>
    </div>

    <div class="timeline">
        <!-- Hito 1 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fas fa-book-open"></i></div>
                <h2>Invención de la Imprenta</h2>
                <div class="date">1440 - Johannes Gutenberg</div>
                <p>Johannes Gutenberg crea la imprenta de tipos móviles, democratizando el acceso a libros y materiales educativos, revolucionando la difusión del conocimiento más allá de copias manuscritas.</p>
                <div class="sources">[web:1][web:4]</div>
            </div>
        </div>

        <!-- Hito 2 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fas fa-radio"></i></div>
                <h2>Radio Educativa</h2>
                <div class="date">1920</div>
                <p>Introducción de la radio en aulas para transmitir lecciones y programas educativos, permitiendo acceso remoto a información y ampliando el alcance de la enseñanza audiovisual.</p>
                <div class="sources">[web:6][web:4]</div>
            </div>
        </div>

        <!-- Hito 3 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fas fa-laptop-code"></i></div>
                <h2>Sistema PLATO</h2>
                <div class="date">1960</div>
                <p>PLATO, uno de los primeros sistemas de aprendizaje asistido por computadora, ofrece tutoriales interactivos y comunicación entre estudiantes vía terminales, precursor de e-learning.</p>
                <div class="sources">[web:2][web:3]</div>
            </div>
        </div>

        <!-- Hito 4 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fab fa-apple"></i></div>
                <h2>Apple II en Escuelas</h2>
                <div class="date">1977</div>
                <p>La computadora personal Apple II se integra masivamente en aulas estadounidenses, impulsando software educativo como LOGO y transformando el aprendizaje computacional.</p>
                <div class="sources">[web:2][web:14]</div>
            </div>
        </div>

        <!-- Hito 5 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fas fa-chalkboard"></i></div>
                <h2>Pizarras Digitales</h2>
                <div class="date">1999 - SMART Boards</div>
                <p>Introducción de SMART Boards, pizarras interactivas que permiten anotaciones digitales, multimedia y colaboración en tiempo real en las aulas.</p>
                <div class="sources">[web:2][web:15]</div>
            </div>
        </div>

        <!-- Hito 6 -->
        <div class="container">
            <div class="content">
                <div class="icon"><i class="fas fa-globe"></i></div>
                <h2>Plataformas MOOC</h2>
                <div class="date">2011 - Khan Academy</div>
                <p>Lanzamiento de Khan Academy y Coursera, ofreciendo cursos masivos abiertos en línea gratuitos, accesibles globalmente vía internet y dispositivos móviles.</p>
                <div class="sources">[web:5][web:16]</div>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>Desarrollado por Klisman Andrés Tejera Garrido | Código 2025164031 | Tecnología Educativa
