<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB INTERNATIONAL UNIVERSITY - Redefining Global Higher Education</title>
    <style>
        :root {
            --primary: #003366;
            --secondary: #E31937;
            --accent: #FFD700;
            --light: #F5F5F5;
            --dark: #222222;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 60px;
            margin-right: 15px;
        }
        
        .logo-text h1 {
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .logo-text p {
            font-size: 0.8rem;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--accent);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 51, 102, 0.8), rgba(0, 51, 102, 0.8)), 
                        url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .cta-button:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 1rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--secondary);
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Mission/Vision */
        .mission-vision {
            background-color: var(--primary);
            color: white;
        }
        
        .mv-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }
        
        .mv-box {
            background-color: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 10px;
            transition: all 0.3s ease;
        }
        
        .mv-box:hover {
            transform: translateY(-10px);
            background-color: rgba(255,255,255,0.2);
        }
        
        .mv-box h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        /* Schools Section */
        .schools-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .school-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .school-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .school-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .school-card-content {
            padding: 1.5rem;
        }
        
        .school-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        /* Stats Section */
        .stats {
            background-color: var(--secondary);
            color: white;
            text-align: center;
            padding: 3rem 0;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .stat-box h3 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }
        
        /* Research Section */
        .research-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .research-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Timeline */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 3px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1.5px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border: 3px solid var(--secondary);
            border-radius: 50%;
            top: 15px;
            z-index: 1;
        }
        
        .left {
            left: 0;
        }
        
        .right {
            left: 50%;
        }
        
        .left::after {
            right: -10px;
        }
        
        .right::after {
            left: -10px;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Comparison Table */
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
        }
        
        .comparison-table th, .comparison-table td {
            padding: 1rem;
            text-align: left;
            border: 1px solid #ddd;
        }
        
        .comparison-table th {
            background-color: var(--primary);
            color: white;
        }
        
        .comparison-table tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-column ul li a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            background-color: rgba(255,255,255,0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content, 
            .research-container,
            .mv-container {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 21px;
            }
            
            .left::after, .right::after {
                left: 21px;
            }
            
            .right {
                left: 0%;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
            }
            
            nav {
                margin-top: 1rem;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
            
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
        }
        
        @media (max-width: 576px) {
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="https://via.placeholder.com/60x60?text=EIU" alt="EIU Logo">
                <div class="logo-text">
                    <h1>EYECAB INTERNATIONAL UNIVERSITY</h1>
                    <p>Redefining Global Higher Education</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#academics">Academics</a></li>
                    <li><a href="#research">Research</a></li>
                    <li><a href="#admissions">Admissions</a></li>
                    <li><a href="#campus">Campus</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>The Harvard of the 21st Century</h2>
            <p>A world-class institution combining Ivy League rigor with cutting-edge interdisciplinary learning and global impact.</p>
            <a href="#admissions" class="cta-button">Apply Now</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About EIU</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Redefining Global Higher Education</h3>
                    <p>EYECAB INTERNATIONAL UNIVERSITY (EIU) is a visionary institution founded in 2024 with the ambitious goal of becoming a top-50 global university within 25 years. Inspired by Harvard's excellence but designed for the modern world, EIU combines academic rigor with innovative approaches to learning and research.</p>
                    <p>Our $500M initial funding supports the creation of a world-class campus, recruitment of top faculty, and generous scholarships to attract the brightest minds from around the world, particularly from underserved regions.</p>
                    <p>EIU focuses on solving real-world challenges through interdisciplinary research in AI ethics, climate resilience, global health, and other critical areas that will shape our future.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Students collaborating">
                </div>
            </div>
        </div>
    </section>

    <!-- Mission/Vision Section -->
    <section class="mission-vision">
        <div class="container">
            <div class="mv-container">
                <div class="mv-box">
                    <h3>Our Vision</h3>
                    <p>"To redefine global higher education by fostering innovation, leadership, and societal impact."</p>
                </div>
                <div class="mv-box">
                    <h3>Our Mission</h3>
                    <p>"To educate and empower future leaders through transformative research, interdisciplinary learning, and ethical problem-solving."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Core Values Section -->
    <section class="core-values">
        <div class="container">
            <div class="section-title">
                <h2>Our Core Values</h2>
            </div>
            <div class="values-container" style="display: grid; grid-template-columns: repeat(4, 1fr); gap: 2rem; text-align: center;">
                <div class="value-box">
                    <i class="fas fa-medal" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
                    <h3>Excellence</h3>
                    <p>Uncompromising academic rigor in all our programs</p>
                </div>
                <div class="value-box">
                    <i class="fas fa-lightbulb" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
                    <h3>Innovation</h3>
                    <p>Encouraging bold, disruptive ideas that change the world</p>
                </div>
                <div class="value-box">
                    <i class="fas fa-globe" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
                    <h3>Inclusivity</h3>
                    <p>Need-blind admissions & commitment to global diversity</p>
                </div>
                <div class="value-box">
                    <i class="fas fa-hand-holding-heart" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
                    <h3>Impact</h3>
                    <p>Research that changes lives and solves real problems</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container stats-container">
            <div class="stat-box">
                <h3>30,000+</h3>
                <p>Students by Year 5</p>
            </div>
            <div class="stat-box">
                <h3>50%</h3>
                <p>International Students</p>
            </div>
            <div class="stat-box">
                <h3>$200M</h3>
                <p>Research Funding Target</p>
            </div>
            <div class="stat-box">
                <h3>30%</h3>
                <p>Scholarship Recipients</p>
            </div>
        </div>
    </section>

    <!-- Academics Section -->
    <section id="academics" class="academics">
        <div class="container">
            <div class="section-title">
                <h2>Academic Programs</h2>
            </div>
            <div class="schools-container">
                <div class="school-card">
                    <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Business School">
                    <div class="school-card-content">
                        <h3>EIU Business School</h3>
                        <p>Developing ethical leaders for the digital economy with cutting-edge programs in entrepreneurship, fintech, and sustainable business.</p>
                    </div>
                </div>
                <div class="school-card">
                    <img src="https://images.unsplash.com/photo-1576091160550-2173dba999ef?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Medical School">
                    <div class="school-card-content">
                        <h3>EIU Medical School</h3>
                        <p>Pioneering approaches to global health with emphasis on AI in medicine, pandemic preparedness, and hea
