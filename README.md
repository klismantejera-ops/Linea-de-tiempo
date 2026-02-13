<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Línea de Tiempo: Evolución Tecnología Educativa</title>
    <style>
        body { font-family: Arial, sans-serif; background: linear-gradient(to right, #e3f2fd, #f5f5f5); padding: 20px; }
        .timeline { position: relative; max-width: 1200px; margin: 0 auto; }
        .timeline::after { content: ''; position: absolute; width: 6px; background: #2196F3; top: 0; bottom: 0; left: 50%; margin-left: -3px; }
        .container { padding: 10px 40px; position: relative; background-color: inherit; width: 50%; }
        .container::after { content: ''; position: absolute; width: 25px; height: 25px; right: -17px; background: #2196F3; border: 4px solid #fff; top: 15px; border-radius: 50%; z-index: 1; }
        .left { left: 0; }
        .right { left: 50%; }
        .right::after { left: -16px; }
        .content { padding: 20px 30px; background: white; position: relative; border-radius: 6px; box-shadow: 0 4px 8px rgba(0,0,0,0.1); transition: transform 0.3s; }
        .content:hover { transform: scale(1.05); }
        .content h2 { margin: 0 0 10px; color: #2196F3; }
        .content p { margin: 0 0 10px; }
        .icon { width: 60px; height: 60px; background: #2196F3; color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 24px; margin-bottom: 10px; }
        @media screen and (max-width: 600px) { .timeline::after { left: 31px; } .container { width: 100%; padding-left: 70px; padding-right: 25px; } .container::before { left: 60px; border: medium solid #2196F3; border-width: 10px 10px 0 0; border-color: #2196F3 transparent transparent transparent; } .right::after, .left::after { left: 15px; } .right { left: 0%; } }
    </style>
</head>
<body>
    <div class="timeline">
        <!-- Hito 1 -->
        <div class="container left">
            <div class="content">
                <div class="icon">📚</div>
                <h2>Invención de la Imprenta (1440)</h2>
                <p>Johannes Gutenberg crea la imprenta de tipos móviles, democratizando el acceso a libros y materiales educativos, revolucionando la difusión del conocimiento más allá de copias manuscritas.[web:1][web:4]</p>
            </div>
        </div>
        <!-- Hito 2 -->
        <div class="container right">
            <div class="content">
                <div class="icon">📻</div>
                <h2>Radio Educativa (1920)</h2>
                <p>Introducción de la radio en aulas para transmitir lecciones y programas educativos, permitiendo acceso remoto a información y ampliando el alcance de la enseñanza audiovisual.[web:6][web:4]</p>
            </div>
        </div>
        <!-- Hito 3 -->
        <div class="container left">
            <div class="content">
                <div class="icon">💻</div>
                <h2>Sistema PLATO (1960)</h2>
                <p>PLATO, uno de los primeros sistemas de aprendizaje asistido por computadora, ofrece tutoriales interactivos y comunicación entre estudiantes vía terminales, precursor de e-learning.[web:2][web:3]</p>
            </div>
        </div>
        <!-- Hito 4 -->
        <div class="container right">
            <div class="content">
                <div class="icon">🍎</div>
                <h2>Apple II en Escuelas (1977)</h2>
                <p>La computadora personal Apple II se integra masivamente en aulas estadounidenses, impulsando software educativo como LOGO y transformando el aprendizaje computacional.[web:2][web:14]</p>
            </div>
        </div>
        <!-- Hito 5 -->
        <div class="container left">
            <div class="content">
                <div class="icon">🖼️</div>
                <h2>Pizarras Digitales (1999)</h2>
                <p>Introducción de SMART Boards, pizarras interactivas que permiten anotaciones digitales, multimedia y colaboración en tiempo real en las aulas.[web:2][web:15]</p>
            </div>
        </div>
        <!-- Hito 6 -->
        <div class="container right">
            <div class="content">
                <div class="icon">📱</div>
                <h2>Plataformas MOOC (2011)</h2>
                <p>Lanzamiento de Khan Academy y Coursera, ofreciendo cursos masivos abiertos en línea gratuitos, accesibles globalmente vía internet y dispositivos móviles.[web:5][web:16]</p>
            </div>
        </div>
    </div>
    <script>
        // Efecto de scroll para activar animaciones
        window.addEventListener('scroll', () => {
            const contents = document.querySelectorAll('.content');
            contents.forEach(content => {
                const contentPos = content.getBoundingClientRect().top;
                if (contentPos < window.innerHeight - 100) {
                    content.style.opacity = '1';
                    content.style.transform = 'translateY(0)';
                }
            });
        });
    </script>
</body>
</html># Linea-de-tiempo
