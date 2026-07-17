# MISHEL-
Para que Mishel sepa que vale mucho 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para mi bonita Mishel ❤️</title>
    <!-- Fuentes Premium -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* ==========================================
           VARIABLES Y CONFIGURACIÓN GLOBAL
           ========================================== */
        :root {
            --bg-color: #fff7f8;
            --primary: #ff4d6d;
            --secondary: #ff85a1;
            --detail: #ffc2d1;
            --text: #4a2c2a;
            --white-glass: rgba(255, 255, 255, 0.75);
            --shadow-sm: 0 4px 12px rgba(255, 77, 109, 0.1);
            --shadow-md: 0 8px 30px rgba(255, 77, 109, 0.15);
            --shadow-lg: 0 16px 40px rgba(74, 44, 42, 0.12);
            --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-color);
            color: var(--text);
            overflow-x: hidden;
            line-height: 1.6;
        }

        h1, h2, h3, .font-serif {
            font-family: 'Playfair Display', serif;
        }

        /* Gradiente animado de fondo suave */
        .bg-animated {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -10;
            background: linear-gradient(135deg, #fff7f8 0%, #fff0f2 50%, #ffe5eb 100%);
            background-size: 400% 400%;
            animation: gradientMove 20s ease infinite;
        }

        @keyframes gradientMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Contenedores y Estilos de Grid */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
            position: relative;
        }

        /* Botones Premium */
        .btn-premium {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            padding: 0.9rem 2.2rem;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            text-decoration: none;
            outline: none;
        }

        .btn-premium:hover {
            transform: translateY(-4px) scale(1.02);
            box-shadow: 0 12px 24px rgba(255, 77, 109, 0.35);
        }

        .btn-premium:active {
            transform: translateY(-1px);
        }

        /* Estilo Glassmorphism General */
        .glass-panel {
            background: var(--white-glass);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            box-shadow: var(--shadow-md);
            border-radius: 24px;
        }

        /* ==========================================
           PANTALLA DE BIENVENIDA (SOBRE)
           ========================================== */
        #welcome-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: var(--bg-color);
            z-index: 10000;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: opacity 1s ease, visibility 1s;
        }

        .envelope-wrapper {
            position: relative;
            cursor: pointer;
            perspective: 1000px;
            width: 320px;
            height: 220px;
            margin-bottom: 30px;
        }

        .envelope {
            position: relative;
            width: 100%;
            height: 100%;
            background-color: var(--secondary);
            border-radius: 0 0 10px 10px;
            box-shadow: var(--shadow-lg);
            transition: var(--transition);
        }

        .envelope::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            border-left: 160px solid transparent;
            border-right: 160px solid transparent;
            border-top: 110px solid var(--detail);
            transform-origin: top;
            transition: transform 0.6s ease 0.2s, z-index 0.2s ease 0.4s;
            z-index: 4;
        }

        /* Cuerpo del sobre */
        .envelope-body {
            position: absolute;
            bottom: 0;
            width: 0;
            height: 0;
            border-left: 160px solid var(--secondary);
            border-right: 160px solid var(--secondary);
            border-bottom: 110px solid #ff5d8f;
            border-radius: 0 0 10px 10px;
            z-index: 3;
        }

        .letter {
            position: absolute;
            top: 15px;
            left: 15px;
            right: 15px;
            bottom: 15px;
            background: white;
            border-radius: 8px;
            z-index: 2;
            transition: transform 0.6s ease;
            padding: 20px;
            text-align: center;
            box-shadow: 0 -5px 15px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .letter p {
            font-family: 'Playfair Display', serif;
            font-size: 1.1rem;
            color: var(--text);
            margin-bottom: 8px;
        }

        /* Apertura del sobre */
        .envelope-wrapper.open .envelope::before {
            transform: rotateX(180deg);
            z-index: 1;
        }

        .envelope-wrapper.open .letter {
            transform: translateY(-110px);
            z-index: 5;
        }

        .welcome-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        /* ==========================================
           SISTEMA DE ANIMACIÓN AL SCROLL (FADE IN/ZOOM)
           ========================================== */
        .reveal {
            opacity: 0;
            transform: translateY(40px) scale(0.97);
            transition: opacity 1.2s cubic-bezier(0.16, 1, 0.3, 1), transform 1.2s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0) scale(1);
        }

        /* ==========================================
           HERO SECTION
           ========================================== */
        header {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            position: relative;
        }

        .hero-card {
            padding: 4rem 3rem;
            max-width: 750px;
            width: 100%;
        }

        .hero-card h1 {
            font-size: 4.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            line-height: 1.2;
            animation: bounceSoft 4s ease-in-out infinite;
        }

        .hero-card p {
            font-size: 1.35rem;
            margin-bottom: 2.5rem;
            font-weight: 300;
        }

        @keyframes bounceSoft {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-12px); }
        }

        /* ==========================================
           MENSAJE PRINCIPAL
           ========================================== */
        .main-message {
            background: linear-gradient(135deg, rgba(255, 77, 109, 0.08) 0%, rgba(255, 133, 161, 0.05) 100%);
            border: 1px solid rgba(255, 77, 109, 0.15);
            padding: 5rem 3rem;
            text-align: center;
            border-radius: 35px;
            margin: 2rem 0;
        }

        .main-message p {
            font-family: 'Playfair Display', serif;
            font-size: 2.1rem;
            line-height: 1.7;
            font-style: italic;
            color: var(--text);
            max-width: 900px;
            margin: 0 auto;
        }

        /* ==========================================
           CONTADOR
           ========================================== */
        .counter-section {
            text-align: center;
        }

        .counter-section h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 3rem;
        }

        .counter-container {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .counter-box {
            min-width: 120px;
            padding: 2rem 1rem;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .counter-number {
            font-family: 'Playfair Display', serif;
            font-size: 3.2rem;
            font-weight: 700;
            color: var(--primary);
            line-height: 1;
        }

        .counter-label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
            opacity: 0.8;
        }

        /* ==========================================
           GALERÍA POLAROID
           ========================================== */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .polaroid {
            background-color: white;
            padding: 1.2rem;
            padding-bottom: 2.5rem;
            box-shadow: var(--shadow-md);
            border-radius: 4px;
            transition: var(--transition);
            cursor: pointer;
            position: relative;
        }

        /* Distribución ligeramente desalineada para efecto realista */
        .polaroid:nth-child(1) { transform: rotate(-2deg); }
        .polaroid:nth-child(2) { transform: rotate(1.5deg); }
        .polaroid:nth-child(3) { transform: rotate(-1deg); }

        .polaroid:hover {
            transform: scale(1.05) rotate(0deg) translateY(-10px);
            box-shadow: var(--shadow-lg);
            z-index: 10;
        }

        .polaroid-img-wrapper {
            width: 100%;
            aspect-ratio: 1;
            overflow: hidden;
            background-color: #eee;
            margin-bottom: 1.5rem;
            border: 1px solid rgba(0,0,0,0.05);
        }

        .polaroid-img-wrapper img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s ease;
        }

        .polaroid:hover .polaroid-img-wrapper img {
            transform: scale(1.1);
        }

        .polaroid-caption {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            text-align: center;
            font-size: 1.15rem;
            color: var(--text);
        }

        /* Lightbox */
        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(74, 44, 42, 0.95);
            backdrop-filter: blur(8px);
            z-index: 20000;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.4s ease;
        }

        .lightbox.active {
            opacity: 1;
            pointer-events: auto;
        }

        .lightbox-content {
            max-width: 90%;
            max-height: 80%;
            border-radius: 12px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
            transform: scale(0.9);
            transition: transform 0.4s ease;
        }

        .lightbox.active .lightbox-content {
            transform: scale(1);
        }

        .lightbox-close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: white;
            font-size: 3rem;
            cursor: pointer;
            user-select: none;
        }

        /* ==========================================
           TARJETAS FLIP (RAZONES POR LAS QUE TE AMO)
           ========================================== */
        .reasons-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 3rem;
        }

        .reasons-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 2rem;
        }

        .card-container {
            perspective: 1000px;
            height: 250px;
        }

        .card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            transform-style: preserve-3d;
            cursor: pointer;
        }

        .card-container:hover .card-inner {
            transform: rotateY(180deg);
        }

        .card-front, .card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            border-radius: 20px;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .card-front {
            background: var(--white-glass);
            border: 1px solid rgba(255, 77, 109, 0.2);
            color: var(--primary);
        }

        .card-front span {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
        }

        .card-front h3 {
            font-size: 1.3rem;
            font-weight: 600;
        }

        .card-back {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            transform: rotateY(180deg);
        }

        .card-back p {
            font-size: 1.05rem;
            font-weight: 500;
            line-height: 1.5;
        }

        /* ==========================================
           SECCIÓN DE NOTAS INTERACTIVAS
           ========================================== */
        .notes-section {
            max-width: 800px;
            margin: 0 auto;
        }

        .notes-section h2 {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 2rem;
        }

        .note-creator {
            padding: 2rem;
            margin-bottom: 3rem;
        }

        .note-creator textarea {
            width: 100%;
            height: 120px;
            background: rgba(255, 255, 255, 0.8);
            border: 1px solid var(--detail);
            border-radius: 12px;
            padding: 1rem;
            font-family: inherit;
            font-size: 1rem;
            color: var(--text);
            resize: none;
            outline: none;
            margin-bottom: 1rem;
            transition: var(--transition);
        }

        .note-creator textarea:focus {
            border-color: var(--primary);
            box-shadow: 0 0 10px rgba(255, 77, 109, 0.15);
        }

        .notes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 1.5rem;
        }

        .note-card {
            background: #fff;
            border-left: 5px solid var(--primary);
            padding: 1.5rem;
            border-radius: 8px 16px 16px 8px;
            box-shadow: var(--shadow-sm);
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-height: 180px;
            transition: var(--transition);
        }

        .note-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .note-content {
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
            word-wrap: break-word;
            white-space: pre-wrap;
        }

        .note-actions {
            display: flex;
            justify-content: flex-end;
            gap: 0.5rem;
        }

        .btn-note-action {
            background: none;
            border: none;
            cursor: pointer;
            font-size: 0.9rem;
            padding: 4px 8px;
            border-radius: 4px;
            transition: var(--transition);
        }

        .btn-edit {
            color: var(--text);
            background-color: rgba(0,0,0,0.05);
        }

        .btn-edit:hover { background-color: rgba(0,0,0,0.1); }

        .btn-delete {
            color: white;
            background-color: var(--primary);
        }

        .btn-delete:hover { filter: brightness(0.9); }

        /* ==========================================
           LÍNEA DEL TIEMPO
           ========================================== */
        .timeline-container {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem 0;
        }

        .timeline-container::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 50%;
            width: 4px;
            background: var(--detail);
            transform: translateX(-50%);
        }

        .timeline-event {
            position: relative;
            margin-bottom: 4rem;
            width: 50%;
            padding-right: 3rem;
            text-align: right;
        }

        .timeline-event:nth-child(even) {
            left: 50%;
            padding-right: 0;
            padding-left: 3rem;
            text-align: left;
        }

        .timeline-event::after {
            content: '';
            position: absolute;
            top: 20px;
            right: -10px;
            width: 20px;
            height: 20px;
            background-color: var(--primary);
            border: 4px solid var(--bg-color);
            border-radius: 50%;
            z-index: 1;
            box-shadow: var(--shadow-sm);
        }

        .timeline-event:nth-child(even)::after {
            left: -10px;
            right: auto;
        }

        .timeline-card {
            padding: 2rem;
        }

        .timeline-date {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 1.1rem;
            color: var(--primary);
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .timeline-card h3 {
            margin-bottom: 0.5rem;
            font-size: 1.4rem;
        }

        /* ==========================================
           REPRODUCTOR DE MÚSICA FLOTANTE
           ========================================== */
        .music-player {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 9999
