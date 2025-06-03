<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EIU-X | The Future of Global Education</title>
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Satoshi:wght@700;900&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- A-Frame (VR) -->
    <script src="https://aframe.io/releases/1.3.0/aframe.min.js"></script>
    <!-- Three.js (3D) -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <!-- Web3.js (Blockchain) -->
    <script src="https://cdn.jsdelivr.net/npm/web3@1.5.2/dist/web3.min.js"></script>
    <style>
        :root {
            --eiu-navy: #002366;
            --eiu-gold: #FFD700;
            --ai-teal: #00CED1;
            --impact-green: #2E8B57;
            --text-light: #f8f9fa;
            --text-dark: #212529;
            --bg-light: #f5f7fa;
            --card-shadow: 0 8px 30px rgba(0, 35, 102, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--bg-light);
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Satoshi', sans-serif;
            font-weight: 700;
        }

        /* Header with AI Assistant */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 1rem 3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            z-index: 1000;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo img {
            height: 40px;
        }

        .logo-text {
            font-weight: 900;
            font-size: 1.5rem;
            background: linear-gradient(90deg, var(--eiu-navy), var(--ai-teal));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .user-menu {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .ai-assistant-btn {
            background-color: var(--ai-teal);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .ai-assistant-btn:hover {
            transform: scale(1.1);
        }

        /* Main Dashboard Layout */
        .dashboard {
            display: flex;
            min-height: 100vh;
            padding-top: 80px;
        }

        /* AI Navigation Sidebar */
        .sidebar {
            width: 280px;
            background-color: white;
            padding: 2rem 1rem;
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.05);
        }

        .nav-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 0.8rem 1rem;
            border-radius: 8px;
            margin-bottom: 0.5rem;
            cursor: pointer;
            transition: all 0.3s;
        }

        .nav-item:hover {
            background-color: rgba(0, 194, 209, 0.1);
            color: var(--ai-teal);
        }

        .nav-item.active {
            background-color: var(--eiu-navy);
            color: white;
        }

        /* Main Content Area */
        .main-content {
            flex: 1;
            padding: 2rem 3rem;
        }

        .welcome-banner {
            background: linear-gradient(135deg, var(--eiu-navy), var(--ai-teal));
            color: white;
            padding: 2rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .welcome-text h1 {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .impact-score {
            background-color: white;
            color: var(--eiu-navy);
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        /* Course Cards with 3D Effects */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .course-card {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            transform-style: preserve-3d;
        }

        .course-card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 15px 40px rgba(0, 35, 102, 0.15);
        }

        .course-image {
            height: 160px;
            background-size: cover;
            background-position: center;
        }

        .course-details {
            padding: 1.5rem;
        }

        .course-details h3 {
            margin-bottom: 0.5rem;
        }

        .course-meta {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            font-size: 0.9rem;
            color: #666;
        }

        .vr-badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background-color: var(--ai-teal);
            color: white;
            padding: 0.3rem 0.6rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 600;
            cursor: pointer;
        }

        /* AI Mentor Chat Interface */
        .ai-mentor-chat {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 350px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            z-index: 1000;
            transform: translateY(100%);
            opacity: 0;
            transition: all 0.3s;
        }

        .ai-mentor-chat.active {
            transform: translateY(0);
            opacity: 1;
        }

        .chat-header {
            background: linear-gradient(90deg, var(--eiu-navy), var(--ai-teal));
            color: white;
            padding: 1rem;
            border-top-left-radius: 12px;
            border-top-right-radius: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .chat-close {
            background: none;
            border: none;
            color: white;
            cursor: pointer;
        }

        .chat-messages {
            height: 300px;
            padding: 1rem;
            overflow-y: auto;
        }

        .message {
            margin-bottom: 1rem;
            max-width: 80%;
            padding: 0.8rem;
            border-radius: 12px;
        }

        .message.ai {
            align-self: flex-start;
            background-color: #f0f8ff;
            border-radius: 0 12px 12px 12px;
        }

        .message.user {
            align-self: flex-end;
            background-color: var(--eiu-navy);
            color: white;
            border-radius: 12px 0 12px 12px;
        }

        .chat-input {
            display: flex;
            padding: 1rem;
            border-top: 1px solid #eee;
        }

        .chat-input input {
            flex: 1;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
        }

        .chat-send {
            background-color: var(--ai-teal);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            margin-left: 0.5rem;
            cursor: pointer;
        }

        /* VR Classroom */
        .vr-classroom {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 2000;
            display: none;
            justify-content: center;
            align-items: center;
        }

        .vr-container {
            width: 90%;
            height: 90%;
            background-color: #111;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
        }

        .vr-toolbar {
            position: absolute;
            bottom: 1rem;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 1rem;
            z-index: 10;
        }

        .vr-btn {
            background-color: rgba(255, 255, 255, 0.2);
            color: white;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            backdrop-filter: blur(5px);
        }

        /* Blockchain Credential Viewer */
        .credential-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            display: none;
            justify-content: center;
            align-items: center;
        }

        .credential-card {
            width: 600px;
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            position: relative;
        }

        .credential-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .credential-qr {
            width: 150px;
            height: 150px;
            margin: 1rem auto;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Ethics Scanner */
        .ethics-scanner {
            position: fixed;
            bottom: 2rem;
            left: 2rem;
            background-color: var(--impact-green);
            color: white;
            padding: 1rem;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
            z-index: 1000;
        }

        /* Responsive Design */
        @media (max-width: 1200px) {
            .sidebar {
                width: 220px;
            }
        }

        @media (max-width: 992px) {
            .dashboard {
                flex-direction: column;
            }
            .sidebar {
                width: 100%;
                padding: 1rem;
                display: flex;
                overflow-x: auto;
            }
            .nav-item {
                flex-shrink: 0;
            }
        }

        @media (max-width: 768px) {
            .welcome-banner {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }
            .courses-grid {
                grid-template-columns: 1fr;
            }
            .ai-mentor-chat {
                width: 90%;
                right: 5%;
            }
        }
    </style>
</head>
<body>
    <!-- AI-Powered Header -->
    <header>
        <div class="logo">
            <img src="https://via.placeholder.com/40x40?text=EIU" alt="EIU Logo">
            <span class="logo-text">EIU-X</span>
        </div>
        <div class="user-menu">
            <button class="ai-assistant-btn" id="openAiChat">
                <i class="fas fa-robot"></i>
            </button>
            <div class="user-avatar">
                <img src="https://via.placeholder.com/40x40?text=User" alt="User" style="border-radius: 50%;">
            </div>
        </div>
    </header>

    <!-- Ethics Scanner Button -->
    <div class="ethics-scanner" id="ethicsScanner">
        <i class="fas fa-search"></i>
        <span>AI Ethics Scanner</span>
    </div>

    <!-- Split Dashboard -->
    <div class="dashboard">
        <!-- AI Navigation Sidebar -->
        <div class="sidebar">
            <div class="nav-item active">
                <i class="fas fa-home"></i>
                <span>Dashboard</span>
            </div>
            <div class="nav-item">
                <i class="fas fa-graduation-cap"></i>
                <span>My Courses</span>
            </div>
            <div class="nav-item">
                <i class="fas fa-flask"></i>
                <span>Research Labs</span>
            </div>
            <div class="nav-item">
                <i class="fas fa-users"></i>
                <span>Collaboration Hub</span>
            </div>
            <div class="nav-item" id="viewCredentials">
                <i class="fas fa-certificate"></i>
                <span>Blockchain Credentials</span>
            </div>
            <div class="nav-item">
                <i class="fas fa-vr-cardboard"></i>
                <span>VR Classrooms</span>
            </div>
            <div class="nav-item">
                <i class="fas fa-chart-line"></i>
                <span>Impact Analytics</span>
            </div>
        </div>

        <!-- Main Content -->
        <div class="main-content">
            <!-- Personalized Welcome -->
            <div class="welcome-banner">
                <div class="welcome-text">
                    <h1>Welcome back, Alex!</h1>
                    <p>Your AI mentor recommends working on "Climate Resilience Lab" today</p>
                </div>
                <div class="impact-score">
                    <i class="fas fa-bolt"></i>
                    <span>Impact Score: 87/100</span>
                </div>
            </div>

            <!-- AI-Suggested Courses -->
            <h2>Your Learning Pathway</h2>
            <div class="courses-grid">
                <!-- Course 1: AI Ethics -->
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://via.placeholder.com/400x200?text=AI+Ethics');">
                        <div class="vr-badge" onclick="openVrClassroom('ai-ethics')">
                            <i class="fas fa-vr-cardboard"></i> VR Lab
                        </div>
                    </div>
                    <div class="course-details">
                        <h3>AI & Ethics</h3>
                        <p>Explore ethical frameworks for artificial intelligence development.</p>
                        <div class="course-meta">
                            <span><i class="fas fa-chart-bar"></i> 85% Mastery</span>
                            <span><i class="fas fa-users"></i> 12 Collaborators</span>
                        </div>
                        <button class="ethics-scan-btn" data-course="ai-ethics" style="background-color: var(--impact-green); color: white; border: none; padding: 0.5rem 1rem; border-radius: 6px; margin-top: 1rem; width: 100%;">
                            <i class="fas fa-search"></i> Scan for Ethics
                        </button>
                    </div>
                </div>

                <!-- Course 2: Climate Resilience -->
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://via.placeholder.com/400x200?text=Climate+Resilience');"></div>
                    <div class="course-details">
                        <h3>Climate Resilience Lab</h3>
                        <p>Design solutions for carbon-neutral cities with global teams.</p>
                        <div class="course-meta">
                            <span><i class="fas fa-chart-bar"></i> 62% Mastery</span>
                            <span><i class="fas fa-users"></i> 8 Collaborators</span>
                        </div>
                        <button style="background-color: var(--eiu-navy); color: white; border: none; padding: 0.5rem 1rem; border-radius: 6px; margin-top: 1rem; width: 100%;">
                            Join Global Project
                        </button>
                    </div>
                </div>

                <!-- Course 3: Quantum Computing -->
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://via.placeholder.com/400x200?text=Quantum+Computing');">
                        <div class="vr-badge" onclick="openVrClassroom('quantum')">
                            <i class="fas fa-vr-cardboard"></i> VR Lab
                        </div>
                    </div>
                    <div class="course-details">
                        <h3>Quantum Computing</h3>
                        <p>Hands-on with quantum algorithms in our virtual lab.</p>
                        <div class="course-meta">
                            <span><i class="fas fa-chart-bar"></i> 45% Mastery</span>
                            <span><i class="fas fa-users"></i> 5 Collaborators</span>
                        </div>
                        <button style="background-color: var(--ai-teal); color: white; border: none; padding: 0.5rem 1rem; border-radius: 6px; margin-top: 1rem; width: 100%;">
                            Start Lab Session
                        </button>
                    </div>
                </div>
            </div>

            <!-- Industry Challenges -->
            <h2 style="margin-top: 3rem;">Industry Challenges</h2>
            <div class="courses-grid">
                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://via.placeholder.com/400x200?text=Tesla+Challenge');"></div>
                    <div class="course-details">
                        <h3>Tesla: Solar Microgrids</h3>
                        <p>Design affordable solar solutions for emerging markets.</p>
                        <div class="course-meta">
                            <span><i class="fas fa-award"></i> $50K Prize</span>
                            <span><i class="fas fa-user-friends"></i> 3-5 Team</span>
                        </div>
                        <button style="background-color: var(--eiu-gold); color: var(--eiu-navy); border: none; padding: 0.5rem 1rem; border-radius: 6px; margin-top: 1rem; width: 100%; font-weight: 600;">
                            Join Challenge
                        </button>
                    </div>
                </div>

                <div class="course-card">
                    <div class="course-image" style="background-image: url('https://via.placeholder.com/400x200?text=WHO+Challenge');"></div>
                    <div class="course-details">
                        <h3>WHO: Pandemic Response</h3>
                        <p>Develop AI models for early outbreak detection.</p>
                        <div class="course-meta">
                            <span><i class="fas fa-award"></i> $30K Prize</span>
                            <span><i class="fas fa-user-friends"></i> 2-4 Team</span>
                        </div>
                        <button style="background-color: var(--eiu-gold); color: var(--eiu-n
