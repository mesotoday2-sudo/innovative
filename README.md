<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Innovative Financial - Empowering Your Financial Future</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #B89538;
            --primary-dark: #9A7D2F;
            --primary-light: #D4B15F;
            --bg: #FFFFFF;
            --panel: #F8F9FA;
            --text: #2D3748;
            --muted: #718096;
            --border: #E2E8F0;
            --glass-alpha: 0.85;
            --radius: 12px;
            --shadow: 0 4px 12px rgba(0,0,0,0.08);
            --transition: all 0.3s ease;
        }

        [data-theme="dark"] {
            --bg: #0F1419;
            --panel: #1A202C;
            --text: #E2E8F0;
            --muted: #A0AEC0;
            --border: #2D3748;
            --shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            font-size: 16px;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--bg);
            transition: var(--transition);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(255,255,255,var(--glass-alpha));
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            transition: var(--transition);
        }

        [data-theme="dark"] header {
            background: rgba(15,20,25,var(--glass-alpha));
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 16px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 700;
            font-size: 24px;
            color: var(--primary);
        }

        .logo-icon {
            font-size: 28px;
        }

        .nav-links {
            display: flex;
            gap: 32px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-links a i {
            color: var(--primary);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            color: var(--text);
            cursor: pointer;
        }

        .mobile-nav {
            display: none;
            flex-direction: column;
            gap: 0;
            padding: 20px 0;
            border-top: 1px solid var(--border);
        }

        .mobile-nav.active {
            display: flex;
        }

        .mobile-nav a {
            padding: 12px 0;
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 12px;
            border-bottom: 1px solid var(--border);
        }

        .mobile-nav a i {
            color: var(--primary);
            width: 24px;
            text-align: center;
        }

        .btn {
            padding: 12px 24px;
            border-radius: var(--radius);
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            justify-content: center;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(184, 149, 56, 0.3);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--text);
            border: 1px solid var(--border);
        }

        .btn-secondary:hover {
            border-color: var(--primary);
            color: var(--primary);
        }

        .theme-toggle {
            background: none;
            border: none;
            cursor: pointer;
            color: var(--text);
            font-size: 20px;
            padding: 8px;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .theme-toggle:hover {
            background-color: var(--panel);
        }

        .hero {
            padding: 120px 0 80px;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 700px;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 48px;
            font-weight: 700;
            margin-bottom: 24px;
            line-height: 1.1;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 40px;
            color: var(--muted);
        }

        .hero-actions {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        .glass-card {
            background: rgba(255,255,255,var(--glass-alpha));
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            box-shadow: var(--shadow);
            border-radius: var(--radius);
            padding: 24px;
            transition: var(--transition);
        }

        [data-theme="dark"] .glass-card {
            background: rgba(15,20,25,var(--glass-alpha));
            border: 1px solid rgba(255,255,255,0.05);
        }

        .glass-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.12);
        }

        .section {
            padding: 80px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 36px;
            margin-bottom: 16px;
            color: var(--text);
        }

        .section-header p {
            font-size: 18px;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            padding: 30px;
            height: 100%;
            display: flex;
            flex-direction: column;
            text-align: center;
        }

        .service-icon {
            width: 70px;
            height: 70px;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: var(--primary);
            background-color: var(--panel);
            border-radius: 50%;
        }

        .service-card h3 {
            font-size: 20px;
            margin-bottom: 16px;
        }

        .service-card p {
            color: var(--muted);
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .team-card {
            text-align: center;
            padding: 30px 20px;
        }

        .team-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto 20px;
            border: 3px solid var(--primary);
            background-color: var(--panel);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px;
            color: var(--primary);
        }

        .team-card h3 {
            margin-bottom: 8px;
        }

        .team-card .role {
            color: var(--primary);
            margin-bottom: 16px;
            font-weight: 500;
        }

        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }

        .value-item {
            text-align: center;
            padding: 30px 20px;
        }

        .value-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: var(--panel);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 32px;
            color: var(--primary);
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        .contact-detail {
            display: flex;
            align-items: flex-start;
            gap: 16px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--panel);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            flex-shrink: 0;
            font-size: 20px;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .form-group label {
            font-weight: 500;
        }

        .form-control {
            padding: 12px 16px;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            background-color: var(--panel);
            color: var(--text);
            font-family: inherit;
            transition: var(--transition);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(184, 149, 56, 0.2);
        }

        .qr-section {
            text-align: center;
            margin-top: 30px;
            padding: 30px;
            background-color: var(--panel);
            border-radius: var(--radius);
        }

        .qr-code {
            width: 180px;
            height: 180px;
            margin: 0 auto 20px;
            background: white;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .qr-code i {
            font-size: 100px;
            color: var(--primary);
        }

        .qr-text {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--primary);
        }

        .qr-subtext {
            color: var(--muted);
            font-size: 14px;
        }

        footer {
            background-color: var(--panel);
            padding: 60px 0 30px;
            margin-top: 80px;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 16px;
            color: var(--primary);
        }

        .footer-links h3 {
            margin-bottom: 20px;
            font-size: 18px;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            text-decoration: none;
            color: var(--muted);
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-links a i {
            color: var(--primary);
            width: 16px;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid var(--border);
            color: var(--muted);
            font-size: 14px;
        }

        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 40px;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero-actions {
                flex-direction: column;
            }
            
            .section-header h2 {
                font-size: 28px;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .glass-card {
                padding: 20px;
            }
            
            .section {
                padding: 60px 0;
            }
        }

        @media (max-width: 480px) {
            .hero {
                padding: 100px 0 60px;
            }
            
            .hero h1 {
                font-size: 28px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .section-header h2 {
                font-size: 24px;
            }
            
            .section-header p {
                font-size: 16px;
            }
            
            .service-card, .team-card, .value-item {
                padding: 20px 15px;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-chart-line logo-icon"></i>
                <span>Innovative Financial</span>
            </div>
            <nav class="nav-links">
                <a href="#home"><i class="fas fa-home"></i> Home</a>
                <a href="#about"><i class="fas fa-building"></i> About</a>
                <a href="#services"><i class="fas fa-concierge-bell"></i> Services</a>
                <a href="#team"><i class="fas fa-users"></i> Team</a>
                <a href="#contact"><i class="fas fa-envelope"></i> Contact</a>
            </nav>
            <div class="header-actions">
                <button class="theme-toggle" id="theme-toggle" aria-label="Toggle theme">
                    <i class="fas fa-moon"></i>
                </button>
                <a href="#contact" class="btn btn-primary">
                    <i class="fas fa-calendar-check"></i> Get a Consult
                </a>
                <button class="mobile-menu-btn" id="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
        <nav class="mobile-nav" id="mobile-nav">
            <a href="#home"><i class="fas fa-home"></i> Home</a>
            <a href="#about"><i class="fas fa-building"></i> About</a>
            <a href="#services"><i class="fas fa-concierge-bell"></i> Services</a>
            <a href="#team"><i class="fas fa-users"></i> Team</a>
            <a href="#contact"><i class="fas fa-envelope"></i> Contact</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Empowering Your Financial Future</h1>
                <p>Trusted financial partners for sustainable growth through innovation and integrity.</p>
                <div class="hero-actions">
                    <a href="#contact" class="btn btn-primary">
                        <i class="fas fa-calendar-alt"></i> Get a Free Consult
                    </a>
                    <a href="#services" class="btn btn-secondary">
                        <i class="fas fa-search"></i> Explore Services
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="services">
        <div class="container">
            <div class="section-header">
                <h2>Comprehensive Financial Solutions</h2>
                <p>Tailored to your unique needs and goals</p>
            </div>
            <div class="services-grid">
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-calculator"></i>
                    </div>
                    <h3>Accounting & Bookkeeping</h3>
                    <p>Ensure precision, compliance, and clarity with our professional accounting support.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-file-invoice-dollar"></i>
                    </div>
                    <h3>Tax Planning & Advisory</h3>
                    <p>Optimize your tax outcomes while maintaining full legal and regulatory compliance.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-briefcase"></i>
                    </div>
                    <h3>Business Consulting</h3>
                    <p>Improve efficiency, profitability, and decision-making with expert financial insights.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <h3>Financial Planning</h3>
                    <p>Develop personalized financial strategies that align with your goals and long-term stability.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-search-dollar"></i>
                    </div>
                    <h3>Audit & Assurance</h3>
                    <p>Independent reviews that strengthen credibility and provide deeper financial clarity.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
                <div class="glass-card service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Corporate Advisory</h3>
                    <p>Guidance for startups and established companies looking to expand or restructure.</p>
                    <a href="#" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Learn More
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="about">
        <div class="container">
            <div class="section-header">
                <h2>Who We Are</h2>
                <p>Innovative Financial is a forward-thinking financial services company built on trust, transparency, and innovation.</p>
            </div>
            <div class="glass-card fade-in" style="padding: 40px; margin-bottom: 60px;">
                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 40px; align-items: center;">
                    <div>
                        <p style="margin-bottom: 20px;">We provide individuals and businesses with strategic financial guidance to help them grow, plan, and secure their future.</p>
                        <p>Our goal is not only to manage numbers but to create lasting financial confidence and value for every client we serve.</p>
                    </div>
                    <div style="background-color: var(--panel); height: 300px; border-radius: var(--radius); display: flex; align-items: center; justify-content: center;">
                        <i class="fas fa-building" style="font-size: 80px; color: var(--primary);"></i>
                    </div>
                </div>
                <div style="text-align: center; margin-top: 30px; padding: 20px; border-left: 3px solid var(--primary); background-color: var(--panel); border-radius: var(--radius);">
                    <p style="font-size: 18px; font-weight: 500;"><i class="fas fa-quote-left" style="color: var(--primary); margin-right: 10px;"></i>Creating financial confidence through innovation and integrity.<i class="fas fa-quote-right" style="color: var(--primary); margin-left: 10px;"></i></p>
                </div>
            </div>

            <div class="section-header">
                <h2>Our Mission, Vision & Core Values</h2>
            </div>
            
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 40px; margin-bottom: 60px;">
                <div class="glass-card fade-in">
                    <h3 style="margin-bottom: 16px; color: var(--primary); display: flex; align-items: center; gap: 10px;">
                        <i class="fas fa-bullseye"></i> Mission
                    </h3>
                    <p>To deliver transparent, innovative, and results-driven financial services that empower individuals and businesses to achieve their goals.</p>
                </div>
                <div class="glass-card fade-in">
                    <h3 style="margin-bottom: 16px; color: var(--primary); display: flex; align-items: center; gap: 10px;">
                        <i class="fas fa-eye"></i> Vision
                    </h3>
                    <p>To be recognized as a leading financial partner that combines expertise, technology, and integrity to shape a better financial future.</p>
                </div>
            </div>

            <div class="values-grid">
                <div class="glass-card value-item fade-in">
                    <div class="value-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Integrity</h3>
                    <p>We uphold the highest ethical standards in all our interactions.</p>
                </div>
                <div class="glass-card value-item fade-in">
                    <div class="value-icon">
                        <i class="fas fa-lightbulb"></i>
                    </div>
                    <h3>Innovation</h3>
                    <p>We embrace new technologies and approaches to deliver better solutions.</p>
                </div>
                <div class="glass-card value-item fade-in">
                    <div class="value-icon">
                        <i class="fas fa-star"></i>
                    </div>
                    <h3>Excellence</h3>
                    <p>We strive for the highest quality in everything we do.</p>
                </div>
                <div class="glass-card value-item fade-in">
                    <div class="value-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Trust</h3>
                    <p>We build lasting relationships based on reliability and transparency.</p>
                </div>
                <div class="glass-card value-item fade-in">
                    <div class="value-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3>Sustainability</h3>
                    <p>We focus on long-term value creation for our clients and community.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="team">
        <div class="container">
            <div class="section-header">
                <h2>Meet Our Experts</h2>
                <p>Our team is composed of certified financial specialists with years of professional experience.</p>
            </div>
            <div class="team-grid">
                <div class="glass-card team-card fade-in">
                    <div class="team-photo">
                        <i class="fas fa-user"></i>
                    </div>
                    <h3>John Smith</h3>
                    <p class="role">Senior Financial Advisor</p>
                    <p>15+ years experience in wealth management and financial planning.</p>
                </div>
                <div class="glass-card team-card fade-in">
                    <div class="team-photo">
                        <i class="fas fa-user"></i>
                    </div>
                    <h3>Sarah Johnson</h3>
                    <p class="role">Tax Specialist</p>
                    <p>Expert in tax optimization strategies for individuals and businesses.</p>
                </div>
                <div class="glass-card team-card fade-in">
                    <div class="team-photo">
                        <i class="fas fa-user"></i>
                    </div>
                    <h3>Michael Brown</h3>
                    <p class="role">Business Consultant</p>
                    <p>Helping businesses improve efficiency and profitability through data-driven insights.</p>
                </div>
                <div class="glass-card team-card fade-in">
                    <div class="team-photo">
                        <i class="fas fa-user"></i>
                    </div>
                    <h3>Emily Davis</h3>
                    <p class="role">Audit Director</p>
                    <p>Ensuring financial compliance and transparency for our corporate clients.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="contact">
        <div class="container">
            <div class="section-header">
                <h2>Let's Build Your Financial Future Together</h2>
                <p>Contact us today and take the next step toward financial confidence.</p>
            </div>
            <div class="glass-card fade-in" style="padding: 40px;">
                <div class="contact-container">
                    <div class="contact-info">
                        <h3 style="margin-bottom: 24px;">Get In Touch</h3>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Address</h4>
                                <p>96, Dagbreek Street<br>Cape Town, South Africa</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+27 78 260 4809</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>info@innovativefinancial.com</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <i class="fas fa-globe"></i>
                            </div>
                            <div>
                                <h4>Website</h4>
                                <p>www.innovativefinancial.com</p>
                            </div>
                        </div>
                        
                        <div class="qr-section">
                            <div class="qr-code">
                                <i class="fas fa-qrcode"></i>
                            </div>
                            <p class="qr-text">Scan to get a consult</p>
                            <p class="qr-subtext">Point your camera at the code to schedule your free consultation</p>
                        </div>
                    </div>
                    <div class="contact-form">
                        <h3 style="margin-bottom: 10px;">Send Us a Message</h3>
                        <p style="color: var(--muted); margin-bottom: 20px;">We'll get back to you within 24 business hours.</p>
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Your name">
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="Your email">
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" class="form-control" placeholder="Your phone">
                        </div>
                        <div class="form-group">
                            <label for="service">Service Interested In</label>
                            <select id="service" class="form-control">
                                <option value="">Select a service</option>
                                <option value="accounting">Accounting & Bookkeeping</option>
                                <option value="tax">Tax Planning & Advisory</option>
                                <option value="consulting">Business Consulting</option>
                                <option value="planning">Financial Planning</option>
                                <option value="audit">Audit & Assurance</option>
                                <option value="corporate">Corporate Advisory</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" rows="5" placeholder="How can we help you?"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">
                            <i class="fas fa-paper-plane"></i> Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-container">
                <div>
                    <div class="footer-logo">
                        <i class="fas fa-chart-line"></i>
                        <span>Innovative Financial</span>
                    </div>
                    <p>Empowering your financial future through innovation and integrity.</p>
                </div>
                <div class="footer-links">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-calculator"></i> Accounting</a></li>
                        <li><a href="#"><i class="fas fa-file-invoice-dollar"></i> Tax Planning</a></li>
                        <li><a href="#"><i class="fas fa-briefcase"></i> Business Consulting</a></li>
                        <li><a href="#"><i class="fas fa-chart-pie"></i> Financial Planning</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Company</h3>
                    <ul>
                        <li><a href="#about"><i class="fas fa-building"></i> About Us</a></li>
                        <li><a href="#team"><i class="fas fa-users"></i> Our Team</a></li>
                        <li><a href="#contact"><i class="fas fa-envelope"></i> Contact</a></li>
                        <li><a href="#"><i class="fas fa-briefcase"></i> Careers</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Connect</h3>
                    <ul>
                        <li><a href="#"><i class="fab fa-linkedin"></i> LinkedIn</a></li>
                        <li><a href="#"><i class="fab fa-twitter"></i> Twitter</a></li>
                        <li><a href="#"><i class="fab fa-facebook"></i> Facebook</a></li>
                        <li><a href="#"><i class="fab fa-instagram"></i> Instagram</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 Innovative Financial. All rights reserved. Website: www.innovativefinancial.com Email: info@innovativefinancial.com</p>
            </div>
        </div>
    </footer>

    <script>
        const toggle = document.getElementById('theme-toggle');
        const root = document.documentElement;
        const themeIcon = document.querySelector('.theme-toggle i');
        
        const saved = localStorage.getItem('theme') || (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
        if(saved === 'dark') {
            root.setAttribute('data-theme','dark');
            themeIcon.className = 'fas fa-sun';
        }

        toggle.addEventListener('click', ()=>{
            const current = root.getAttribute('data-theme') === 'dark' ? 'light' : 'dark';
            root.setAttribute('data-theme', current);
            localStorage.setItem('theme', current);
            
            if(current === 'dark') {
                themeIcon.className = 'fas fa-sun';
            } else {
                themeIcon.className = 'fas fa-moon';
            }
        });

        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileNav = document.getElementById('mobile-nav');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileNav.classList.toggle('active');
            const icon = mobileMenuBtn.querySelector('i');
            if (mobileNav.classList.contains('active')) {
                icon.className = 'fas fa-times';
            } else {
                icon.className = 'fas fa-bars';
            }
        });

        const fadeElements = document.querySelectorAll('.fade-in');
        
        const fadeInOnScroll = () => {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < window.innerHeight - elementVisible) {
                    element.classList.add('visible');
                }
            });
        };
        
        window.addEventListener('scroll', fadeInOnScroll);
        window.addEventListener('load', fadeInOnScroll);
        
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    if (mobileNav.classList.contains('active')) {
                        mobileNav.classList.remove('active');
                        mobileMenuBtn.querySelector('i').className = 'fas fa-bars';
                    }
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
