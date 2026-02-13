<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Línea de Tiempo - Klisman Andrés Tejera Garrido</title>
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
            margin-bottom: 80px;
            padding: 20px;
        }

        .header h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 15px;
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
            width: 6px;
            background: linear-gradient(to bottom, #ff6b6b, #feca57, #48dbfb);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
            border-radius: 3px;
            box-shadow: 0 0 20px rgba(255,255,255,0.3);
        }

        /* ✅ ESTADOS INICIALES CLAROS */
        .container {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
            opacity: 0;
            transform: translateX(-100px);
        }

        /* ✅ ANIMACIÓN SIMPLIFICADA */
        .container.show {
            opacity: 1;
            transform: translateX(0);
            transition: all 0.8s ease;
        }

        .container.right {
            left: 50%;
            transform: translateX(100px);
        }

        .container.right.show {
            transform: translateX(0);
        }

        .container::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            right: -17px;
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            border: 4px solid white;
            top: 20px;
            border-radius: 50%;
            z-index: 1;
            box-shadow: 0 0 15px rgba(255,107,107,0.6);
        }

        .container.right::after {
            left: -16px;
        }

        .content {
            padding: 25px 30px;
            background: rgba(255,255,255,0.95);
            position: relative;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
            transition: all 0.4s ease;
        }

        .content:hover {
            transform: translateY(-8px);
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
            transition: all 0.3s ease;
        }

        .content:hover .icon {
            transform: scale(1.1);
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
        }

        .footer {
            text-align: center;
            margin-top: 100px;
            color: white;
            font-size: 0.9rem;
            opacity: 0.9;
            padding: 20px;
        }

        /* Responsive */
        @media screen and (max-width: 768px) {
            .timeline::after { left: 31px; }
            .container { 
                width: 100%; 
                padding-left: 70px; 
                padding-right: 25px; 
            }
            .container::before {
                left: 60px;
                border: medium solid white;
                border-width: 10px 10px 0 0;
                border-color: transparent transparent transparent white;
            }
            .right { left: 0%; }
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
        <div class="container left">
            <div class="content">
                <div class="icon"><i class="fas fa-book-open"></i></div>
                <h2>Invención de la Imprenta</h2>
                <div class="date">1440 - Johannes Gutenberg</div>
                <p>Johannes Gutenberg crea la imprenta de tipos móviles, democratizando el acceso a libros y materiales educativos.</p>
            </div>
        </div>

        <div class="container right">
            <div class="content">
                <div class="icon"><i class="fas fa-radio"></i></div>
                <h2>Radio Educativa</h2>
                <div class="date">1920</div>
                <p>Introducción de la radio en aulas para transmitir lecciones remotas y expandir la enseñanza audiovisual.</p>
            </div>
        </div>

        <div class="container left">
            <div class="content">
                <div class="icon"><i class="fas fa-laptop-code"></i></div>
                <h2>Sistema PLATO</h2>
                <div class="date">1960</div>
                <p>Primer sistema de aprendizaje asistido por computadora con tutoriales interactivos, precursor del e-learning.</p>
            </div>
        </div>

        <div class="container right">
            <div class="content">
                <div class="icon"><i class="fab fa-apple"></i></div>
                <h2>Apple II en Escuelas</h2>
                <div class="date">1977</div>
                <p>Computadora personal que impulsa software educativo en aulas, transformando el aprendizaje computacional.</p>
            </div>
        </div>

        <div class="container left">
            <div class="content">
                <div class="icon"><i class="fas fa-chalkboard"></i></div>
                <h2>Pizarras Digitales</h2>
                <div class="date">1999 - SMART Boards</div>
                <p>Pizarras interactivas con anotaciones digitales y multimedia colaborativa en tiempo real.</p>
            </div>
        </div>

        <div class="container right">
            <div class="content">
                <div class="icon"><i class="fas fa-globe"></i></div>
                <h2>Plataformas MOOC</h2>
                <div class="date">2011 - Khan Academy</div>
                <p>Cursos masivos abiertos en línea gratuitos, democratizando la educación superior globalmente.</p>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>Desarrollado por Klisman Andrés Tejera Garrido | Código 2025164031 | Tecnología Educativa 2026</p>
    </div>

    <script>
        // JavaScript ULTRA SIMPLE Y ESTABLE
        window.addEventListener('load', function() {
            const containers = document.querySelectorAll('.container');
            
            containers.forEach((container, index) => {
                setTimeout(() => {
                    container.classList.add('show');
                }, index * 300);
            });
        });
    </script>
</body>
</html>
