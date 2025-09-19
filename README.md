<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gauri Suryawanshi - Interactive GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0d1117, #161b22, #21262d);
            color: #ffffff;
            font-family: 'Segoe UI', 'Fira Code', monospace;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Animated Background */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 245, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 107, 107, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 80%, rgba(0, 245, 255, 0.05) 0%, transparent 50%);
            animation: backgroundShift 20s ease-in-out infinite;
            z-index: -1;
        }

        @keyframes backgroundShift {
            0%, 100% { transform: rotate(0deg) scale(1); }
            50% { transform: rotate(180deg) scale(1.1); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 60px 0;
            background: linear-gradient(135deg, #00f5ff, #ff6b6b, #00f5ff);
            background-size: 400% 400%;
            animation: gradientShift 8s ease-in-out infinite;
            margin-bottom: 40px;
            border-radius: 20px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(13, 17, 23, 0.8);
            z-index: 1;
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .typing-animation {
            font-size: 2.5em;
            font-weight: bold;
            color: #00f5ff;
            margin: 20px 0;
            min-height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .stats-badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .badge {
            background: linear-gradient(135deg, #00f5ff, #0066cc);
            padding: 8px 16px;
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .badge:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 25px rgba(0, 245, 255, 0.3);
            border-color: #00f5ff;
        }

        /* Terminal Section */
        .terminal {
            background: #0d1117;
            border: 2px solid #00f5ff;
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            font-family: 'Fira Code', monospace;
            position: relative;
            box-shadow: 0 0 30px rgba(0, 245, 255, 0.2);
        }

        .terminal::before {
            content: '● ● ●';
            position: absolute;
            top: 15px;
            left: 20px;
            color: #ff6b6b;
            font-size: 12px;
        }

        .terminal-header {
            text-align: center;
            color: #00f5ff;
            margin-bottom: 20px;
            font-size: 1.2em;
        }

        .code-block {
            background: #161b22;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #00f5ff;
            margin: 20px 0;
            overflow-x: auto;
        }

        /* Tech Stack Grid */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .tech-category {
            background: rgba(22, 27, 34, 0.8);
            border: 2px solid #00f5ff;
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .tech-category::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 245, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .tech-category:hover::before {
            left: 100%;
        }

        .tech-category:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 245, 255, 0.3);
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 15px;
        }

        .tech-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #00f5ff, #ff6b6b);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 12px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-icon:hover {
            transform: rotate(360deg) scale(1.2);
            box-shadow: 0 5px 15px rgba(0, 245, 255, 0.5);
        }

        /* Stats Dashboard */
        .stats-dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .stat-card {
            background: linear-gradient(135deg, #161b22, #21262d);
            border: 2px solid #00f5ff;
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .stat-card::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent, rgba(0, 245, 255, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .stat-card:hover::after {
            opacity: 1;
        }

        .stat-card:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 25px rgba(0, 245, 255, 0.3);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: #00f5ff;
            text-shadow: 0 0 10px rgba(0, 245, 255, 0.5);
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        /* Progress Bars */
        .progress-section {
            margin: 40px 0;
        }

        .progress-item {
            margin: 20px 0;
        }

        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: bold;
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: #21262d;
            border-radius: 6px;
            overflow: hidden;
            box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #00f5ff, #ff6b6b);
            border-radius: 6px;
            transition: width 2s ease-in-out;
            position: relative;
            overflow: hidden;
        }

        .progress-fill::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 2s ease-in-out infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        /* Project Cards */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .project-card {
            background: rgba(22, 27, 34, 0.9);
            border: 2px solid #ff6b6b;
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 107, 107, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 20px 40px rgba(255, 107, 107, 0.3);
        }

        .project-status {
            display: inline-block;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8em;
            font-weight: bold;
            margin: 10px 0;
        }

        .status-development { background: #ffa500; color: #000; }
        .status-planning { background: #00ff00; color: #000; }
        .status-prototype { background: #ffff00; color: #000; }

        /* Interactive Elements */
        .interactive-section {
            background: rgba(13, 17, 23, 0.8);
            border: 2px solid #00f5ff;
            border-radius: 20px;
            padding: 30px;
            margin: 40px 0;
            text-align: center;
        }

        .quote-box {
            background: linear-gradient(135deg, #ff6b6b, #00f5ff);
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            font-style: italic;
            font-size: 1.1em;
            animation: colorShift 5s ease-in-out infinite;
        }

        @keyframes colorShift {
            0%, 100% { filter: hue-rotate(0deg); }
            50% { filter: hue-rotate(180deg); }
        }

        .coding-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .stat-item {
            background: rgba(22, 27, 34, 0.8);
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #00f5ff;
        }

        /* Social Links */
        .social-section {
            text-align: center;
            margin: 50px 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 30px 0;
        }

        .social-link {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(135deg, #0077b5, #00f5ff);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .social-link:hover::before {
            left: 100%;
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 15px 30px rgba(0, 245, 255, 0.4);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #161b22, #0d1117);
            border-radius: 20px;
            margin-top: 50px;
        }

        .footer-animation {
            font-size: 3em;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container { padding: 10px; }
            .typing-animation { font-size: 1.8em; }
            .stats-badges { flex-direction: column; align-items: center; }
            .tech-grid { grid-template-columns: 1fr; }
            .projects-grid { grid-template-columns: 1fr; }
        }

        /* Loading Animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0d1117;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }

        .loading.hide {
            opacity: 0;
            pointer-events: none;
        }

        .spinner {
            width: 50px;
            height: 50px;
            border: 3px solid #21262d;
            border-top: 3px solid #00f5ff;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loading" id="loading">
        <div class="spinner"></div>
    </div>

    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="header-content">
                <h1 style="font-size: 3em; margin-bottom: 10px;">💫 Gauri Suryawanshi</h1>
                <div class="typing-animation" id="typing-text">Frontend Developer</div>
                <p style="font-size: 1.2em; margin: 20px 0;">Passionate Coder from India 🇮🇳</p>
                
                <div class="stats-badges">
                    <a href="#" class="badge">👀 Profile Views: 1,234</a>
                    <a href="#" class="badge">👥 Followers: 567</a>
                    <a href="#" class="badge">⭐ Stars: 890</a>
                    <a href="#" class="badge">📅 Years on GitHub: 3</a>
                </div>
            </div>
        </div>

        <!-- Terminal About Section -->
        <div class="terminal">
            <div class="terminal-header">🧠 About Me - Interactive Terminal</div>
            <div style="text-align: center; margin-bottom: 20px;">
                <code style="color: #00f5ff;">gauri@developer:~$ whoami</code>
            </div>
            
            <div class="code-block">
                <pre style="color: #ffffff; font-size: 0.9em;">
<span style="color: #ff6b6b;">class</span> <span style="color: #00f5ff;">GauriSuryawanshi</span> {
    <span style="color: #ffa500;">private</span> info = {
        name: <span style="color: #90EE90;">"Gauri Suryawanshi 👩‍💻"</span>,
        location: <span style="color: #90EE90;">"India 🇮🇳"</span>,
        role: <span style="color: #90EE90;">"Frontend Developer"</span>,
        experience: <span style="color: #90EE90;">"Passionate Developer"</span>,
        education: <span style="color: #90EE90;">"Computer Science Student"</span>,
        mindset: <span style="color: #90EE90;">"Growth-oriented & Solution-focused"</span>
    };

    <span style="color: #ffa500;">public</span> <span style="color: #00f5ff;">getMotivation</span>(): <span style="color: #ff6b6b;">string</span> {
        <span style="color: #ffa500;">return</span> <span style="color: #90EE90;">"Code with passion, create with purpose! ✨"</span>;
    }
}

<span style="color: #ffa500;">const</span> gauri = <span style="color: #ffa500;">new</span> <span style="color: #00f5ff;">GauriSuryawanshi</span>();
console.log(gauri.getMotivation());
                </pre>
            </div>
        </div>

        <!-- Tech Stack Section -->
        <h2 style="text-align: center; font-size: 2.5em; margin: 40px 0; color: #00f5ff;">💻 Tech Arsenal</h2>
        <div class="tech-grid">
            <div class="tech-category">
                <h3 style="color: #00f5ff; text-align: center;">🏆 Primary Languages</h3>
                <div class="tech-icons">
                    <div class="tech-icon" style="background: linear-gradient(135deg, #ED8B00, #ff9500);">Java</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #00599C, #0077CC);">C++</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #3776AB, #4B9CD3);">Python</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #F7DF1E, #FFE55C);">JS</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #3178C6, #4B9CD3);">TS</div>
                </div>
            </div>
            
            <div class="tech-category">
                <h3 style="color: #ff6b6b; text-align: center;">🎨 Frontend Mastery</h3>
                <div class="tech-icons">
                    <div class="tech-icon" style="background: linear-gradient(135deg, #E34F26, #FF6B47);">HTML5</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #1572B6, #4B9CD3);">CSS3</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #61DAFB, #87E6FB);">React</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #06B6D4, #38BDF8);">Tailwind</div>
                </div>
            </div>

            <div class="tech-category">
                <h3 style="color: #90EE90; text-align: center;">⚙️ Backend & Databases</h3>
                <div class="tech-icons">
                    <div class="tech-icon" style="background: linear-gradient(135deg, #339933, #66BB6A);">Node.js</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #4479A1, #6B9BD2);">MySQL</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #47A248, #66BB6A);">MongoDB</div>
                    <div class="tech-icon" style="background: linear-gradient(135deg, #000000, #404040);">Express</div>
                </div>
            </div>
        </div>

        <!-- Stats Dashboard -->
        <h2 style="text-align: center; font-size: 2.5em; margin: 40px 0; color: #ff6b6b;">📊 GitHub Analytics</h2>
        <div class="stats-dashboard">
            <div class="stat-card">
                <div class="stat-number" id="commits">234</div>
                <div>Total Commits</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="repos">42</div>
                <div>Repositories</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="contributions">156</div>
                <div>Contributions</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="streak">28</div>
                <div>Day Streak</div>
            </div>
        </div>

        <!-- Skills Progress -->
        <h2 style="text-align: center; font-size: 2.5em; margin: 40px 0; color: #90EE90;">🌟 Skills Progress</h2>
        <div class="progress-section">
            <div class="progress-item">
                <div class="progress-label">
                    <span>Java</span>
                    <span>90%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 90%;"></div>
                </div>
            </div>
            
            <div class="progress-item">
                <div class="progress-label">
                    <span>JavaScript</span>
                    <span>85%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 85%;"></div>
                </div>
            </div>
            
            <div class="progress-item">
                <div class="progress-label">
                    <span>React</span>
                    <span>80%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 80%;"></div>
                </div>
            </div>
            
            <div class="progress-item">
                <div class="progress-label">
                    <span>Python</span>
                    <span>75%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 75%;"></div>
                </div>
            </div>
        </div>

        <!-- Projects Section -->
        <h2 style="text-align: center; font-size: 2.5em; margin: 40px 0; color: #ffa500;">🚀 Active Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3 style="color: #00f5ff;">Frontend Portfolio</h3>
                <p>Building stunning personal portfolio with React & Three.js</p>
                <div class="project-status status-development">🟡 In Development</div>
                <div style="margin-top: 15px;">
                    <strong>Tech:</strong> React, Three.js, Framer Motion, Tailwind CSS
                </div>
            </div>
            
            <div class="project-card">
                <h3 style="color: #00f5ff;">Algorithm Visualizer</h3>
                <p>Interactive tool for learning data structures & algorithms</p>
                <div class="project-status status-planning">🟢 Planning Phase</div>
                <div style="margin-top: 15px;">
                    <strong>Tech:</strong> JavaScript, Canvas API, React
                </div>
            </div>
            
            <div class="project-card">
                <h3 style="color: #00f5ff;">Unity Game Project</h3>
                <p>2D platformer with unique mechanics</p>
                <div class="project-status status-prototype">🟡 Prototyping</div>
                <div style="margin-top: 15px;">
                    <strong>Tech:</strong> Unity, C#, Photoshop
                </div>
            </div>
        </div>

        <!-- Interactive Fun Zone -->
        <div class="interactive-section">
            <h2 style="color: #ff6b6b; margin-bottom: 30px;">🎮 Fun Zone - Interactive Elements</h2>
            
            <div class="quote-box" id="quote-box">
                "Code is like humor. When you have to explain it, it's bad." - Cory House
            </div>
            
            <h3 style="color: #00f5ff; margin: 30px 0;">🎵 Coding Vibes</h3>
            <div class="coding-stats">
                <div class="stat-item">
                    <div>🎧 Currently Playing</div>
                    <div style="color: #00f5ff;">Lo-fi Hip Hop Radio 📻</div>
                </div>
                <div class="stat-item">
                    <div>☕ Coffee Status</div>
                    <div style="color: #ffa500;">████████░░ 80% Full</div>
                </div>
                <div class="stat-item">
                    <div>🌙 Night Owl Mode</div>
                    <div style="color: #90EE90;">✅ Activated</div>
                </div>
                <div class="stat-item">
                    <div>💡 Ideas Today</div>
                    <div style="color: #ff6b6b;" id="ideas-counter">47</div>
                </div>
                <div class="stat-item">
                    <div>🔥 Lines of Code</div>
                    <div style="color: #00f5ff;" id="code-counter">234</div>
                </div>
            </div>
        </div>

        <!-- Social Links -->
        <div class="social-section">
            <h2 style="color: #00f5ff; margin-bottom: 30px;">🌐 Connect With Me</h2>
            <p style="font-size: 1.2em; margin-bottom: 30px;">Let's build something amazing together! 🚀</p>
            
            <div class="social-links">
                <a href="#" class="social-link" style="background: linear-gradient(135deg, #0077B5, #00A0DC);">
                    LinkedIn - Connect
                </a>
                <a href="#" class="social-link" style="background: linear-gradient(135deg, #D14836, #FF6B6B);">
                    Gmail - Email Me
                </a>
                <a href="#" class="social-link" style="background: linear-gradient(135deg, #5B4638, #8B6914);">
                    CodeChef - Follow
                </a>
                <a href="#" class="social-link" style="background: linear-gradient(135deg, #181717, #404040);">
                    GitHub - Follow
                </a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-animation">🚀</div>
            <h2 style="color: #00f5ff; margin: 20px 0;">Thanks for Visiting My Digital Space!</h2>
            <p style="font-size: 1.2em; color: #ff6b6b; margin: 15px 0;">
                💫 "The best way to predict the future is to create it!" 💫
            </p>
            <p style="color: #90EE90;">
                Made with 💖, fueled by ☕, and powered by endless curiosity!
            </p>
            <p style="margin-top: 20px; font-weight: bold; color: #00f5ff;">
                Keep coding, keep creating! 🚀✨
            </p>
        </div>
    </div>

    <script>
        // Loading Animation
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('loading').classList.add('hide');
            }, 2000);
        });

        // Typing Animation
        const typingTexts = [
            "💻 Frontend Developer",
            "🎮 Game Development Enthusiast", 
            "🚀 Building Digital Experiences",
            "⚡ Competitive Programmer",
            "🎯 Problem Solver",
            "🌟 Creative Coder"
        ];
        
        let currentTextIndex = 0;
        let currentCharIndex = 0;
        let isDeleting = false;
        const typingElement = document.getElementById('typing-text');
        
        function typeEffect() {
            const currentText = typingTexts[currentTextIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, currentCharIndex - 1);
                currentCharIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, currentCharIndex + 1);
                currentCharIndex++;
            }
            
            if (!isDeleting && currentCharIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && currentCharIndex === 0) {
                isDeleting = false;
                currentTextIndex = (currentTextIndex + 1) % typingTexts.length;
            }
            
            const speed = isDeleting ? 50 : 100;
            setTimeout(typeEffect, speed);
        }
        
        typeEffect();

        // Counter Animations
        function animateCounter(elementId, finalValue, duration = 2000) {
            const element = document.getElementById(elementId);
            let startValue = 0;
            const increment = finalValue / (duration / 50);
            
            const counter = setInterval(() => {
                startValue += increment;
                element.textContent = Math.floor(startValue);
                
                if (startValue >= finalValue) {
                    element.textContent = finalValue;
                    clearInterval(counter);
                }
            }, 50);
        }

        // Animate counters when they come into view
        const observerOptions = {
            threshold: 0.5
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const counters = entry.target.querySelectorAll('[id$="-counter"], .stat-number');
                    counters.forEach(counter => {
                        const finalValue = parseInt(counter.textContent) || 0;
                        animateCounter(counter.id, finalValue);
                    });
                }
            });
        }, observerOptions);

        // Observe stats dashboard
        document.addEventListener('DOMContentLoaded', () => {
            const statsSection = document.querySelector('.stats-dashboard');
            if (statsSection) {
                observer.observe(statsSection);
                
                // Start counter animations after a delay
                setTimeout(() => {
                    animateCounter('commits', 234, 2000);
                    animateCounter('repos', 42, 1500);
                    animateCounter('contributions', 156, 1800);
                    animateCounter('streak', 28, 1200);
                    animateCounter('ideas-counter', 47, 1000);
                    animateCounter('code-counter', 234, 1500);
                }, 3000);
            }
        });

        // Random Dev Quotes
        const quotes = [
            "Code is like humor. When you have to explain it, it's bad. - Cory House",
            "First, solve the problem. Then, write the code. - John Johnson", 
            "Experience is the name everyone gives to their mistakes. - Oscar Wilde",
            "In order to be irreplaceable, one must always be different. - Coco Chanel",
            "Java is to JavaScript what car is to Carpet. - Chris Heilmann",
            "The best way to get a project done faster is to start sooner. - Jim Highsmith",
            "Perfection is achieved not when there is nothing more to add, but rather when there is nothing more to take away. - Antoine de Saint-Exupery",
            "Code never lies, comments sometimes do. - Ron Jeffries"
        ];

        function changeQuote() {
            const quoteBox = document.getElementById('quote-box');
            const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
            
            quoteBox.style.opacity = '0';
            setTimeout(() => {
                quoteBox.textContent = randomQuote;
                quoteBox.style.opacity = '1';
            }, 500);
        }

        // Change quote every 10 seconds
        setInterval(changeQuote, 10000);

        // Parallax Effect for Background
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const rate = scrolled * -0.5;
            document.body.style.backgroundPositionY = rate + 'px';
        });

        // Interactive Tech Icons
        document.querySelectorAll('.tech-icon').forEach(icon => {
            icon.addEventListener('click', () => {
                icon.style.transform = 'rotate(360deg) scale(1.5)';
                icon.style.transition = 'all 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
                
                setTimeout(() => {
                    icon.style.transform = '';
                    icon.style.transition = 'all 0.3s ease';
                }, 800);
            });
        });

        // Progress Bar Animation
        function animateProgressBars() {
            const progressFills = document.querySelectorAll('.progress-fill');
            progressFills.forEach((fill, index) => {
                setTimeout(() => {
                    const width = fill.style.width;
                    fill.style.width = '0%';
                    fill.offsetWidth; // Trigger reflow
                    fill.style.width = width;
                }, index * 200);
            });
        }

        // Animate progress bars when they come into view
        const progressObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateProgressBars();
                }
            });
        }, observerOptions);

        document.addEventListener('DOMContentLoaded', () => {
            const progressSection = document.querySelector('.progress-section');
            if (progressSection) {
                progressObserver.observe(progressSection);
            }
        });

        // Social Link Interactions
        document.querySelectorAll('.social-link').forEach(link => {
            link.addEventListener('mouseover', () => {
                link.style.transform = 'translateY(-8px) scale(1.15)';
            });
            
            link.addEventListener('mouseout', () => {
                link.style.transform = 'translateY(-5px) scale(1.1)';
            });
        });

        // Easter Egg - Konami Code
        let konamiCode = [38, 38, 40, 40, 37, 39, 37, 39, 66, 65];
        let userInput = [];

        document.addEventListener('keydown', (e) => {
            userInput.push(e.keyCode);
            
            if (userInput.length > konamiCode.length) {
                userInput.shift();
            }
            
            if (JSON.stringify(userInput) === JSON.stringify(konamiCode)) {
                // Easter egg activated!
                document.body.style.filter = 'hue-rotate(180deg) saturate(2)';
                alert('🎉 Easter Egg Activated! You found the secret Konami code! 🥚');
                
                setTimeout(() => {
                    document.body.style.filter = '';
                }, 5000);
                
                userInput = [];
            }
        });

        // Dynamic Background Particles
        function createParticle() {
            const particle = document.createElement('div');
            particle.style.position = 'fixed';
            particle.style.width = '2px';
            particle.style.height = '2px';
            particle.style.backgroundColor = Math.random() > 0.5 ? '#00f5ff' : '#ff6b6b';
            particle.style.borderRadius = '50%';
            particle.style.left = Math.random() * window.innerWidth + 'px';
            particle.style.top = '-10px';
            particle.style.pointerEvents = 'none';
            particle.style.zIndex = '-1';
            particle.style.opacity = '0.7';
            
            document.body.appendChild(particle);
            
            const animation = particle.animate([
                { transform: 'translateY(0px)', opacity: 0.7 },
                { transform: `translateY(${window.innerHeight + 10}px)`, opacity: 0 }
            ], {
                duration: Math.random() * 3000 + 2000,
                easing: 'linear'
            });
            
            animation.onfinish = () => {
                particle.remove();
            };
        }

        // Create particles periodically
        setInterval(createParticle, 300);

        // Console Easter Egg
        console.log(`
            🎉 Welcome to Gauri's GitHub Profile! 
            
            You're checking the console - you must be a developer! 
            
            Want to connect? Here are some fun facts:
            • This profile has ${document.querySelectorAll('.tech-icon').length} tech icons
            • There are ${quotes.length} random quotes
            • Try the Konami code: ↑ ↑ ↓ ↓ ← → ← → B A
            
            Let's build something amazing together! 🚀
        `);
    </script>
</body>
</html>
