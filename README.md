<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB International University | The Future of Higher Education</title>
    <meta name="description" content="World-class education with innovative programs at EYECAB International University">
    <meta property="og:title" content="EYECAB International University">
    <meta property="og:image" content="https://example.com/uni-social-preview.jpg">
    
    <!-- Preload Optimizations -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="preload" href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" as="style">
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" as="style">
    <link rel="preload" href="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=initMap" as="script">
    <link rel="preload" href="https://cdn.jsdelivr.net/npm/panolens@0.11.0/build/panolens.min.js" as="script">
    
    <!-- Fonts and Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <style>
        :root {
            --primary: #0A2463;
            --secondary: #3E92CC;
            --accent: #FFD700;
            --light: #FFF9F0;
            --dark: #1A1A1A;
            --success: #28a745;
            --info: #17a2b8;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Raleway', sans-serif;
            --accent-rgb: 255, 215, 0;
            --primary-rgb: 10, 36, 99;
            --background: var(--light);
            --text-color: var(--dark);
            --card-bg: white;
            --header-bg: rgba(10, 36, 99, 0.95);
        }
        
        /* Dark Mode Variables */
        .dark-theme {
            --bg-dark: #121212;
            --text-dark: #f0f0f0;
            --card-dark: #1e1e1e;
            
            --background: var(--bg-dark);
            --text-color: var(--text-dark);
            --card-bg: var(--card-dark);
            --header-bg: rgba(30, 30, 30, 0.9);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-body);
            line-height: 1.8;
            color: var(--text-color);
            background-color: var(--background);
            overflow-x: hidden;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        
        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: var(--header-bg);
            color: white;
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(8px);
        }
        
        header.scrolled {
            padding: 1rem 0;
            background-color: rgba(var(--primary-rgb), 0.98);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-right: 15px;
        }
        
        .logo-text {
            font-family: var(--font-heading);
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            font-weight: 700;
            line-height: 1.2;
            color: white;
        }
        
        .logo-text p {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
            position: relative;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            position: relative;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        nav ul li a.active {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Theme Toggle */
        .theme-toggle {
            position: relative;
            width: 60px;
            height: 30px;
            border-radius: 30px;
            background: var(--card-bg);
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            padding: 0 5px;
            margin-left: 15px;
        }
        
        .theme-toggle i {
            font-size: 14px;
            padding: 0 5px;
            color: var(--text-color);
        }
        
        .toggle-ball {
            position: absolute;
            left: 5px;
            width: 22px;
            height: 22px;
            background: var(--accent);
            border-radius: 50%;
            transition: transform 0.3s ease;
        }
        
        .dark-theme .toggle-ball {
            transform: translateX(30px);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 800px;
            background: linear-gradient(rgba(10, 36, 99, 0.7), rgba(10, 36, 99, 0.7)), 
                        url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s forwards;
            opacity: 0;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            animation: fadeInUp 1s ease 0.4s forwards;
            opacity: 0;
        }
        
        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            letter-spacing: 1px;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--primary);
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.4);
        }
        
        .btn-outline {
            border: 2px solid white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .btn-accent {
            background-color: var(--accent);
            color: var(--primary);
            font-weight: 600;
        }
        
        .btn-accent:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.3);
        }
        
        /* About Section */
        .section {
            padding: 8rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
        }
        
        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            margin-bottom: 1.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent);
        }
        
        .section-title p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .about-features {
            margin-top: 2rem;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .feature-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            margin-top: 0.3rem;
        }
        
        .feature-text h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(10, 36, 99, 0.2);
            transform: rotate(-2deg);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(10, 36, 99, 0.2), rgba(62, 146, 204, 0.2));
            z-index: 1;
        }
        
        /* Schools Section with Program Filter */
        .schools {
            background-color: var(--card-bg);
        }
        
        .program-filter {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }
        
        .filter-btn {
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--text-color);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .filter-btn.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        .filter-btn:hover:not(.active) {
            background: rgba(var(--accent-rgb), 0.1);
        }
        
        .schools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .school-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(var(--primary-rgb), 0.1);
        }
        
        .school-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .school-card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .school-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .school-card:hover .school-card-img img {
            transform: scale(1.1);
        }
        
        .school-card-content {
            padding: 2rem;
        }
        
        .program-badge {
            display: inline-block;
            padding: 3px 10px;
            background: var(--accent);
            color: var(--primary);
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .school-card-content h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .school-card-content p {
            margin-bottom: 1.5rem;
            color: var(--text-color);
            opacity: 0.8;
        }
        
        .school-card-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .school-card-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }
        
        .school-card-link:hover {
            color: var(--primary);
        }
        
        .school-card-link:hover i {
            transform: translateX(5px);
        }
        
        /* Stats Section */
        .stats {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 6rem 0;
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .stat-item {
            padding: 2rem;
        }
        
        .stat-number {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .stat-label {
            font-size: 1.2rem;
            letter-spacing: 1px;
            opacity: 0.9;
        }
        
        /* Testimonials */
        .testimonials {
            position: relative;
            padding: 8rem 0;
            background-color: var(--background);
        }
        
        .testimonial-slider {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            margin: 0 1rem;
        }
        
        .testimonial-quote {
            font-size: 1.2rem;
            font-style: italic;
            color: var(--text-color);
            margin-bottom: 2rem;
            line-height: 1.8;
            position: relative;
        }
        
        .testimonial-quote::before,
        .testimonial-quote::after {
            content: '"';
            font-size: 3rem;
            color: var(--accent);
            opacity: 0.3;
            position: absolute;
        }
        
        .testimonial-quote::before {
            top: -20px;
            left: -15px;
        }
        
        .testimonial-quote::after {
            bottom: -40px;
            right: -15px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .testimonial-author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .testimonial-author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .testimonial-author-info h4 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 0.3rem;
        }
        
        .testimonial-author-info p {
            color: var(--text-color);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Virtual Tour Section */
        .virtual-tour {
            background-color: var(--card-bg);
        }
        
        .tour-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .panorama-view {
            width: 100%;
            height: 500px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
            background-color: #eee;
        }
        
        .tour-hotspots {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .hotspot {
            background: var(--card-bg);
            border: 2px solid var(--accent);
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            color: var(--text-color);
            font-weight: 600;
        }
        
        .hotspot.active {
            background: var(--accent);
            color: var(--primary);
        }
        
        /* Tuition Calculator */
        .calculator {
            background-color: var(--background);
        }
        
        .calculator-card {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            background: var(--card-bg);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .calculator-form {
            display: grid;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-group select {
            padding: 12px 15px;
            border-radius: 8px;
            border: 1px solid rgba(var(--primary-rgb), 0.2);
            background-color: var(--card-bg);
            color: var(--text-color);
            font-family: var(--font-body);
        }
        
        .calculator-results {
            background: rgba(var(--accent-rgb), 0.1);
            padding: 25px;
            border-radius: 10px;
            align-self: center;
        }
        
        .result-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            color: var(--text-color);
        }
        
        .result-item.total {
            font-weight: bold;
            font-size: 1.2rem;
            padding-top: 10px;
            border-top: 1px solid rgba(var(--primary-rgb), 0.1);
        }
        
        .financial-aid-note {
            margin-top: 20px;
            font-size: 0.9rem;
            opacity: 0.8;
            color: var(--text-color);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        /* Campus Map Section */
        .map-section {
            background-color: var(--card-bg);
        }
        
        #campusesMap {
            height: 500px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .map-locations {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .location-card {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border: 1px solid rgba(var(--primary-rgb), 0.1);
        }
        
        .location-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .location-card h4 {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .location-card h4 i {
            color: var(--accent);
        }
        
        .location-card p {
            color: var(--text-color);
            opacity: 0.8;
        }
        
        /* CTA Section */
        .cta {
            background: linear-gradient(rgba(10, 36, 99, 0.9), rgba(10, 36, 99, 0.9)), 
                        url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 8rem 0;
        }
        
        .cta h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            margin-bottom: 2rem;
        }
        
        .cta p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 5rem 0 2rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-col h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
        }
        
        .footer-col p {
            margin-bottom: 1rem;
            opacity: 0.8;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: all 0.3s ease;
        }
        
        .footer-links a:hover {
            opacity: 1;
            color: var(--accent);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--accent);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .contact-form {
            display: grid;
            gap: 15px;
        }
        
        .contact-form input,
        .contact-form select,
        .contact-form textarea {
            padding: 12px 15px;
            border-radius: 8px;
            border: none;
            background-color: rgba(255,255,255,0.1);
            color: white;
            font-family: var(--font-body);
        }
        
        .contact-form textarea {
            resize: vertical;
            min-height: 100px;
        }
        
        .contact-form button {
            margin-top: 10px;
            position: relative;
        }
        
        .loading-icon {
            display: none;
            margin-left: 10px;
        }
        
        .success-message {
            background: rgba(40, 167, 69, 0.1);
            padding: 15px;
            border-radius: 5px;
            margin-top: 15px;
            color: var(--success);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive Styles */
        @media (max-width: 1200px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .about-image {
                max-width: 600px;
                margin: 0 auto;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero p {
                font-size: 1.3rem;
            }
            
            .section-title h2 {
                font-size: 2.5rem;
            }
            
            .calculator-card {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 80%;
                height: calc(100vh - 80px);
                background-color: var(--primary);
                transition: all 0.3s ease;
                z-index: 999;
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
                padding: 2rem;
            }
            
            nav ul li {
                margin: 1rem 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-btns {
                flex-direction: column;
                gap: 1rem;
            }
            
            .btn {
                width: 100%;
            }
            
            .section {
                padding: 5rem 0;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .cta h2 {
                font-size: 2.2rem;
            }
            
            .panorama-view {
                height: 350px;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .stat-item {
                padding: 1.5rem;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .logo-text h1 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">
                <div class="logo-icon">
                    <i class="fas fa-university"></i>
                </div>
                <div class="logo-text">
                    <h1>EYECAB INTERNATIONAL UNIVERSITY</h1>
                    <p>Redefining Global Education</p>
                </div>
            </a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav id="mainNav">
                <ul>
                    <li><a href="#home" class="active">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#schools">Schools</a></li>
                    <li><a href="#tour">Virtual Tour</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li>
                        <button id="themeToggle" class="theme-toggle">
                            <i class="fas fa-moon"></i>
                            <i class="fas fa-sun"></i>
                            <span class="toggle-ball"></span>
                        </button>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Shape Your Future With World-Class Education</h1>
            <p>Join a vibrant community of innovators and leaders at EYECAB International University</p>
            <div class="hero-btns">
                <a href="#schools" class="btn btn-primary">Explore Programs</a>
                <a href="#contact" class="btn btn-outline">Contact Admissions</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About EYECAB</h2>
                <p>Discover our commitment to excellence in education and research</p>
            </div>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>A New Vision for Higher Education</h3>
                    <p>Founded in 2023, EYECAB International University brings together world-class faculty, cutting-edge research facilities, and an innovative curriculum designed to prepare students for the challenges of tomorrow.</p>
                    <p>Our interdisciplinary approach breaks down traditional academic silos, encouraging collaboration across fields to solve complex global problems.</p>
                    
                    <div class="about-features">
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-globe"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Global Network</h4>
                                <p>Partnerships with 50+ institutions worldwide</p>
                            </div>
                        </div>
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-flask"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Research Excellence</h4>
                                <p>$250M annual research funding</p>
                            </div>
                        </div>
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-user-graduate"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Student Success</h4>
                                <p>94% career placement within 6 months</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="EYECAB Campus">
                </div>
            </div>
        </div>
    </section>

    <!-- Schools Section with Program Filter -->
    <section class="section schools" id="schools">
        <div class="container">
            <div class="section-title">
                <h2>Our Academic Schools</h2>
                <p>Explore our diverse range of accredited programs</p>
            </div>
            
            <!-- Program Filter -->
            <div class="program-filter">
                <button class="filter-btn active" data-filter="all">All Programs</button>
                <button class="filter-btn" data-filter="undergrad">Undergraduate</button>
                <button class="filter-btn" data-filter="masters">Masters</button>
                <button class="filter-btn" data-filter="phd">PhD</button>
                <button class="filter-btn" data-filter="online">Online</button>
            </div>
            
            <div class="schools-grid">
                <div class="school-card" data-category="undergrad online">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173" alt="Technology School">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">Bachelor's</div>
                        <h3>School of Technology</h3>
                        <p>Cutting-edge programs in Computer Science, Artificial Intelligence, Cybersecurity, and Data Science with industry-aligned curriculum.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="school-card" data-category="masters phd">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1532094349884-543bc11b234d" alt="Business School">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">Graduate</div>
                        <h3>Business School</h3>
                        <p>Transform your career with our MBA, Executive Education, and Doctoral programs designed for tomorrow's business leaders.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="school-card" data-category="undergrad masters online">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1575505586569-646b2ca898fc" alt="Health Sciences">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">Undergrad & Masters</div>
                        <h3>Health Sciences</h3>
                        <p>Innovative programs in Medicine, Nursing, Public Health, and Biomedical Engineering with clinical partnerships worldwide.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="school-card" data-category="phd">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1456513080510-7bf3a84b82f8" alt="Advanced Research">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">PhD</div>
                        <h3>Advanced Research Institute</h3>
                        <p>Doctoral programs in emerging fields with access to state-of-the-art labs and global research collaborations.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="school-card" data-category="undergrad online">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1497633762265-9d179a990aa6" alt="Liberal Arts">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">Bachelor's</div>
                        <h3>Liberal Arts</h3>
                        <p>Interdisciplinary programs in Humanities, Social Sciences, and Creative Arts with global study opportunities.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="school-card" data-category="masters online">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1521791055366-0d553872125f" alt="Engineering">
                    </div>
                    <div class="school-card-content">
                        <div class="program-badge">Masters</div>
                        <h3>Engineering</h3>
                        <p>Specialized graduate programs in Robotics, Sustainable Energy, Aerospace, and more with industry co-op options.</p>
                        <a href="#" class="school-card-link">View Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-container">
                <div class="stat-item">
                    <div class="stat-number">150+</div>
                    <div class="stat-label">Degree Programs</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">92%</div>
                    <div class="stat-label">Graduation Rate</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">120</div>
                    <div class="stat-label">Countries Represented</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">1:10</div>
                    <div class="stat-label">Faculty-Student Ratio</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Virtual Tour Section -->
    <section class="section virtual-tour" id="tour">
        <div class="container">
            <div class="section-title">
                <h2>Virtual Campus Tour</h2>
                <p>Explore our facilities from anywhere in the world</p>
            </div>
            
            <div class="tour-container">
                <div class="panorama-view" id="campusPanorama"></div>
                
                <div class="tour-hotspots">
                    <button class="hotspot active" data-view="library">
                        <i class="fas fa-book"></i> Library
                    </button>
                    <button class="hotspot" data-view="labs">
                        <i class="fas fa-flask"></i> Science Labs
                    </button>
                    <button class="hotspot" data-view="sports">
                        <i class="fas fa-running"></i> Sports Complex
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Tuition Calculator -->
    <section class="section calculator">
        <div class="container">
            <div class="section-title">
                <h2>Admissions Calculator</h2>
                <p>Estimate your tuition and scholarship opportunities</p>
            </div>
            
            <div class="calculator-card">
                <div class="calculator-form">
                    <div class="form-group">
                        <label for="programLevel">Program Level</label>
                        <select id="programLevel">
                            <option value="undergrad">Undergraduate</option>
                            <option value="masters">Master's</option>
                            <option value="phd">PhD</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="residency">Residency Status</label>
                        <select id="residency">
                            <option value="domestic">Domestic</option>
                            <option value="international">International</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="scholarship">Scholarship Type</label>
                        <select id="scholarship">
                            <option value="none">None</option>
                            <option value="academic">Academic (20%)</option>
                            <option value="athletic">Athletic (30%)</option>
                            <option value="need-based">Need-Based (40%)</option>
                        </select>
                    </div>
                    
                    <button id="calculateBtn" class="btn btn-accent">
                        Calculate Estimate
                    </button>
                </div>
                
                <div class="calculator-results">
                    <div class="result-item">
                        <span>Base Tuition:</span>
                        <span id="baseTuition">$0</span>
                    </div>
                    <div class="result-item">
                        <span>Scholarship:</span>
                        <span id="scholarshipAmount">-$0</span>
                    </div>
                    <hr>
                    <div class="result-item total">
                        <span>Estimated Annual Cost:</span>
                        <span id="totalCost">$0</span>
                    </div>
                    
                    <div class="financial-aid-note">
                        <i class="fas fa-info-circle"></i> 78% of students receive financial aid
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Campus Map Section -->
    <section class="section map-section">
        <div class="container">
            <div class="section-title">
                <h2>Our Global Campuses</h2>
                <p>Visit us at any of our worldwide locations</p>
            </div>
            
            <div id="campusesMap"></div>
            
            <div class="map-locations">
                <div class="location-card" data-lat="40.7128" data-lng="-74.0060" data-campus="New York">
                    <h4><i class="fas fa-map-marker-alt"></i> New York Campus</h4>
                    <p>123 Education Blvd, NY 10001</p>
                </div>
                
                <div class="location-card" data-lat="51.5074" data-lng="-0.1278" data-campus="London">
                    <h4><i class="fas fa-map-marker-alt"></i> London Campus</h4>
                    <p>456 Innovation Way, London WC1</p>
                </div>
                
                <div class="location-card" data-lat="35.6762" data-lng="139.6503" data-campus="Tokyo">
                    <h4><i class="fas fa-map-marker-alt"></i> Tokyo Campus</h4>
                    <p>789 Future Street, Shinjuku</p>
                </div>
                
                <div class="location-card" data-lat="-33.8688" data-lng="151.2093" data-campus="Sydney">
                    <h4><i class="fas fa-map-marker-alt"></i> Sydney Campus</h4>
                    <p>101 Knowledge Ave, NSW 2000</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="section testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Student Experiences</h2>
                <p>Hear from our global community of learners</p>
            </div>
            
            <div class="testimonial-slider">
                <div class="testimonial-card">
                    <div class="testimonial-quote">
                        EYECAB's interdisciplinary approach allowed me to combine computer science with business studies, giving me a unique edge in the startup world. The faculty's dedication to student success is unparalleled.
                    </div>
                    <div class="testimonial-author">
                        <div class="testimonial-author-img">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Maria Chen">
                        </div>
                        <div class="testimonial-author-info">
                            <h4>Maria Chen</h4>
                            <p>Computer Science & Business, Class of 2022</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="container">
            <h2>Ready to Begin Your Journey?</h2>
            <p>Applications for Fall 2023 are now open. Join our next generation of innovators and leaders.</p>
            <div class="hero-btns">
                <a href="#" class="btn btn-primary">Apply Now</a>
                <a href="#" class="btn btn-outline">Request Information</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h3>About EYECAB</h3>
                    <p>EYECAB International University is a premier institution dedicated to transformative education and research that addresses global challenges.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#">Academic Calendar</a></li>
                        <li><a href="#">Course Catalog</a></li>
                        <li><a href="#">Student Portal</a></li>
                        <li><a href="#">Faculty Directory</a></li>
                        <li><a href="#">Careers at EYECAB</a></li>
                        <li><a href="#">Alumni Network</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Resources</h3>
                    <ul class="footer-links">
                        <li><a href="#">Library</a></li>
                        <li><a href="#">Research Centers</a></li>
                        <li><a href="#">International Students</a></li>
                        <li><a href="#">Disability Services</a></li>
                        <li><a href="#">Campus Safety</a></li>
                        <li><a href="#">IT Support</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Contact Admissions</h3>
                    <form id="admissionForm" class="contact-form">
                        <input type="text" name="name" placeholder="Full Name" required>
                        <input type="email" name="email" placeholder="Email" required>
                        <select name="program" required>
                            <option value="">Select Program</option>
                            <option>Undergraduate</option>
                            <option>Graduate</option>
                            <option>PhD</option>
                        </select>
                        <textarea name="message" placeholder="Your questions..." rows="3"></textarea>
                        <button type="submit" class="btn btn-primary">
                            <span class="btn-text">Submit</span>
                            <i class="fas fa-spinner fa-spin loading-icon"></i>
                        </button>
                    </form>
                    <div id="formResponse"></div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 EYECAB International University. All rights reserved. | <a href="#">Privacy Policy</a> | <a href="#">Accessibility</a></p>
            </div>
        </div>
    </footer>

    <!-- Scripts -->
    <!-- Google Maps API -->
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
    
    <!-- Panorama Viewer -->
    <script src="https://cdn.jsdelivr.net/npm/panolens@0.11.0/build/panolens.min.js"></script>
    
    <!-- Tawk.to Live Chat -->
    <script>
        var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
        (function(){
        var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
        s1.async=true;
        s1.src='https://embed.tawk.to/YOUR_WIDGET_ID/default';
        s1.charset='UTF-8';
        s1.setAttribute('crossorigin','*');
        s0.parentNode.insertBefore(s1,s0);
        })();
    </script>

    <!-- Main JavaScript -->
    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mainNav = document.getElementById('mainNav');
        
        mobileMenuBtn.addEventListener('click', () => {
            mainNav.classList.toggle('active');
            mobileMenuBtn.innerHTML = mainNav.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                if(this.getAttribute('href') === '#') return;
                
                const target = document.querySelector(this.getAttribute('href'));
                if(target) {
                    window.scrollTo({
                        top: target.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if(mainNav.classList.contains('active')) {
                        mainNav.classList.remove('active');
                        mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                }
            });
        });
        
        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if(window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Dark Mode Toggle
        const themeToggle = document.getElementById('themeToggle');
        const prefersDarkScheme = window.matchMedia('(prefers-color-scheme: dark)');
        
        // Check for saved preference or system preference
        const currentTheme = localStorage.getItem('theme') || 
                            (prefersDarkScheme.matches ? 'dark' : 'light');
        if(currentTheme === 'dark') {
            document.body.classList.add('dark-theme');
        }
        
        themeToggle.addEventListener('click', () => {
            document.body.classList.toggle('dark-theme');
            const theme = document.body.classList.contains('dark-theme') ? 'dark' : 'light';
            localStorage.setItem('theme', theme);
        });
        
        // Program Filter
        const filterButtons = document.querySelectorAll('.filter-btn');
        filterButtons.forEach(btn => {
            btn.addEventListener('click', () => {
                filterButtons.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                
                const filter = btn.dataset.filter;
                document.querySelectorAll('.school-card').forEach(card => {
                    card.style.display = (filter === 'all' || card.dataset.category.includes(filter)) 
                        ? 'block' : 'none';
                });
            });
        });
        
        // Google Maps Initialization
        function initMap() {
            const map = new google.maps.Map(document.getElementById("campusesMap"), {
                zoom: 2,
                center: { lat: 20, lng: 0 },
                styles: [
                    {
                        "featureType": "poi",
                        "stylers": [{ "visibility": "off" }]
                    }
                ]
            });

            // Add markers for each campus
            document.querySelectorAll('.location-card').forEach(location => {
                const marker = new google.maps.Marker({
                    position: { 
                        lat: parseFloat(location.dataset.lat), 
                        lng: parseFloat(location.dataset.lng) 
                    },
                    map: map,
                    title: location.dataset.campus
                });
                
                // Click event for location cards
                location.addEventListener('click', () => {
                    map.panTo(marker.getPosition());
                    map.setZoom(15);
                });
            });
        }
        
        // Virtual Tour
        const panoramaViews = {
            library: 'https://i.imgur.com/5G6mYQa.jpg',
            labs: 'https://i.imgur.com/8V7yQzC.jpg',
            sports: 'https://i.imgur.com/3JYQZ7j.jpg'
        };
        
        let viewer;
        function initPanorama(view) {
            if(viewer) viewer.dispose();
            
            viewer = new PANOLENS.Viewer({
                container: document.getElementById('campusPanorama'),
                autoRotate: true,
                autoRotateSpeed: 0.3,
                controlBar: true
            });
            
            const panorama = new PANOLENS.ImagePanorama(panoramaViews[view]);
            viewer.add(panorama);
        }
        
        // Set default view
        document.addEventListener('DOMContentLoaded', () => initPanorama('library'));
        
        // Hotspot controls
        document.querySelectorAll('.hotspot').forEach(btn => {
            btn.addEventListener('click', () => {
                initPanorama(btn.dataset.view);
                document.querySelectorAll('.hotspot').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
            });
        });
        
        // Tuition Calculator
        const tuitionRates = {
            undergrad: { domestic: 28000, international: 45000 },
            masters: { domestic: 35000, international: 52000 },
            phd: { domestic: 25000, international: 40000 }
        };
        
        const scholarshipRates = {
            none: 0,
            academic: 0.2,
            athletic: 0.3,
            'need-based': 0.4
        };
        
        document.getElementById('calculateBtn').addEventListener('click', () => {
            const program = document.getElementById('programLevel').value;
            const residency = document.getElementById('residency').value;
            const scholarship = document.getElementById('scholarship').value;
            
            const base = tuitionRates[program][residency];
            const discount = base * scholarshipRates[scholarship];
            const total = base - discount;
            
            // Animate the results
            animateValue('baseTuition', 0, base, 1000);
            animateValue('scholarshipAmount', 0, discount, 1000);
            animateValue('totalCost', 0, total, 1000);
        });
        
        function animateValue(id, start, end, duration) {
            const obj = document.getElementById(id);
            let startTimestamp = null;
            const step = (timestamp) => {
                if (!startTimestamp) startTimestamp = timestamp;
                const progress = Math.min((timestamp - startTimestamp) / duration, 1);
                const value = Math.floor(progress * (end - start) + start);
                obj.textContent = formatCurrency(value);
                if (progress < 1) window.requestAnimationFrame(step);
            };
            window.requestAnimationFrame(step);
        }
        
        function formatCurrency(value) {
            return '$' + value.toLocaleString();
        }
        
        // Form Submission
        const contactForm = document.getElementById('admissionForm');
        contactForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const submitBtn = contactForm.querySelector('button[type="submit"]');
            submitBtn.disabled = true;
            submitBtn.querySelector('.btn-text').textContent = 'Sending...';
            submitBtn.querySelector('.loading-icon').style.display = 'inline-block';
            
            // Simulate form submission
            await new Promise(resolve => setTimeout(resolve, 1500));
            
            document.getElementById('formResponse').innerHTML = `
                <div class="success-message">
                    <i class="fas fa-check-circle"></i>
                    Thank you! Our admissions team will contact you within 24 hours.
                </div>
            `;
            
            contactForm.reset();
            submitBtn.disabled = false;
            submitBtn.querySelector('.btn-text').textContent = 'Submit';
            submitBtn.querySelector('.loading-icon').style.display = 'none';
        });
        
        // Lazy Loading Images
        const lazyLoad = () => {
            const lazyImages = [].slice.call(document.querySelectorAll("img.lazy"));
            
            if ("IntersectionObserver" in window) {
                let lazyImageObserver = new IntersectionObserver((entries) => {
                    entries.forEach((entry) => {
                        if (entry.isIntersecting) {
                            let lazyImage = entry.target;
                            lazyImage.src = lazyImage.dataset.src;
                            lazyImage.classList.remove("lazy");
                            lazyImageObserver.unobserve(lazyImage);
                        }
                    });
                });

                lazyImages.forEach((lazyImage) => {
                    lazyImageObserver.observe(lazyImage);
                });
            }
        };
        
        document.addEventListener("DOMContentLoaded", lazyLoad);
    </script>
</body>
</html>
