<div class="skill-item">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/android/android-original.svg" alt="Android" class="skill-icon-img">
                        <div class="skill-name">Android</div>
                    </div>
                    <div class="skill-item">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" class="skill-icon-img">
                        <div class="skill-name">C++</div>
                    </div>
                    <div class="skill-item">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg" alt="C#" class="skill-icon-img">
                        <div class="skill-name">C#</div>
                    </div>
                    <div class="skill-item">
                        <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" class=<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gauri Suryawanshi - Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0f0f1e 0%, #1a1a2e 50%, #16213e 100%);
            color: #e1e1e6;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .wave-emoji {
            display: inline-block;
            animation: wave 2s infinite;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0% { transform: rotate(0deg); }
            10% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            30% { transform: rotate(14deg); }
            40% { transform: rotate(-4deg); }
            50% { transform: rotate(10deg); }
            60% { transform: rotate(0deg); }
            100% { transform: rotate(0deg); }
        }

        .typing {
            font-size: 3rem;
            font-weight: bold;
            margin: 1rem 0;
            background: linear-gradient(45deg, #64ffda, #536dfe, #ff6b9d);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 3s ease infinite, typing 3s steps(22) 1s both;
            overflow: hidden;
            white-space: nowrap;
            border-right: 3px solid #64ffda;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        .subtitle {
            font-size: 1.5rem;
            color: #64ffda;
            margin-bottom: 2rem;
            opacity: 0;
            animation: fadeInUp 1s 2s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            opacity: 0;
            animation: fadeInUp 1s 3s both;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(100, 255, 218, 0.1);
        }

        .card h3 {
            color: #64ffda;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .skill-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-item:hover {
            background: rgba(100, 255, 218, 0.1);
            transform: scale(1.05);
        }

        .skill-icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .skill-name {
            font-size: 0.8rem;
            text-align: center;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem 2rem;
            background: rgba(100, 255, 218, 0.1);
            border: 2px solid #64ffda;
            border-radius: 50px;
            color: #64ffda;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .contact-link:hover {
            background: #64ffda;
            color: #0f0f1e;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(100, 255, 218, 0.3);
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            background: #64ffda;
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
            opacity: 0.1;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-30px) rotate(120deg); }
            66% { transform: translateY(30px) rotate(240deg); }
        }

        .trophy-section {
            margin: 2rem 0;
            display: flex;
            justify-content: center;
        }

        .trophy-section .card {
            max-width: 800px;
            width: 100%;
        }

        .trophy-image {
            width: 100%;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .trophy-image:hover {
            transform: scale(1.02);
        }

        .profile-views {
            text-align: center;
            margin: 2rem 0;
        }

        .views-badge {
            border-radius: 10px;
            transition: transform 0.3s ease;
            box-shadow: 0 5px 15px rgba(100, 255, 218, 0.3);
        }

        .views-badge:hover {
            transform: scale(1.05);
        }

        .github-stats {
            text-align: center;
            margin-top: 2rem;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
            justify-items: center;
        }

        .stats-image {
            border-radius: 15px;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 2px solid rgba(100, 255, 218, 0.2);
        }

        .stats-image:hover {
            transform: scale(1.03) translateY(-5px);
            box-shadow: 0 20px 40px rgba(100, 255, 218, 0.2);
            border-color: #64ffda;
        }

        .streak-stat {
            max-width: 500px;
            width: 100%;
        }

        @media (max-width: 768px) {
            .typing {
                font-size: 2rem;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
            
            .stats-section {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <div class="header">
            <h1 class="typing">Hi <span class="wave-emoji">👋</span>, I'm Gauri Suryawanshi</h1>
            <p class="subtitle">A passionate frontend developer from India</p>
        </div>

        <div class="stats-section">
            <div class="card">
                <h3>💬 About Me</h3>
                <p>Ask me about <strong>Git, GitHub, LaTeX</strong></p>
                <p>📫 Reach me: <strong>suryawanshigauri23@gmail.com</strong></p>
            </div>

            <div class="card">
                <h3>🚀 Languages & Tools</h3>
                <div class="skills-grid">
                    <div class="skill-item">
                        <div class="skill-icon">🤖</div>
                        <div class="skill-name">Android</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">⚡</div>
                        <div class="skill-name">C++</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🎯</div>
                        <div class="skill-name">C#</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🌿</div>
                        <div class="skill-name">Git</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🌐</div>
                        <div class="skill-name">HTML5</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">☕</div>
                        <div class="skill-name">Java</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🐧</div>
                        <div class="skill-name">Linux</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🗄️</div>
                        <div class="skill-name">MySQL</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🐍</div>
                        <div class="skill-name">Python</div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-icon">🎮</div>
                        <div class="skill-name">Unity</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="contact-links">
            <a href="https://linkedin.com/in/gauri-suryawanshi" class="contact-link">
                <span>💼</span> LinkedIn
            </a>
            <a href="https://www.codechef.com/users/band_dog_63" class="contact-link">
                <span>👨‍💻</span> CodeChef
            </a>
        </div>

        <div class="trophy-section">
            <div class="card">
                <h3>🏆 GitHub Trophies</h3>
                <img src="https://github-profile-trophy.vercel.app/?username=s-au-23&theme=darkhub&no-frame=true&column=3&margin-w=15" alt="GitHub Trophies" class="trophy-image">
            </div>
        </div>

        <div class="profile-views">
            <img src="https://komarev.com/ghpvc/?username=s-au-23&label=Profile%20views&color=64ffda&style=for-the-badge" alt="Profile Views" class="views-badge">
        </div>

        <div class="github-stats">
            <div class="stats-grid">
                <img src="https://github-readme-stats.vercel.app/api/top-langs?username=s-au-23&show_icons=true&locale=en&layout=compact&theme=dark&bg_color=0f0f1e&border_color=64ffda&title_color=64ffda&text_color=e1e1e6" alt="Top Languages" class="stats-image">
                <img src="https://github-readme-stats.vercel.app/api?username=s-au-23&show_icons=true&locale=en&theme=dark&bg_color=0f0f1e&border_color=64ffda&title_color=64ffda&text_color=e1e1e6&icon_color=64ffda" alt="GitHub Stats" class="stats-image">
            </div>
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=s-au-23&theme=dark&background=0f0f1e&border=64ffda&stroke=64ffda&ring=64ffda&fire=ff6b9d&currStreakLabel=64ffda" alt="GitHub Streak" class="stats-image streak-stat">
        </div>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 30;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                const size = Math.random() * 4 + 2;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 6;
                
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                particle.style.left = posX + '%';
                particle.style.top = posY + '%';
                particle.style.animationDelay = delay + 's';
                
                particlesContainer.appendChild(particle);
            }
        }

        // Add staggered animation to cards
        function animateCards() {
            const cards = document.querySelectorAll('.card');
            cards.forEach((card, index) => {
                card.style.animationDelay = (3 + index * 0.2) + 's';
            });
        }

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            animateCards();
            
            // Remove typing cursor after animation
            setTimeout(() => {
                document.querySelector('.typing').style.borderRight = 'none';
            }, 4000);
        });

        // Add some interactive hover effects
        document.querySelectorAll('.skill-item').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.05) rotate(5deg)';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1) rotate(0deg)';
            });
        });
    </script>
</body>
</html>
