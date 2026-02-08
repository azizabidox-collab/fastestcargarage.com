html
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FASTEST CAR GARAGE | أسرع كراج للسيارات</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary-green: #00a859;
            --dark-green: #008046;
            --black: #000000;
            --light-black: #111111;
            --gray: #222222;
            --light-gray: #f5f5f5;
            --white: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Arial, sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            background-color: var(--black);
            color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .section {
            padding: 80px 0;
        }
        
        /* Bilingual Text */
        .bilingual {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .english {
            font-weight: 600;
        }
        
        .arabic {
            font-weight: 600;
            direction: rtl;
            font-size: 1.1em;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        /* Header */
        header {
            background-color: var(--black);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid var(--primary-green);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--primary-green);
        }
        
        .logo-text {
            display: flex;
            flex-direction: column;
        }
        
        .logo-main {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--white);
            letter-spacing: 1px;
        }
        
        .logo-arabic {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--primary-green);
            direction: rtl;
        }
        
        .tagline {
            font-size: 0.9rem;
            color: #aaa;
            margin-top: 5px;
        }
        
        /* Navigation */
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }
        
        nav ul li a:hover {
            color: var(--primary-green);
        }
        
        nav ul li a .arabic-nav {
            font-size: 0.9rem;
            color: #aaa;
            direction: rtl;
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            padding: 180px 0 120px;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 20px;
            color: var(--white);
        }
        
        .hero h1 span {
            color: var(--primary-green);
        }
        
        .hero-subtitle {
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: var(--primary-green);
            font-weight: 700;
        }
        
        .hero-arabic {
            font-size: 2rem;
            color: var(--white);
            margin-bottom: 40px;
            direction: rtl;
            font-weight: 700;
        }
        
        .hero-tagline {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 50px;
            color: #ccc;
        }
        
        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        
        .btn-primary {
            background-color: var(--primary-green);
            color: var(--white);
        }
        
        .btn-primary:hover {
            background-color: var(--dark-green);
            transform: translateY(-5px);
        }
        
        .btn-secondary {
            background-color: transparent;
            color: var(--white);
            border: 2px solid var(--primary-green);
        }
        
        .btn-secondary:hover {
            background-color: var(--primary-green);
            transform: translateY(-5px);
        }
        
        /* Services Section */
        .services {
            background-color: var(--light-black);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title .english {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--white);
        }
        
        .section-title .arabic {
            font-size: 1.8rem;
            color: var(--primary-green);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--gray);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
            border-top: 5px solid var(--primary-green);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            background-color: var(--black);
            color: var(--primary-green);
            font-size: 3rem;
            padding: 30px;
            text-align: center;
        }
        
        .service-content {
            padding: 30px;
        }
        
        .service-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--white);
        }
        
        .service-content p {
            color: #ccc;
            margin-bottom: 20px;
        }
        
        /* About Section */
        .about {
            background-color: var(--black);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
            align-items: center;
        }
        
        .about-text {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .about-text h2 {
            font-size: 2.2rem;
            color: var(--primary-green);
            margin-bottom: 10px;
        }
        
        .about-arabic {
            font-size: 1.5rem;
            color: var(--white);
            direction: rtl;
            margin-bottom: 20px;
            font-weight: 600;
        }
        
        .about-features {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }
        
        .feature {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .feature i {
            color: var(--primary-green);
            font-size: 1.5rem;
        }
        
        /* Hours & Contact */
        .info-section {
            background-color: var(--light-black);
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .info-card {
            background-color: var(--gray);
            border-radius: 10px;
            padding: 40px;
            border-left: 5px solid var(--primary-green);
        }
        
        .info-card h3 {
            font-size: 1.8rem;
            margin-bottom: 25px;
            color: var(--white);
        }
        
        .hours-list {
            list-style: none;
        }
        
        .hours-list li {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #444;
        }
        
        .closed {
            color: #ff4444;
            font-weight: 700;
        }
        
        .contact-info p {
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-info i {
            color: var(--primary-green);
            font-size: 1.2rem;
            width: 25px;
        }
        
        .contact-info a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .contact-info a:hover {
            color: var(--primary-green);
        }
        
        /* Branding Section */
        .branding {
            background-color: var(--black);
            text-align: center;
        }
        
        .branding-title {
            font-size: 2.5rem;
            color: var(--primary-green);
            margin-bottom: 20px;
        }
        
        .branding-subtitle {
            font-size: 1.2rem;
            color: #ccc;
            max-width: 800px;
            margin: 0 auto 50px;
        }
        
        .brand-logos {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .brand-logo-item {
            background-color: var(--gray);
            padding: 30px;
            border-radius: 10px;
            min-width: 250px;
            border: 2px solid var(--primary-green);
        }
        
        .brand-logo-text {
            font-size: 2rem;
            font-weight: 800;
            color: var(--white);
            margin-bottom: 10px;
        }
        
        .brand-logo-arabic {
            font-size: 1.5rem;
            color: var(--primary-green);
            direction: rtl;
            font-weight: 700;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
        }
        
        .social-icon {
            width: 60px;
            height: 60px;
            background-color: var(--gray);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.5rem;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-icon:hover {
            background-color: var(--primary-green);
            transform: translateY(-5px);
        }
        
        /* Footer */
        footer {
            background-color: var(--black);
            padding: 60px 0 30px;
            border-top: 3px solid var(--primary-green);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: var(--primary-green);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 15px;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .footer-column ul li a:hover {
            color: var(--primary-green);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #333;
            color: #888;
            font-size: 0.9rem;
        }
        
        /* Language Toggle */
        .lang-toggle {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: 30px;
        }
        
        .lang-btn {
            background: none;
            border: none;
            color: #aaa;
            font-weight: 600;
            cursor: pointer;
            padding: 5px 10px;
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        .lang-btn.active {
            background-color: var(--primary-green);
            color: var(--white);
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--black);
                flex-direction: column;
                padding: 20px;
                border-top: 2px solid var(--primary-green);
            }
            
            nav ul.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero-subtitle {
                font-size: 1.5rem;
            }
        }
        
        @media (max-width: 768px) {
            .hero {
                padding: 150px 0 80px;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .about-features {
                grid-template-columns: 1fr;
            }
            
            .lang-toggle {
                margin-left: 0;
                margin-top: 15px;
                justify-content: center;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero-arabic {
                font-size: 1.5rem;
            }
            
            .section-title .english {
                font-size: 2rem;
            }
            
            .brand-logo-item {
                min-width: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
    <img src="logo.png.jpg" alt="Fastest Car Garage Logo" style="height: 60px; margin-right: 15px;">
    <div class="logo-text">
        <div class="logo-main">FASTEST CAR GARAGE</div>
        <div class="logo-arabic">أسرع كراج للسيارات</div>
        <div class="tagline">Fast & Reliable - Affordable</div>
    </div>
</div>
            
            <div class="lang-toggle">
                <button class="lang-btn active" id="enBtn">EN</button>
                <button class="lang-btn" id="arBtn">AR</button>
            </div>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">
                        <span class="english">Home</span>
                        <span class="arabic-nav">الرئيسية</span>
                    </a></li>
                    <li><a href="#services">
                        <span class="english">Services</span>
                        <span class="arabic-nav">الخدمات</span>
                    </a></li>
                    <li><a href="#about">
                        <span class="english">About</span>
                        <span class="arabic-nav">من نحن</span>
                    </a></li>
                    <li><a href="#hours">
                        <span class="english">Hours</span>
                        <span class="arabic-nav">المواعيد</span>
                    </a></li>
                    <li><a href="#contact">
                        <span class="english">Contact</span>
                        <span class="arabic-nav">اتصل بنا</span>
                    </a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>FASTEST CAR <span>GARAGE</span></h1>
            <div class="hero-subtitle">Fast & Reliable - Affordable</div>
            <div class="hero-arabic">أسرع كراج للسيارات</div>
            <p class="hero-tagline">Professional automotive repair and maintenance services in Thumama, Qatar. We specialize in quick, reliable, and affordable solutions for all your vehicle needs.</p>
            <div class="cta-buttons">
                <a href="tel:+97466680412" class="btn btn-primary">
                    <i class="fas fa-phone-alt"></i> CALL NOW: +974 6668 0412
                </a>
                <a href="#services" class="btn btn-secondary">
                    <i class="fas fa-tools"></i> OUR SERVICES
                </a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services section" id="services">
        <div class="container">
            <div class="section-title">
                <div class="english">Our Services</div>
                <div class="arabic">خدماتنا</div>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-oil-can"></i>
                    </div>
                    <div class="service-content">
                        <h3>Oil Change & Maintenance</h3>
                        <p>Professional oil change services using premium quality oils and filters to keep your engine running smoothly.</p>
                        <div class="bilingual">
                            <div class="arabic">تغيير الزيت والصيانة</div>
                        </div>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <div class="service-content">
                        <h3>Brake System Repair</h3>
                        <p>Complete brake inspection, pad replacement, rotor resurfacing, and brake fluid flush services.</p>
                        <div class="bilingual">
                            <div class="arabic">إصلاح نظام الفرامل</div>
                        </div>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-engine"></i>
                    </div>
                    <div class="service-content">
                        <h3>Engine Diagnostics & Repair</h3>
                        <p>Advanced engine diagnostics and repair services for all vehicle makes and models.</p>
                        <div class="bilingual">
                            <div class="arabic">تشخيص وإصلاح المحرك</div>
                        </div>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tire"></i>
                    </div>
                    <div class="service-content">
                        <h3>Tire Services</h3>
                        <p>Tire rotation, balancing, alignment, and replacement services with premium quality tires.</p>
                        <div class="bilingual">
                            <div class="arabic">خدمات الإطارات</div>
                        </div>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-car-battery"></i>
                    </div>
                    <div class="service-content">
                        <h3>Battery & Electrical</h3>
                        <p>Battery testing, replacement, alternator repairs, and complete electrical system diagnostics.</p>
                        <div class="bilingual">
                            <div class="arabic">البطارية والكهرباء</div>
                        </div>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-wind"></i>
                    </div>
                    <div class="service-content">
                        <h3>AC & Heating Services</h3>
                        <p>Professional AC repair, recharging, heater core replacement, and climate control system services.</p>
                        <div class="bilingual">
                            <div class="arabic">خدمات التكييف والتدفئة</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about section" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>About Fastest Car Garage</h2>
                    <div class="about-arabic">من نحن - أسرع كراج للسيارات</div>
                    <p>We are a professional automotive service center located in Thumama, Qatar, specializing in fast, reliable, and affordable vehicle repairs and maintenance.</p>
                    <p>With years of experience and certified technicians, we provide top-quality services for all types of vehicles, from regular maintenance to complex repairs.</p>
                    
                    <div class="about-features">
                        <div class="feature">
                            <i class="fas fa-clock"></i>
                            <div class="bilingual">
                                <div class="english">Fast Service</div>
                                <div class="arabic">خدمة سريعة</div>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-shield-alt"></i>
                            <div class="bilingual">
                                <div class="english">Reliable Work</div>
                                <div class="arabic">عمل موثوق</div>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-tag"></i>
                            <div class="bilingual">
                                <div class="english">Affordable Prices</div>
                                <div class="arabic">أسعار معقولة</div>
                            </div>
                        </div>
                        <div class="feature">
                            <i class="fas fa-user-tie"></i>
                            <div class="bilingual">
                                <div class="english">Professional Team</div>
                                <div class="arabic">فريق محترف</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="info-card">
                    <h3>Why Choose Us?</h3>
                    <div class="contact-info">
                        <p><i class="fas fa-check-circle"></i> Certified Technicians</p>
                        <p><i class="fas fa-check-circle"></i> Quality Parts & Materials</p>
                        <p><i class="fas fa-check-circle"></i> Latest Diagnostic Equipment</p>
                        <p><i class="fas fa-check-circle"></i> Warranty on Services</p>
                        <p><i class="fas fa-check-circle"></i> Emergency Roadside Assistance</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Hours & Contact -->
    <section class="info-section section" id="hours">
        <div class="container">
            <div class="section-title">
                <div class="english">Working Hours & Contact</div>
                <div class="arabic">ساعات العمل والاتصال</div>
            </div>
            
            <div class="info-grid">
                <div class="info-card">
                    <h3>Business Hours</h3>
                    <ul class="hours-list">
                        <li><span>Saturday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span>Sunday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span>Monday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span>Tuesday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span>Wednesday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span>Thursday</span><span>8:00 AM - 8:00 PM</span></li>
                        <li><span class="closed">Friday</span><span class="closed">Closed</span></li>
                    </ul>
                </div>
                
                <div class="info-card" id="contact">
                    <h3>Contact Information</h3>
                    <div class="contact-info">
                        <p>
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Location: <strong>Thumama, Doha, Qatar</strong></span>
                        </p>
                        <p>
                            <i class="fas fa-phone-alt"></i>
                            <span>Phone: <a href="tel:+97466680412"><strong>+974 6668 0412</strong></a></span>
                        </p>
                        <p>
                            <i class="fas fa-clock"></i>
                            <span>Open: <strong>8:00 AM - 8:00 PM</strong></span>
                        </p>
                        <p>
                            <i class="fas fa-calendar-times"></i>
                            <span>Closed: <strong>Friday</strong></span>
                        </p>
                    </div>
                    <a href="tel:+97466680412" class="btn btn-primary" style="margin-top: 20px; display: inline-block; width: 100%; text-align: center;">
                        <i class="fas fa-phone-alt"></i> CALL FOR APPOINTMENT
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Branding Section -->
    <section class="branding section">
        <div class="container">
            <h2 class="branding-title">FULL BRAND IDENTITY</h2>
            <p class="branding-subtitle">Professional brand identity and logo integration for a luxury mechanic garage. Ready for website, marketing, and social media.</p>
            
            <div class="brand-logos">
                <div class="brand-logo-item">
                    <div class="brand-logo-text">FASTEST CAR</div>
                    <div class="brand-logo-arabic">أسرع سيارة</div>
                </div>
                <div class="brand-logo-item">
                    <div class="brand-logo-text">FASTEST CAR GARAGE</div>
                    <div class="brand-logo-arabic">أسرع كراج للسيارات</div>
                </div>
                <div class="brand-logo-item">
                    <div class="brand-logo-text">FAST & RELIABLE</div>
                    <div class="brand-logo-arabic">سريع وموثوق</div>
                </div>
            </div>
            
            <div class="section-title">
                <div class="english">Social Media Ready</div>
                <div class="arabic">جاهز لوسائل التواصل الاجتماعي</div>
            </div>
            
            <div class="social-icons">
                <a href="#" class="social-icon"><i class="fab fa-whatsapp"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-tiktok"></i></a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>FASTEST CAR GARAGE</h3>
                    <p>أسرع كراج للسيارات</p>
                    <p>Professional automotive repair and maintenance services in Thumama, Qatar. Fast, reliable, and affordable solutions for all vehicle needs.</p>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home"><i class="fas fa-chevron-right"></i> Home / الرئيسية</a></li>
                        <li><a href="#services"><i class="fas fa-chevron-right"></i> Services / الخدمات</a></li>
                        <li><a href="#about"><i class="fas fa-chevron-right"></i> About / من نحن</a></li>
                        <li><a href="#contact"><i class="fas fa-chevron-right"></i> Contact / اتصل بنا</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <ul>
                        <li><a href="https://maps.google.com/?q=Thumama,Doha,Qatar" target="_blank">
                            <i class="fas fa-map-marker-alt"></i> Thumama, Doha, Qatar
                        </a></li>
                        <li><a href="tel:+97466680412">
                            <i class="fas fa-phone-alt"></i> +974 6668 0412
                        </a></li>
                        <li><a href="#">
                            <i class="fas fa-clock"></i> Sat-Thu: 8:00 AM - 8:00 PM
                        </a></li>
                        <li><a href="#">
                            <i class="fas fa-calendar-times"></i> Friday: Closed
                        </a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 FASTEST CAR GARAGE. أسرع كراج للسيارات. All rights reserved.</p>
                <p>Thumama, Doha, Qatar | Phone: +974 6668 0412</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            navMenu.classList.toggle('active');
            const icon = mobileMenuBtn.querySelector('i');
            if (icon.classList.contains('fa-bars')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });
        
        // Language Toggle
        const enBtn = document.getElementById('enBtn');
        const arBtn = document.getElementById('arBtn');
        
        enBtn.addEventListener('click', () => {
            enBtn.classList.add('active');
            arBtn.classList.remove('active');
            document.documentElement.dir = 'ltr';
            document.documentElement.lang = 'en';
        });
        
        arBtn.addEventListener('click', () => {
            arBtn.classList.add('active');
            enBtn.classList.remove('active');
            document.documentElement.dir = 'rtl';
            document.documentElement.lang = 'ar';
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    // Close mobile menu if open
                    navMenu.classList.remove('active');
                    mobileMenuBtn.querySelector('i').classList.remove('fa-times');
                    mobileMenuBtn.querySelector('i').classList.add('fa-bars');
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.padding = '15px 0';
                header.style.boxShadow = '0 5px 20px rgba(0,0,0,0.3)';
            } else {
                header.style.padding = '20px 0';
                header.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>
