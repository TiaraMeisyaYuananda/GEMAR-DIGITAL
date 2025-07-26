# GEMAR-DIGITAL
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>GEMAR DIGITAL - Generasi Medis Berkarakter Digital</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    <style>
        :root {
            --primary: #00a8e8;
            --secondary: #2dc653;
            --accent: #ff9e00;
            --dark: #003459;
            --light: #f5f5f5;
            --white: #ffffff;
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--dark);
        }

        .logo-icon {
            width: 50px;
            height: 50px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: var(--gradient);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: -50%;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,122.7C672,117,768,139,864,154.7C960,171,1056,181,1152,165.3C1248,149,1344,107,1392,85.3L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            animation: wave 10s linear infinite;
        }

        @keyframes wave {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            z-index: 1;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 2rem;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: white;
            color: var(--primary);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .hero-image {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        /* Sections */
        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
        }

        .section-title p {
            font-size: 1.2rem;
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .about-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .about-card:hover {
            transform: translateY(-10px);
        }

        .about-card i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .about-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        /* Program Section */
        .program-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .program-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .program-card:hover {
            transform: translateY(-10px);
        }

        .program-image {
            height: 200px;
            background: var(--gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .program-content {
            padding: 2rem;
        }

        .program-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        /* Curriculum Section */
        .curriculum-timeline {
            position: relative;
            max-width: 800px;
            margin: 3rem auto;
        }

        .timeline-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 2rem;
            position: relative;
        }

        .timeline-icon {
            flex-shrink: 0;
            width: 60px;
            height: 60px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-right: 2rem;
        }

        .timeline-content {
            flex: 1;
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-item i {
            width: 50px;
            height: 50px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
        }

        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-family: inherit;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }

        .social-links a:hover {
            transform: translateY(-5px);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu {
                display: block;
            }

            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                justify-content: center;
            }
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.appear {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">
                <div class="logo-icon">
                    <i class="fas fa-heartbeat"></i>
                </div>
                <span>GEMAR DIGITAL</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Beranda</a></li>
                <li><a href="#about">Tentang</a></li>
                <li><a href="#programs">Program</a></li>
                <li><a href="#curriculum">Kurikulum</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>GEMAR DIGITAL</h1>
                    <p>Generasi Medis Berkarakter Digital<br>
                    <em>"Berkarya di Dunia Medis, Berjiwa Kemanusiaan"</em></p>
                    <div class="cta-buttons">
                        <a href="#programs" class="btn btn-primary">
                            <i class="fas fa-rocket"></i>
                            Bergabung Sekarang
                        </a>
                        <a href="#about" class="btn btn-secondary">
                            <i class="fas fa-info-circle"></i>
                            Pelajari Lebih
                        </a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Dokter Digital" />
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Visi & Misi Kami</h2>
                <p>Menciptakan generasi dokter yang terampil di bidang teknologi medis digital tanpa kehilangan esensi humanisme</p>
            </div>
            <div class="about-grid">
                <div class="about-card fade-in">
                    <i class="fas fa-eye"></i>
                    <h3>Visi</h3>
                    <p>Menciptakan generasi dokter yang terampil di bidang teknologi medis digital tanpa kehilangan esensi humanisme dalam pelayanan kesehatan.</p>
                </div>
                <div class="about-card fade-in">
                    <i class="fas fa-target"></i>
                    <h3>Misi 1</h3>
                    <p>Mengisi kesenjangan antara pelatihan teknologi medis dan pengembangan karakter humanis.</p>
                </div>
                <div class="about-card fade-in">
                    <i class="fas fa-lightbulb"></i>
                    <h3>Misi 2</h3>
                    <p>Menghasilkan dokter yang kritis, etis, dan inovatif di era digital.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="programs" style="background: var(--light);">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Program Unggulan</h2>
                <p>"The Empathy Algorithm" - Membangun empati klinis melalui pendekatan teknologi dan mentoring</p>
            </div>
            <div class="program-grid">
                <div class="program-card fade-in">
                    <div class="program-image">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="program-content">
                        <h3>Studi Kasus AI</h3>
                        <p>Analisis skenario diagnostik menggunakan AI dengan fokus pada konsekuensi etika dan empati.</p>
                    </div>
                </div>
                <div class="program-card fade-in">
                    <div class="program-image">
                        <i class="fas fa-vr-cardboard"></i>
                    </div>
                    <div class="program-content">
                        <h3>Simulasi Komunikasi</h3>
                        <p>Pelatihan bermain peran dengan pasien virtual (VR) untuk membangun keterampilan komunikasi sensitif budaya.</p>
                    </div>
                </div>
                <div class="program-card fade-in">
                    <div class="program-image">
                        <i class="fas fa-user-md"></i>
                    </div>
                    <div class="program-content">
                        <h3>Mentoring Dokter Senior</h3>
                        <p>Diskusi bulanan dengan dokter berpengalaman tentang tantangan humanisme di era digital.</p>
                    </div>
                </div>
                <div class="program-card fade-in">
                    <div class="program-image">
                        <i class="fas fa-users"></i>
                    </div>
                    <div class="program-content">
                        <h3>Workshop Kolaborasi</h3>
                        <p>Kolaborasi dengan insinyur dan etikawan untuk mengembangkan solusi teknologi yang ramah pasien.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="curriculum">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Kurikulum Mini</h2>
                <p>"Etika dan Karakter Dokter di Era Digital" - 8 sesi untuk mahasiswa kedokteran tahun pertama</p>
            </div>
            <div class="curriculum-timeline">
                <div class="timeline-item fade-in">
                    <div class="timeline-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Privasi Digital Pasien</h3>
                        <p>Perlindungan data kesehatan dalam sistem elektronik</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Etika Penggunaan AI</h3>
                        <p>Tanggung jawab moral saat menggunakan alat diagnostik AI</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-icon">
                        <i class="fas fa-heart"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Empati vs. Otomatisasi</h3>
                        <p>Studi kasus tentang dehumanisasi dalam pelayanan kesehatan digital</p>
                    </div>
                </div>
                <div class="timeline-item fade-in">
                    <div class="timeline-icon">
                        <i class="fas fa-laptop-medical"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Personalisasi dalam Telemedisin</h3>
                        <p>Strategi membangun kepercayaan pasien secara virtual</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" style="background: var(--light);">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Hubungi Kami</h2>
                <p>Bersama GEMAR DIGITAL, kita wujudkan dokter masa depan yang tak hanya cakap teknologi, tapi juga berhati!</p>
            </div>
            <div class="contact-grid">
                <div class="contact-info">
                    <div class="contact-item fade-in">
                        <i class="fab fa-whatsapp"></i>
                        <div>
                            <h4>WhatsApp/Telegram</h4>
                            <p>+62 857 6453 3145</p>
                        </div>
                    </div>
                    <div class="contact-item fade-in">
                        <i class="fab fa-instagram"></i>
                        <div>
                            <h4>Instagram</h4>
                            <p>@GemarDigital2025</p>
                        </div>
                    </div>
                    <div class="contact-item fade-in">
                        <i class="fab fa-facebook"></i>
                        <div>
                            <h4>Facebook</h4>
                            <p>GEMAR DIGITAL</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form fade-in">
                    <form>
                        <div class="form-group">
                            <label>Nama Lengkap</label>
                            <input type="text" placeholder="Masukkan nama Anda" required>
                        </div>
                        <div class="form-group">
                            <label>Email</label>
                            <input type="email" placeholder="Masukkan email Anda" required>
                        </div>
                        <div class="form-group">
                            <label>Pesan</label>
                            <textarea rows="4" placeholder="Tulis pesan Anda" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">
                            <i class="fas fa-paper-plane"></i>
                            Kirim Pesan
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>GEMAR DIGITAL</h3>
                    <p>Generasi Medis Berkarakter Digital<br>
                    "Berkarya di Dunia Medis, Berjiwa Kemanusiaan"</p>
                </div>
                <div class="footer-section">
                    <h3>Kontak</h3>
                    <p>WhatsApp/Telegram: +62 857 6453 3145</p>
                </div>
                <div class="footer-section">
                    <h3>Media Sosial</h3>
                    <p>Instagram/Facebook: @GemarDigital2025</p>
                </div>
            </div>
            <div class="social-links">
                <a href="#"><i class="fab fa-whatsapp"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-telegram"></i></a>
            </div>
            <p>&copy; 2025 GEMAR DIGITAL. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Fade in animation on scroll
        const faders = document.querySelectorAll('.fade-in');
        const appearOptions = {
            threshold: 0.15,
            rootMargin: "0px 0px -100px 0px"
        };

        const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll) {
            entries.forEach(entry => {
                if (!entry.isIntersecting) return;
                entry.target.classList.add('appear');
                appearOnScroll.unobserve(entry.target);
            });
        }, appearOptions);

        faders.forEach(fader => {
            appearOnScroll.observe(fader);
        });

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Terima kasih! Pesan Anda telah terkirim.');
            this.reset();
        });

        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
                header.style.boxShadow = '0 2px 30px rgba(0, 0, 0, 0.2)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
                header.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>

Web
