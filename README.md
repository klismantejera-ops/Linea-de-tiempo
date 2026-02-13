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
            overflow-x: hidden;
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
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background: linear-gradient(to bottom, #ff6b6b, #feca57, #48dbfb, #ff9ff3);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
            border-radius: 2px;
            box-shadow: 0 0 10px rgba(255,255,255,0.3);
        }

        /* ✅ CORREGIDO: Estados iniciales y animaciones */
        .container {
            padding: 20px 50px;
            position: relative;
            width: 50%;
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        .container.animate {
            opacity: 1 !important;
            transform: translateY(0) !important;
        }

        .container::after {
            content: '';
            position: absolute;
            width: 30px;
            height: 30px;
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            border: 5px solid white;
            top: 25px;
            border-radius: 50%;
            z-index: 2;
            box-shadow: 0 0 15px rgba(255,107,107,0.6);
            transition: all 0.3s ease;
        }

        .container:hover::after {
            transform: scale(1.2);
            box-shadow: 0 0 25px rgba(255,107,107,0.8);
        }

        .left { left: 0; }
        .right { left: 50%; }
        .left::after { right: -20px; }
        .right::after { left: -20px; }

        .content {
            position: relative;
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(20px);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.4s ease;
        }

        .content::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ff6b6b, #feca57, #48dbfb);
        }

        .content:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 30px 80px rgba(0,0,0,0.25);
        }

        .ic
