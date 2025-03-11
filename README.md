<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photography Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: #e0e0e0;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        header {
            background: #1f1f1f;
            color: #e0e0e0;
            padding: 1rem 0;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        header img {
            height: 50px;
            width: auto;
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
        }

        nav {
            background: #292929;
            padding: 0.5rem;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }

        nav ul li {
            margin: 0 1rem;
        }

        nav ul li a {
            color: #e0e0e0;
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #ff9800;
        }

        .hero {
            background: url('./theame.png') no-repeat center center/cover;
            height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
        }

        .hero h2 {
            font-size: 3rem;
            background: rgba(0, 0, 0, 0.5);
            padding: 1rem;
            animation: fadeIn 2s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .gallery {
            padding: 2rem;
            max-width: 1200px;
            margin: auto;
        }

        .gallery-section {
            margin-bottom: 2rem;
            transition: transform 0.3s;
        }

        .gallery-section:hover {
            transform: scale(1.02);
        }

        .gallery-section h3 {
            margin-bottom: 1rem;
            text-align: center;
            font-size: 1.8rem;
            color: #ff9800;
            cursor: pointer;
            transition: color 0.3s;
        }

        .gallery-section h3:hover {
            color: #e0e0e0;
        }

        .gallery-grid {
            display: none;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-grid img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            border: 2px solid #333;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .gallery-grid img:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        footer {
            background: #1f1f1f;
            color: #e0e0e0;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
        }

        footer p {
            margin: 0;
        }

        footer a {
            color: #ff9800;
            text-decoration: none;
            transition: color 0.3s;
        }

        footer a:hover {
            color: #e0e0e0;
        }

        .visible {
            display: grid;
        }

        @media (max-width: 768px) {
            .hero h2 {
                font-size: 2rem;
            }

            .gallery-section h3 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <img src="logo-removebg-preview.png" alt="Logo">
        <h1>Photography Portfolio</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    <section id="gallery" class="gallery">
        <!-- Wedding Gallery -->
        <div class="gallery-section" onclick="toggleGallery('wedding')">
            <h3>Wedding Photos</h3>
            <div class="gallery-grid" id="wedding">
                <img src="./theame.png" alt="Wedding Photo 1">
                <img src="./theame.png" alt="Wedding Photo 2">
                <img src="./images/wedding3.jpg" alt="Wedding Photo 3">
                <img src="./images/wedding4.jpg" alt="Wedding Photo 4">
            </div>
        </div>
    
        <!-- Candid Gallery -->
        <div class="gallery-section" onclick="toggleGallery('candid')">
            <h3>Candid Photos</h3>
            <div class="gallery-grid" id="candid">
                <img src="./images/candid1.jpg" alt="Candid Photo 1">
                <img src="./images/candid2.jpg" alt="Candid Photo 2">
                <img src="./images/candid3.jpg" alt="Candid Photo 3">
                <img src="./images/candid4.jpg" alt="Candid Photo 4">
            </div>
        </div>
    
        <!-- Birthday Gallery -->
        <div class="gallery-section" onclick="toggleGallery('birthday')">
            <h3>Birthday Photos</h3>
            <div class="gallery-grid" id="birthday">
                <img src="./images/birthday1.jpg" alt="Birthday Photo 1">
                <img src="./images/birthday2.jpg" alt="Birthday Photo 2">
                <img src="./images/birthday3.jpg" alt="Birthday Photo 3">
                <img src="./images/birthday4.jpg" alt="Birthday Photo 4">
            </div>
        </div>
    </section>
    
    <footer>
        <p>&copy; 2025 Photography Portfolio. All Rights Reserved.</p>
        <p>Designed by <a href="#">Your Name</a></p>
    </footer>
    <script>
        function toggleGallery(sectionId) {
            const section = document.getElementById(sectionId);
            section.classList.toggle('visible');
        }
    </script>
</body>
</html>
