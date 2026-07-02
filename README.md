<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Fundația Umanitară Meridian S</title>
    <style>
        :root {
            --green: #27ae60;
            --dark-green: #219653;
            --light-green-shadow: rgba(46, 204, 113, 0.1);
            --lighter-green-shadow: rgba(46, 204, 113, 0.2);
            --text-dark: #2c3e50;
            --text-light: #5d6d7e;
            --background-light: #eafaf1;
            --background-offwhite: #f4fbf7;
            --button-shadow: rgba(39, 174, 96, 0.2);
            --accent-yellow: #f1c40f;
            --accent-orange: #d35400;
            --footer-color: #7f8c8d;
        }
        /* Reset bază */
        *, *::before, *::after {
            box-sizing: border-box;
        }
        body, h1, h3, p, ul {
            margin: 0;
            padding: 0;
        }
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background-color: var(--background-light);
            color: var(--text-dark);
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        header {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }
        .logo {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--green);
            text-decoration: none;
        }
        nav a {
            color: var(--text-light);
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            transition: color 0.3s ease;
        }
        nav a:hover,
        nav a:focus {
            color: var(--green);
            outline: none;
        }
        main {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            gap: 25px;
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }
        .photo-column {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 220px;
            flex-shrink: 0;
        }
        .gallery-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 12px;
            box-shadow: 0 5px 15px var(--light-green-shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .gallery-img:hover,
        .gallery-img:focus {
            transform: scale(1.03);
            box-shadow: 0 8px 20px var(--lighter-green-shadow);
            outline: none;
        }
        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(46, 204, 113, 0.08);
            text-align: center;
            max-width: 600px;
            width: 100%;
        }
        h1 {
            color: var(--green);
            font-size: 28px;
            margin-bottom: 15px;
        }
        .mission-text {
            color: var(--text-light);
            font-size: 16px;
            margin-bottom: 25px;
        }
        .goals-box {
            text-align: left;
            background-color: var(--background-offwhite);
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid var(--green);
            margin-bottom: 25px;
        }
        .goals-box h3 {
            color: var(--text-dark);
            font-size: 18px;
            margin-bottom: 10px;
        }
        .goals-box ul {
            list-style-position: inside;
            color: var(--text-light);
        }
        .goals-box li {
            margin-bottom: 8px;
            font-size: 15px;
        }
        .donation-box {
            background-color: #fffdf3;
            border: 2px dashed var(--accent-yellow);
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 25px;
            text-align: left;
        }
        .donation-box h3 {
            color: var(--accent-orange);
            font-size: 18px;
            margin-bottom: 12px;
            text-align: center;
        }
        .bank-details {
            font-size: 15px;
            color: #34495e;
        }
        .bank-details p {
            margin-bottom: 6px;
            display: flex;
            justify-content: space-between;
            border-bottom: 1px dashed #f9e79f;
            padding-bottom: 4px;
        }
        .bank-details p:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }
        .bank-details strong {
            color: var(--text-dark);
            font-family: 'Courier New', Courier, monospace;
            font-size: 16px;
        }
        .btn {
            display: inline-block;
            background-color: var(--green);
            color: #fff;
            text-decoration: none;
            padding: 14px 30px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 16px;
            transition: background 0.3s, transform 0.2s;
            box-shadow: 0 4px 10px var(--button-shadow);
            width: 100%;
            text-align: center;
            cursor: pointer;
            user-select: none;
        }
        .btn:hover,
        .btn:focus {
            background-color: var(--dark-green);
            transform: translateY(-1px);
            outline: none;
        }
        footer {
            background-color: #fff;
            text-align: center;
            padding: 20px;
            margin-top: auto;
            border-top: 1px solid var(--background-light);
            font-size: 14px;
            color: var(--footer-color);
        }
        .email-link {
            color: var(--green);
            text-decoration: none;
            font-weight: 700;
        }
        .email-link:hover,
        .email-link:focus {
            text-decoration: underline;
            outline: none;
        }
        @media (max-width: 1100px) {
            main {
                flex-direction: column;
                align-items: center;
                padding: 20px;
            }
            .photo-column {
                flex-direction: row;
                width: 100%;
                justify-content: center;
                flex-wrap: wrap;
            }
            .gallery-img {
                width: calc(50% - 10px);
                max-width: 250px;
                height: 180px;
            }
            .container {
                max-width: 100%;
                order: -1; /* Textul rămâne sus pe mobil */
            }
        }
    </style>
</head>
<body>
<header id="top">
    <div class="nav-container">
        <a href="#top" class="logo">Fundația Umanitară Meridian S</a>
        <nav class="nav-links">
            <a href="#donatie-sectiune">Acasă</a>
            <a href="mailto:fundatiameridians@gmail.com" rel="noopener noreferrer">Contact</a>
        </nav>
    </div>
</header>
<main>
    <div class="photo-column" aria-label="Galerie foto stânga">
        <img class="gallery-img" src="https://www.osservatoreromano.va/content/dam/or/images/it/2020/07/170/Cetera_27_x.jpg/_jcr_content/renditions/cq5dam.thumbnail.cropped.500.281.jpeg" alt="Persoane în vârstă" />
        <img class="gallery-img" src="https://portal.revistatimpul.ro/timpul-belgia/wp-content/uploads/sites/8/2023/04/doi-batrani.jpg" alt="Ajutor umanitar" />
    </div>
    <section class="container" aria-labelledby="main-title">
        <h1 id="main-title">Fundația Umanitară Meridian S</h1>
        
        <p class="mission-text">Misiunea noastră este să aducem sprijin și speranță celor aflați în dificultate. Ne dedicăm proiectelor umanitare care schimbă vieți și dezvoltă comunități.</p>
        
        <div class="goals-box" aria-label="Obiectivele fundației">
            <h3>Ce ne propunem:</h3>
            <ul>
                <li>Sprijinirea familiilor defavorizate.</li>
                <li>Proiecte educaționale pentru copii, ghidare profesională pentru adolescenți și reorientare/susținere în reconversia profesională.</li>
                <li>Ajutor persoane vârstnice ce prezintă dizabilități sau dificultăți majore în viața de zi cu zi.</li>
            </ul>
        </div>
        <div class="donation-box" id="donatie-sectiune" aria-label="Detalii bancare pentru donații">
            <h3>Susține Activitatea Noastră 💝</h3>
            <div class="bank-details">
                <p><span>Beneficiar:</span> <strong>Fundația Umanitară Meridian S</strong></p>
                <p><span>Cont IBAN (RON):</span> <strong>RO48INGB0000999913484793</strong></p>
                <p><span>Banca:</span> <strong>ING Bank N.V. Sucursala București</strong></p>
                <p><span>Cod Fiscal (CUI):</span> <strong>9556400</strong></p>
                <p style="font-size: 13px; color: #7f8c8d; border: none; margin-top: 10px; text-align: center;">
                    *Vă rugăm să menționați „Donație Umanitara” la detaliile plății.
                </p>
            </div>
        </div>
        <a href="mailto:fundatiameridians@gmail.com" class="btn" rel="noopener noreferrer" aria-label="Devino voluntar / Contactează-ne">Devino Voluntar / Contactează-ne</a>
    </section>
    <div class="photo-column" aria-label="Galerie foto dreapta">
        <img class="gallery-img" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRzaknT7YK6MgjkYAy28i62tLz0-xzpqifG-g&s" alt="Comunitate și sprijin" />
        <img class="gallery-img" src="https://news.liverpool.ac.uk/wp-content/uploads/2023/02/GettyImages-14378301051.jpg" alt="Suport medical și bătrâni" />
    </div>
</main>
<footer>
    <p>&copy; 2026 Fundația Umanitară Meridian S. Toate drepturile rezervate.</p>
    <p>Scrie-ne la: <a href="mailto:fundatiameridians@gmail.com" class="email-link" rel="noopener noreferrer">fundatiameridians@gmail.com</a></p>
</footer>
</body>
</html>
   
Fundatia Umanitara Meridian S
