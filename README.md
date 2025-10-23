<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reagan Omondi | AI-Enhanced Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles */
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #f9fafb;
            --dark: #111827;
            --light: #f3f4f6;
            --gray: #6b7280;
            --light-gray: #e5e7eb;
            --ai-blue: #6366f1;
            --ai-purple: #8b5cf6;
            --transition: all 0.3s ease;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            --ai-gradient: linear-gradient(135deg, var(--ai-blue), var(--ai-purple));
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: #fff;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        img {
            max-width: 100%;
            display: block;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }
        
        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            background: var(--primary);
            color: white;
            border-radius: 0.5rem;
            font-weight: 600;
            transition: var(--transition);
            border: 2px solid var(--primary);
            cursor: pointer;
        }
        
        .btn:hover {
            background: transparent;
            color: var(--primary);
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background: transparent;
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }
        
        .btn-ai {
            background: var(--ai-gradient);
            border: 2px solid transparent;
            color: white;
        }
        
        .btn-ai:hover {
            background: transparent;
            color: var(--ai-blue);
            border: 2px solid var(--ai-blue);
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: var(--shadow);
            backdrop-filter: blur(10px);
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.25rem 0;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            font-weight: 600;
            position: relative;
            padding: 0.5rem 0;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding: 10rem 0 5rem;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(37, 99, 235, 0.1) 0%, transparent 70%);
            z-index: 0;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .hero-text {
            flex: 1;
        }
        
        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero-text p {
            font-size: 1.25rem;
            color: var(--gray);
            margin-bottom: 2rem;
        }
        
        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: var(--shadow-lg);
        }
        
        .hero-btns {
            display: flex;
            gap: 1rem;
        }
        
        /* AI Features Banner */
        .ai-banner {
            background: var(--ai-gradient);
            color: white;
            padding: 1.5rem;
            border-radius: 1rem;
            margin-top: 2rem;
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }
        
        .ai-icon {
            font-size: 2.5rem;
            background: rgba(255, 255, 255, 0.2);
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .ai-banner-content h3 {
            margin-bottom: 0.5rem;
        }
        
        /* About Section */
        .about-content {
            display: flex;
            gap: 3rem;
            align-items: center;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            color: var(--gray);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .skill {
            background: var(--light);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        .about-image {
            flex: 1;
            border-radius: 1rem;
            overflow: hidden;
            box-shadow: var(--shadow-lg);
        }
        
        /* Portfolio Section */
        .portfolio {
            background-color: var(--secondary);
        }
        
        .portfolio-controls {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .portfolio-filters {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }
        
        .filter-btn {
            padding: 0.5rem 1.5rem;
            background: white;
            border: 1px solid var(--light-gray);
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }
        
        .ai-controls {
            display: flex;
            gap: 1rem;
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .portfolio-item {
            background: white;
            border-radius: 1rem;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }
        
        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }
        
        .portfolio-img {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }
        
        .portfolio-info {
            padding: 1.5rem;
        }
        
        .portfolio-info h3 {
            margin-bottom: 0.5rem;
        }
        
        .portfolio-info p {
            color: var(--gray);
            margin-bottom: 1rem;
        }
        
        .portfolio-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .tag {
            background: var(--light);
            padding: 0.25rem 0.75rem;
            border-radius: 50px;
            font-size: 0.8rem;
        }
        
        .ai-badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: var(--ai-gradient);
            color: white;
            padding: 0.25rem 0.75rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
        }
        
        /* AI Assistant */
        .ai-assistant {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            z-index: 100;
        }
        
        .ai-toggle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--ai-gradient);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: var(--shadow-lg);
            transition: var(--transition);
        }
        
        .ai-toggle:hover {
            transform: scale(1.1);
        }
        
        .ai-chat {
            position: absolute;
            bottom: 80px;
            right: 0;
            width: 350px;
            background: white;
            border-radius: 1rem;
            box-shadow: var(--shadow-lg);
            display: none;
            flex-direction: column;
            overflow: hidden;
        }
        
        .ai-chat.active {
            display: flex;
        }
        
        .ai-header {
            padding: 1rem;
            background: var(--ai-gradient);
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .ai-messages {
            padding: 1rem;
            height: 300px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
        
        .message {
            max-width: 80%;
            padding: 0.75rem 1rem;
            border-radius: 1rem;
            line-height: 1.4;
        }
        
        .ai-message {
            background: var(--light);
            align-self: flex-start;
            border-bottom-left-radius: 0;
        }
        
        .user-message {
            background: var(--primary);
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 0;
        }
        
        .ai-input {
            display: flex;
            padding: 0.75rem;
            border-top: 1px solid var(--light-gray);
        }
        
        .ai-input input {
            flex: 1;
            padding: 0.75rem;
            border: 1px solid var(--light-gray);
            border-radius: 0.5rem;
            margin-right: 0.5rem;
        }
        
        .ai-input button {
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 0.5rem;
            padding: 0.75rem 1rem;
            cursor: pointer;
        }
        
        /* Contact Section */
        .contact-container {
            display: flex;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-details {
            margin-bottom: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
            color: var(--primary);
            font-size: 1.25rem;
        }
        
        .contact-form {
            flex: 1;
            background: white;
            padding: 2rem;
            border-radius: 1rem;
            box-shadow: var(--shadow);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .form-control {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 1px solid var(--light-gray);
            border-radius: 0.5rem;
            font-family: inherit;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .social-links {
            display: flex;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
        
        .social-link:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content, .about-content, .contact-container {
                flex-direction: column;
            }
            
            .hero-image, .about-image {
                order: -1;
                margin-bottom: 2rem;
            }
            
            .hero-text h1 {
                font-size: 2.8rem;
            }
            
            .ai-banner {
                flex-direction: column;
                text-align: center;
            }
        }
        
        @media (max-width: 768px) {
            .hamburger {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                flex-direction: column;
                background: white;
                width: 100%;
                text-align: center;
                padding: 2rem 0;
                box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
                transition: var(--transition);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 1.5rem 0;
            }
            
            .hero {
                padding: 8rem 0 4rem;
            }
            
            .hero-text h1 {
                font-size: 2.3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .portfolio-controls {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .ai-controls {
                width: 100%;
                justify-content: center;
            }
        }
        
        @media (max-width: 480px) {
            .hero-btns {
                flex-direction: column;
            }
            
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
            
            .ai-chat {
                width: 300px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">REAGAN OMONDI</a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Hi, I'm Reagan Omondi<br>Creative Designer & Developer</h1>
                    <p>I create beautiful, functional, and user-centered digital experiences that solve real-world problems.</p>
                    <div class="hero-btns">
                        <a href="#portfolio" class="btn">View My Work</a>
                        <a href="#contact" class="btn btn-outline">Contact Me</a>
                    </div>
                    
                    <div class="ai-banner">
                        <div class="ai-icon">
                            <i class="fas fa-brain"></i>
                        </div>
                        <div class="ai-banner-content">
                            <h3>AI-Powered Portfolio</h3>
                            <p>My portfolio uses AI to analyze your interests and recommend relevant projects. Try the AI Assistant!</p>
                        </div>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="Img.webp" alt="Reagan Omondi" class="profile-img">
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>I design and develop experiences that make people's lives simpler.</h3>
                    <p>With over 5 years of experience in UI/UX design and front-end development, I specialize in creating intuitive digital products that delight users and drive business results.</p>
                    <p>My approach combines user-centered design principles with modern development practices to deliver solutions that are both beautiful and functional.</p>
                    
                    <div class="skills">
                        <span class="skill">UI/UX Design</span>
                        <span class="skill">Frontend Development</span>
                        <span class="skill">React</span>
                        <span class="skill">Figma</span>
                        <span class="skill">Responsive Design</span>
                        <span class="skill">User Research</span>
                        <span class="skill">AI Integration</span>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Working on design">
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>My Portfolio</h2>
            </div>
            <div class="portfolio-controls">
                <div class="portfolio-filters">
                    <button class="filter-btn active" data-filter="all">All</button>
                    <button class="filter-btn" data-filter="web">Web Design</button>
                    <button class="filter-btn" data-filter="mobile">Mobile Apps</button>
                    <button class="filter-btn" data-filter="branding">Branding</button>
                </div>
                <div class="ai-controls">
                    <button id="aiRecommend" class="btn btn-ai">AI Recommendations</button>
                    <button id="aiDescribe" class="btn btn-ai">AI Descriptions</button>
                </div>
            </div>
            <div class="portfolio-grid">
                <!-- Project 1 -->
                <div class="portfolio-item" data-category="web">
                    <div class="ai-badge">AI Enhanced</div>
                    <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80" alt="E-commerce Website" class="portfolio-img">
                    <div class="portfolio-info">
                        <h3>E-commerce Platform</h3>
                        <p id="desc1">A complete shopping experience with seamless checkout and inventory management.</p>
                        <div class="portfolio-tags">
                            <span class="tag">Web Design</span>
                            <span class="tag">React</span>
                            <span class="tag">UI/UX</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="portfolio-item" data-category="mobile">
                    <div class="ai-badge">AI Enhanced</div>
                    <img src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Fitness App" class="portfolio-img">
                    <div class="portfolio-info">
                        <h3>Fitness Tracker App</h3>
                        <p id="desc2">Mobile application for tracking workouts, nutrition, and progress over time.</p>
                        <div class="portfolio-tags">
                            <span class="tag">Mobile App</span>
                            <span class="tag">iOS</span>
                            <span class="tag">UI Design</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="portfolio-item" data-category="branding">
                    <div class="ai-badge">AI Enhanced</div>
                    <img src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80" alt="Brand Identity" class="portfolio-img">
                    <div class="portfolio-info">
                        <h3>Brand Identity</h3>
                        <p id="desc3">Complete brand identity for a sustainable fashion startup.</p>
                        <div class="portfolio-tags">
                            <span class="tag">Branding</span>
                            <span class="tag">Logo Design</span>
                            <span class="tag">Visual Identity</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 4 -->
                <div class="portfolio-item" data-category="web">
                    <div class="ai-badge">AI Enhanced</div>
                    <img src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Dashboard UI" class="portfolio-img">
                    <div class="portfolio-info">
                        <h3>Analytics Dashboard</h3>
                        <p id="desc4">Data visualization dashboard for enterprise clients with real-time metrics.</p>
                        <div class="portfolio-tags">
                            <span class="tag">Web Design</span>
                            <span class="tag">Data Visualization</span>
                            <span class="tag">React</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Get In Touch</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Let's talk about your next project</h3>
                    <p>I'm currently available for freelance work and full-time opportunities. Feel free to reach out!</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                               <h4>Email</h4>
                                <p>reaganomondi781@gmail.com</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+254707848992</p>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Location</h4>
                                <p>Homabay, Kenya</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <a href="#" class="logo">Reagan Omondi</a>
                <p>Creative Designer & Developer with AI Integration</p>
                <div class="social-links">
                    <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-dribbble"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 Reagan Omondi. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- AI Assistant -->
    <div class="ai-assistant">
        <div class="ai-toggle" id="aiToggle">💬
            <i class="fas fa-robot"></i>
        </div>
        <div class="ai-chat" id="aiChat">
            <div class="ai-header">
                <h4>AI Assistant</h4>
                <i class="fas fa-times" id="aiClose"></i>
            </div>
            <div class="ai-messages" id="aiMessages">
                <div class="message ai-message">
                    Hello! I'm your AI assistant. I can help you explore Reagan's portfolio, recommend projects based on your interests, or provide more details about any project. How can I help you today?
                </div>
            </div>
            <div class="ai-input">
                <input type="text" id="aiInput" placeholder="Ask me anything...">
                <button id="aiSend"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
    </div>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Portfolio filtering
        const filterBtns = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');
        
        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons
                filterBtns.forEach(b => b.classList.remove('active'));
                // Add active class to clicked button
                btn.classList.add('active');
                
                const filter = btn.getAttribute('data-filter');
                
                portfolioItems.forEach(item => {
                    if (filter === 'all' || item.getAttribute('data-category') === filter) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // AI Recommendations
        document.getElementById('aiRecommend').addEventListener('click', () => {
            // In a real implementation, this would use AI to analyze user preferences
            // For this demo, we'll simulate recommendations
            alert('AI Recommendation: Based on your interests, I recommend checking out the "Analytics Dashboard" project! It showcases advanced data visualization techniques.');
            
            // Highlight the recommended project
            const dashboard = document.querySelector('[data-category="web"]:nth-child(4)');
            if (dashboard) {
                dashboard.scrollIntoView({ behavior: 'smooth', block: 'center' });
                dashboard.style.boxShadow = '0 0 0 3px #6366f1';
                setTimeout(() => {
                    dashboard.style.boxShadow = '';
                }, 3000);
            }
        });
        
        // AI Descriptions
        document.getElementById('aiDescribe').addEventListener('click', () => {
            // Simulate AI-generated descriptions
            const descriptions = {
                desc1: "This e-commerce platform features an intuitive user interface with advanced filtering, personalized recommendations powered by machine learning, and a seamless one-click checkout process that increased conversion rates by 35%.",
                desc2: "The fitness tracker app uses AI to analyze user activity patterns and provide personalized workout recommendations. It includes nutrition tracking with image recognition for food logging and social features to connect with friends.",
                desc3: "This comprehensive brand identity system includes a responsive logo, color palette based on psychological principles, typography system, and brand guidelines that ensure consistency across all touchpoints.",
                desc4: "The analytics dashboard leverages AI to identify trends and anomalies in real-time data. It features interactive visualizations, customizable reports, and predictive analytics to forecast future performance."
            };
            
            Object.keys(descriptions).forEach(id => {
                document.getElementById(id).textContent = descriptions[id];
            });
            
            alert('AI has enhanced all project descriptions with detailed insights!');
        });
        
        // Form submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            
            alert(`Thank you, ${name}! Your message has been sent. I'll get back to you at ${email} soon.`);
            contactForm.reset();
        });
        
        // AI Assistant
        const aiToggle = document.getElementById('aiToggle');
        const aiChat = document.getElementById('aiChat');
        const aiClose = document.getElementById('aiClose');
        const aiMessages = document.getElementById('aiMessages');
        const aiInput = document.getElementById('aiInput');
        const aiSend = document.getElementById('aiSend');
        
        aiToggle.addEventListener('click', () => {
            aiChat.classList.toggle('active');
        });
        
        aiClose.addEventListener('click', () => {
            aiChat.classList.remove('active');
        });
        
        function addMessage(text, isUser = false) {
            const messageDiv = document.createElement('div');
            messageDiv.classList.add('message');
            messageDiv.classList.add(isUser ? 'user-message' : 'ai-message');
            messageDiv.textContent = text;
            aiMessages.appendChild(messageDiv);
            aiMessages.scrollTop = aiMessages.scrollHeight;
        }
        
        function getAIResponse(userMessage) {
            const lowerMessage = userMessage.toLowerCase();
            
            if (lowerMessage.includes('portfolio') || lowerMessage.includes('work')) {
                return "Alex has 4 featured projects: an E-commerce Platform, Fitness Tracker App, Brand Identity, and Analytics Dashboard. Would you like more details about any of them?";
            } else if (lowerMessage.includes('ecommerce') || lowerMessage.includes('shop')) {
                return "The E-commerce Platform features an intuitive UI with advanced filtering, personalized recommendations, and a seamless checkout process that increased conversion rates by 35%. It was built with React and Node.js.";
            } else if (lowerMessage.includes('fitness') || lowerMessage.includes('health')) {
                return "The Fitness Tracker App uses AI to analyze user activity patterns and provide personalized workout recommendations. It includes nutrition tracking with image recognition and social features.";
            } else if (lowerMessage.includes('brand') || lowerMessage.includes('identity')) {
                return "The Brand Identity project includes a responsive logo, color palette based on psychological principles, typography system, and comprehensive brand guidelines for consistent application.";
            } else if (lowerMessage.includes('dashboard') || lowerMessage.includes('analytics')) {
                return "The Analytics Dashboard leverages AI to identify trends and anomalies in real-time data. It features interactive visualizations, customizable reports, and predictive analytics capabilities.";
            } else if (lowerMessage.includes('contact') || lowerMessage.includes('hire')) {
                return "You can contact Alex through the form on this page, or directly at hello@alexmorgan.com. Alex is currently available for freelance and full-time opportunities!";
            } else if (lowerMessage.includes('hello') || lowerMessage.includes('hi') || lowerMessage.includes('hey')) {
                return "Hello! How can I assist you with Alex's portfolio today?";
            } else {
                return "I can help you explore Alex's portfolio, provide details about specific projects, or assist with contact information. What would you like to know?";
            }
        }
        
        function handleSendMessage() {
            const message = aiInput.value.trim();
            if (message) {
                addMessage(message, true);
                aiInput.value = '';
                
                // Simulate AI thinking
                setTimeout(() => {
                    const response = getAIResponse(message);
                    addMessage(response);
                }, 500);
            }
        }
        
        aiSend.addEventListener('click', handleSendMessage);
        aiInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                handleSendMessage();
            }
        });
    </script>
</body>
</html>
