<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TUMC INDONESIA - Komunitas Masyarakat</title>
    <style>
        /* RESET & BASE STYLES */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0b0b0b;
            color: #ffffff;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* NAVIGATION */
        header {
            background-color: #111111;
            border-bottom: 3px solid #ff0000;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ff0000;
            letter-spacing: 2px;
        }

        .logo span {
            color: #ffffff;
        }

        .nav-container {
            display: flex;
            align-items: center;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 20px;
        }

        .nav-links a {
            font-weight: 600;
            transition: color 0.3s;
            text-transform: uppercase;
            font-size: 0.9rem;
        }

        .nav-links a:hover {
            color: #ff0000;
        }

        .btn-ig-nav {
            background-color: #ff0000;
            padding: 5px 12px;
            border-radius: 4px;
            margin-left: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            text-transform: uppercase;
            transition: transform 0.3s, background-color 0.3s;
        }

        .btn-ig-nav:hover {
            background-color: #cc0000;
            transform: scale(1.05);
        }

        /* HERO SECTION */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(11, 11, 11, 1)), url('https://images.unsplash.com/photo-1515162305285-0293e4767cc2?auto=format&fit=crop&q=80&w=1920') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3.5rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            margin-bottom: 10px;
            color: #ffffff;
        }

        .hero h1 span {
            color: #ff0000;
            text-shadow: 0 0 10px rgba(255, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 30px;
            color: #cccccc;
        }

        .btn-join {
            background-color: #ff0000;
            color: #ffffff;
            padding: 12px 30px;
            font-weight: bold;
            text-transform: uppercase;
            border-radius: 5px;
            transition: background 0.3s, transform 0.3s;
            box-shadow: 0 4px 15px rgba(255, 0, 0, 0.4);
        }

        .btn-join:hover {
            background-color: #cc0000;
            transform: translateY(-3px);
        }

        /* ABOUT SECTION */
        .about {
            padding: 80px 5%;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .section-title {
            font-size: 2.5rem;
            text-transform: uppercase;
            margin-bottom: 40px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            background-color: #ff0000;
            bottom: -10px;
            left: 25%;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 30px;
            text-align: left;
            margin-top: 20px;
        }

        .ketum-card {
            background-color: #161616;
            border: 2px solid #ff0000;
            padding: 30px;
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            box-shadow: 0 5px 15px rgba(255, 0, 0, 0.1);
        }

        .ketum-avatar {
            width: 100px;
            height: 100px;
            background-color: #222;
            border: 3px solid #ff0000;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 2rem;
            color: #ff0000;
            margin-bottom: 15px;
        }

        .ketum-title {
            font-size: 0.85rem;
            text-transform: uppercase;
            color: #aaa;
            letter-spacing: 1px;
        }

        .ketum-name {
            font-size: 1.3rem;
            font-weight: bold;
            color: #ffffff;
            margin-top: 5px;
        }

        .about-content {
            background-color: #161616;
            border-left: 5px solid #ff0000;
            padding: 30px;
            border-radius: 0 10px 10px 0;
            display: flex;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
        }

        /* ACTIVITIES / AGENDA */
        .activities {
            background-color: #111111;
            padding: 80px 5%;
        }

        .activity-container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .card {
            background-color: #1a1a1a;
            border: 1px solid #333;
            padding: 25px;
            border-radius: 8px;
            transition: transform 0.3s, border-color 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: #ff0000;
        }

        .card h3 {
            color: #ff0000;
            margin-bottom: 15px;
            text-transform: uppercase;
        }

        /* FOOTER */
        footer {
            background-color: #050505;
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid #222;
            font-size: 0.9rem;
            color: #666;
        }

        footer span {
            color: #ff0000;
        }

        .footer-social {
            margin-bottom: 20px;
        }

        .btn-ig-footer {
            display: inline-block;
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            color: #fff;
            padding: 10px 24px;
            font-weight: bold;
            border-radius: 30px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn-ig-footer:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(220, 39, 67, 0.4);
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .nav-links, .btn-ig-nav {
                display: none; 
            }
            .hero h1 {
                font-size: 2.3rem;
            }
            .hero p {
                font-size: 1rem;
            }
            .about-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- NAVIGATION -->
    <header>
        <div class="navbar">
            <div class="logo">TUMC <span>INDONESIA</span></div>
            <div class="nav-container">
                <ul class="nav-links">
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#about">Tentang Kami</a></li>
                    <li><a href="#activities">Kegiatan</a></li>
                </ul>
                <a href="https://www.instagram.com/dpp_tumc_indonesia?igsh=MXJhcWJ3MWdnaXNqcg==" target="_blank" class="btn-ig-nav">Instagram</a>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <h1>Solidaritas Tanpa <span>Batas</span></h1>
        <p>Wadah berkumpulnya masyarakat yang menjunjung tinggi persaudaraan, aksi sosial, dan nilai-nilai kebersamaan di Indonesia.</p>
        <a href="https://www.instagram.com/dpp_tumc_indonesia?igsh=MXJhcWJ3MWdnaXNqcg==" target="_blank" class="btn-join">Kunjungi Instagram</a>
    </section>

    <!-- ABOUT SECTION -->
    <section class="about" id="about">
        <h2 class="section-title">Tentang TUMC</h2>
        
        <div class="about-grid">
            <!-- KETUA UMUM CARD -->
            <div class="ketum-card">
                <div class="ketum-avatar">MS</div>
                <div class="ketum-title">Ketua Umum</div>
                <div class="ketum-name">MOCHAMAD SULTAN AGENTA</div>
            </div>

            <!-- TENTANG KAMI CONTENT -->
            <div class="about-content">
                <p><strong>TUMC INDONESIA</strong> adalah komunitas masyarakat berskala nasional yang bergerak atas dasar asas kekeluargaan, gotong royong, dan kepedulian sosial. Di bawah kepemimpinan <strong>Mochamad Sultan Agenta</strong> selaku Ketua Umum, kami berkomitmen untuk menjadi wadah positif tempat bertukar pikiran, menyalurkan hobi, serta bergerak bersama melakukan aksi nyata demi kesejahteraan masyarakat umum.</p>
            </div>
        </div>
    </section>

    <!-- ACTIVITIES SECTION -->
    <section class="activities" id="activities">
        <div class="activity-container">
            <h2 class="section-title">Kegiatan Kami</h2>
            <div class="grid">
                <div class="card">
                    <h3>Aksi Sosial</h3>
                    <p>Penyaluran bantuan, donor darah, dan tanggap bencana untuk membantu sesama yang membutuhkan.</p>
                </div>
                <div class="card">
                    <h3>Kopdar & Sharing</h3>
                    <p>Pertemuan rutin untuk mempererat tali silaturahmi antar anggota dan membahas program kerja komunitas.</p>
                </div>
                <div class="card">
                    <h3>Touring & Edukasi</h3>
                    <p>Menjelajah keindahan alam Indonesia sekaligus mengampanyekan keselamatan dan ketertiban di masyarakat.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-social">
            <a href="https://www.instagram.com/dpp_tumc_indonesia?igsh=MXJhcWJ3MWdnaXNqcg==" target="_blank" class="btn-ig-footer">Follow @dpp_tumc_indonesia</a>
        </div>
        <p>&copy; 2026 <span>TUMC INDONESIA</span>. All Rights Reserved. Dipimpin oleh Mochamad Sultan Agenta.</p>
    </footer>

</body>
</html>
