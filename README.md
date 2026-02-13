<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Línea de Tiempo - Klisman Andrés Tejera Garrido</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 30px 0;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            color: white;
            margin-bottom: 100px;
        }

        .header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            margin-bottom: 15px;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.3);
        }

        .author {
            font-size: 1.2rem;
            font-weight: 300;
            letter-spacing: 1px;
        }

        .timeline-container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
        }

        /* LÍNEA CENTRAL SIMPLE */
        .timeline-line {
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(to bottom, #ff6b6b, #4ecdc4);
            margin-left: -2px;
            z-index: 1;
        }

        .timeline-item {
            display: flex;
            justify-content: space-between;
            margin: 60px 0;
            position: relative;
            opacity: 0;
            transform: translateY(50px);
            animation: slideInUp 0.8s ease forwards;
        }

        .timeline-item:nth-child(even) {
            flex-direction: row-reverse;
        }

        .timeline-content {
            width: 45%;
            background: rgba(255,255,255,0.95);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            position: relative;
            margin: 0 30px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .timeline-item:hover .timeline-content {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }

        .icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #ff6b6b, #4ecdc4);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: white;
            margin: 0 auto 20px;
            box-shadow: 0 8px 25px rgba(255,107,107,0.4);
        }

        .timeline-content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.7rem;
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .date {
            color: #667eea;
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .timeline-content p {
            color: #555;
            line-height: 1.7;
            font-size: 1rem;
        }

        /* CÍRCULOS EN LA LÍNEA */
        .timeline-dot {
            position: absolute;
            left: 50%;
            top: 25px;
            width: 20px;
            height: 20px;
            background: white;
            border: 5px solid #ff6b6b;
            border-radius: 50%;
            margin-left: -12px;
            z-index: 3;
            transition: transform 0.3s ease;
        }

        .timeline-item:hover .timeline-dot {
            transform: scale(1.3);
            border-color: #4ecdc4;
        }

        .footer {
            text-align: center;
            color: white;
            margin-top: 100px;
            font-size: 1rem;
            opacity: 0.9;
        }

        @keyframes slideInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ANIMACIÓN SECUENCIAL */
        .timeline-item:nth-child(1) { animation-delay: 0.1s; }
        .timeline-item:nth-child(2) { animation-delay: 0.3s; }
        .timeline-item:nth-child(3) { animation-delay: 0.5s; }
        .timeline-item:nth-child(4) { animation-delay: 0.7s; }
        .timeline-item:nth-child(5) { animation-delay: 0.9s; }
        .timeline-item:nth-child(6) { animation-delay: 1.1s; }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .timeline-line {
                left: 35px;
            }
            .timeline-item,
            .timeline-item:nth-child(even) {
                flex-direction: column;
                align-items: flex-start;
            }
            .timeline-content {
                width: 100%;
                margin: 20px 0 0 60px;
            }
            .timeline-dot {
                left: 35px;
                margin-left: 0;
            }
            .header h1 {
                font-size: 2rem;
            }
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

    <div class="timeline-container">
        <div class="timeline-line"></div>
        
        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-content">
                <div class="icon"><i class="fas fa-book-open"></i></div>
                <h2>Invención de la Imprenta</h2>
                <div class="date">1440 - Johannes Gutenberg</div>
                <p>Johannes Gutenberg crea la imprenta de tipos móviles, democratizando el acceso a libros y materiales educativos.</p>
            </div>
        </div>

        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-content">
                <div class="icon"><i class="fas fa-radio"></i></div>
                <h2>Radio Educativa</h2>
                <div class="date">1920</div>
                <p>Introducción de la radio en aulas para transmitir lecciones remotas y expandir la enseñanza audiovisual.</p>
            </div>
        </
