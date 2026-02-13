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

        /* ✅ LÍNEA CENTRAL NUNCA INTERFIERE */
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
            z-index: 1; /* Debajo de todo */
        }

        .container {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
            opacity: 0;
            transform: translateX(-100px);
            z-index: 2; /* ✅ SIEMPRE ENCIMA DE LA LÍNEA */
        }

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

        /* ✅ CÍRCULOS TAMBIÉN ENCIMA */
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
            z-index: 3; /* ✅ MÁS ALTO QUE TODO */
            box-shadow: 0 0 15px rgba(255,107,107,0.6);
            transition: all 0.3s ease;
        }

        .container.right::after {
            left: -16px;
        }

        .container:hover::after {
            transform: scale(1.3);
            box-shadow: 0 0 25px rgba(255,107,107,0.8);
        }

        .content {
            padding: 25px 30px;
            background: rgba(255,255,255,0.
