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

    /* Header Styles */
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

    /* Mobile Menu */
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

    /* Button Styles */
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

    /* Theme Toggle */
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

    /* Hero Section */
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

    /* Glassmorphic Card */
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

    /* Section Styling */
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

    /* Services Grid */
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

    /* Team Grid */
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

    /* Values Section */
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

    /* Contact Section */
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

    /* QR Code Section */
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

    /* Footer */
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

    /* Responsive Design */
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
    }

    /* Animation Classes */
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
