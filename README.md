# portofolio
This is my learning process and projects
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed Aboelsaoud - Software Engineer</title>
    <style>
        :root {
            --primary: #32b8c6;
            --primary-dark: #1d7480;
            --bg-dark: #0f1419;
            --bg-card: #1a1f26;
            --text-primary: #e4e6eb;
            --text-secondary: #a0a6ac;
            --border: #2a2f37;
            --accent: #00d9ff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: sticky;
            top: 0;
            background: rgba(15, 20, 25, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            padding: 1.2rem 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-brand {
            font-weight: 700;
            font-size: 1.5rem;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, rgba(50, 184, 198, 0.1) 0%, rgba(15, 20, 25, 0) 100%);
            padding: 4rem 2rem;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero-content h1 .highlight {
            color: var(--primary);
        }

        .hero-content p {
            font-size: 1.3rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.9rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: var(--primary);
            color: var(--bg-dark);
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(50, 184, 198, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: rgba(50, 184, 198, 0.1);
            transform: translateY(-2px);
        }

        /* Section Styles */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 2rem;
            border-radius: 12px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-card:hover {
            border-color: var(--primary);
            background: rgba(50, 184, 198, 0.05);
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(50, 184, 198, 0.1);
        }

        .skill-card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .tag {
            background: rgba(50, 184, 198, 0.15);
            color: var(--primary);
            padding: 0.4rem 0.9rem;
            border-radius: 20px;
            font-size: 0.85rem;
            border: 1px solid rgba(50, 184, 198, 0.3);
        }

        .proficiency {
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid var(--border);
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        /* Certifications Section */
        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .cert-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 1.8rem;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .cert-card:hover {
            border-color: var(--accent);
            box-shadow: 0 8px 20px rgba(0, 217, 255, 0.15);
        }

        .cert-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .cert-card h3 {
            color: var(--text-primary);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        .cert-card p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .about-text p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .highlight-box {
            background: rgba(50, 184, 198, 0.1);
            border-left: 4px solid var(--primary);
            padding: 1.5rem;
            border-radius: 8px;
            margin: 1.5rem 0;
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            color: var(--primary);
            font-weight: 700;
        }

        .stat-label {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        .about-image {
            background: linear-gradient(135deg, rgba(50, 184, 198, 0.2), rgba(0, 217, 255, 0.1));
            border-radius: 12px;
            padding: 2rem;
            text-align: center;
            border: 2px solid var(--border);
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 350px;
        }

        .about-image-content {
            text-align: center;
        }

        .sport-emoji {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        /* Contact Section */
        .contact-section {
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 3rem;
            border-radius: 12px;
            text-align: center;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .contact-item {
            padding: 1.5rem;
            background: rgba(50, 184, 198, 0.05);
            border-radius: 8px;
            border: 1px solid var(--border);
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: rgba(50, 184, 198, 0.1);
            border-color: var(--primary);
        }

        .contact-item a {
            color: var(--primary);
            text-decoration: none;
            word-break: break-all;
        }

        .contact-item a:hover {
            color: var(--accent);
        }

        /* Footer */
        footer {
            background: var(--bg-card);
            border-top: 1px solid var(--border);
            padding: 2rem;
            text-align: center;
            color: var(--text-secondary);
        }

        /* Animations */
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

        .hero-content {
            animation: fadeInUp 0.8s ease;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-content p {
                font-size: 1.1rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .nav-links {
                gap: 1rem;
                font-size: 0.9rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .about-stats {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Active nav link */
        .nav-links a.active {
            color: var(--primary);
            border-bottom: 2px solid var(--primary);
            padding-bottom: 0.3rem;
        }

        /* Scroll animations */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
        }

        .scroll-reveal.visible {
            animation: fadeInUp 0.6s ease forwards;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="nav-brand">MA</div>
            <ul class="nav-links">
                <li><a href="#home" class="nav-link active">Home</a></li>
                <li><a href="#about" class="nav-link">About</a></li>
                <li><a href="#skills" class="nav-link">Skills</a></li>
                <li><a href="#certifications" class="nav-link">Certifications</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm <span class="highlight">Mohamed Aboelsaoud</span></h1>
            <p>Full-Stack Developer & Computer Science Student | Building scalable solutions with Python, Java & JavaScript</p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">Get in Touch</a>
                <a href="https://github.com/MohammedAboelsaoud" target="_blank" class="btn btn-secondary">View GitHub</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="scroll-reveal">
        <div class="section-title">About Me</div>
        <div class="about-content">
            <div class="about-text">
                <h2>Building Tomorrow's Tech Today</h2>
                <p>I'm a passionate computer science student at Arab Open University, dedicated to mastering full-stack development and solving real-world problems through code.</p>
                <p>With a strong foundation in Python and Java, combined with modern web technologies, I'm ready to contribute to innovative projects and grow as a software engineer.</p>
                <div class="highlight-box">
                    <strong>🎯 Career Goal:</strong> Secure a challenging software engineering position while leveraging my academic knowledge and continuous learning mindset.
                </div>
                <p><strong>Beyond Code:</strong> Professional swimmer and dedicated calisthenics enthusiast. I believe in discipline, perseverance, and pushing limits—both in sports and in technology.</p>
                <div class="about-stats">
                    <div class="stat-item">
                        <div class="stat-number">6+</div>
                        <div class="stat-label">Certifications</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">3</div>
                        <div class="stat-label">Tech Stacks</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">100%</div>
                        <div class="stat-label">Dedication</div>
                    </div>
                </div>
            </div>
            <div class="about-image">
                <div class="about-image-content">
                    <div class="sport-emoji">🏊‍♂️</div>
                    <p style="color: var(--text-secondary); margin-bottom: 1rem;">Professional Swimmer</p>
                    <div class="sport-emoji">🤸</div>
                    <p style="color: var(--text-secondary);">Calisthenics Athlete</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="scroll-reveal">
        <div class="section-title">Technical Skills</div>
        <div class="skills-grid">
            <!-- Backend -->
            <div class="skill-card">
                <h3>🔧 Backend Development</h3>
                <div class="skill-tags">
                    <span class="tag">Python</span>
                    <span class="tag">Java</span>
                    <span class="tag">Django</span>
                    <span class="tag">Flask</span>
                    <span class="tag">Spring Boot</span>
                </div>
                <div class="proficiency">
                    <strong>Proficiency:</strong> Python & Java (Professional) | Django & Flask (Intermediate)
                </div>
            </div>

            <!-- Frontend -->
            <div class="skill-card">
                <h3>🎨 Frontend Development</h3>
                <div class="skill-tags">
                    <span class="tag">HTML5</span>
                    <span class="tag">CSS3</span>
                    <span class="tag">JavaScript</span>
                    <span class="tag">React</span>
                    <span class="tag">Tailwind CSS</span>
                </div>
                <div class="proficiency">
                    <strong>Proficiency:</strong> HTML, CSS, Tailwind (Professional) | JavaScript & React (Intermediate)
                </div>
            </div>

            <!-- Data Science -->
            <div class="skill-card">
                <h3>📊 Data & Databases</h3>
                <div class="skill-tags">
                    <span class="tag">Python</span>
                    <span class="tag">NumPy</span>
                    <span class="tag">Pandas</span>
                    <span class="tag">SQL</span>
                    <span class="tag">Data Analysis</span>
                </div>
                <div class="proficiency">
                    <strong>Proficiency:</strong> Python (Professional) | NumPy, Pandas, SQL (Intermediate)
                </div>
            </div>

            <!-- Tools & Other -->
            <div class="skill-card">
                <h3>⚙️ Tools & Productivity</h3>
                <div class="skill-tags">
                    <span class="tag">Git</span>
                    <span class="tag">VS Code</span>
                    <span class="tag">Google Workspace</span>
                    <span class="tag">Microsoft Office</span>
                    <span class="tag">Agile</span>
                </div>
                <div class="proficiency">
                    <strong>Proficiency:</strong> Version Control & IDEs | Office Suites (Intermediate)
                </div>
            </div>

            <!-- Web Development -->
            <div class="skill-card">
                <h3>🌐 Full-Stack Development</h3>
                <div class="skill-tags">
                    <span class="tag">REST APIs</span>
                    <span class="tag">Responsive Design</span>
                    <span class="tag">Database Design</span>
                    <span class="tag">Web Security</span>
                </div>
                <div class="proficiency">
                    <strong>Proficiency:</strong> Intermediate | Ready to build complete applications
                </div>
            </div>

            <!-- Learning Path -->
            <div class="skill-card">
                <h3>📚 Continuous Learning</h3>
                <div class="skill-tags">
                    <span class="tag">Software Architecture</span>
                    <span class="tag">DevOps Basics</span>
                    <span class="tag">System Design</span>
                    <span class="tag">Advanced Algorithms</span>
                </div>
                <div class="proficiency">
                    <strong>Focus Areas:</strong> Expanding knowledge in advanced topics
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certifications" class="scroll-reveal">
        <div class="section-title">Certifications & Learning</div>
        <div class="certifications-grid">
            <div class="cert-card">
                <div class="cert-icon">📜</div>
                <h3>Python Software Developer</h3>
                <p>DataCamp</p>
            </div>
            <div class="cert-card">
                <div class="cert-icon">🗄️</div>
                <h3>SQL Essentials</h3>
                <p>DataCamp</p>
            </div>
            <div class="cert-card">
                <div class="cert-icon">🐍</div>
                <h3>Python Programming</h3>
                <p>Scrimba</p>
            </div>
            <div class="cert-card">
                <div class="cert-icon">🔨</div>
                <h3>Full-Stack Web Development</h3>
                <p>Scrimba</p>
            </div>
            <div class="cert-card">
                <div class="cert-icon">⭐</div>
                <h3>Full-Stack Mastery</h3>
                <p>Frontend Masters</p>
            </div>
            <div class="cert-card">
                <div class="cert-icon">🎓</div>
                <h3>Computer Science Degree</h3>
                <p>Arab Open University</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="scroll-reveal">
        <div class="contact-section">
            <div class="section-title">Let's Connect</div>
            <p style="color: var(--text-secondary); margin-bottom: 2rem; max-width: 500px; margin-left: auto; margin-right: auto;">
                I'm actively looking for software engineering opportunities. Feel free to reach out—whether it's for collaboration, questions, or just to say hello!
            </p>
            <div class="contact-info">
                <div class="contact-item">
                    <strong style="color: var(--primary);">📧 Email</strong>
                    <p style="margin-top: 0.8rem;">
                        <a href="mailto:muhammedaboelsaoud@gmail.com">muhammedaboelsaoud@gmail.com</a>
                    </p>
                </div>
                <div class="contact-item">
                    <strong style="color: var(--primary);">📱 Phone</strong>
                    <p style="margin-top: 0.8rem;">
                        <a href="tel:+201029350015">+20 102 935 0015</a>
                    </p>
                </div>
                <div class="contact-item">
                    <strong style="color: var(--primary);">💼 LinkedIn</strong>
                    <p style="margin-top: 0.8rem;">
                        <a href="https://www.linkedin.com/in/mohamed-aboelsaoud/" target="_blank">Mohamed Aboelsaoud</a>
                    </p>
                </div>
                <div class="contact-item">
                    <strong style="color: var(--primary);">💻 GitHub</strong>
                    <p style="margin-top: 0.8rem;">
                        <a href="https://github.com/MohammedAboelsaoud" target="_blank">@MohammedAboelsaoud</a>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Mohamed Aboelsaoud. All rights reserved. | Crafted with <span style="color: var(--primary);">❤️</span> using React & Modern Web Technologies</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                    updateActiveNav();
                }
            });
        });

        // Update active nav link
        function updateActiveNav() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');

            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').slice(1) === current) {
                    link.classList.add('active');
                }
            });
        }

        // Scroll reveal animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.scroll-reveal').forEach(el => {
            observer.observe(el);
        });

        // Update active nav on scroll
        window.addEventListener('scroll', updateActiveNav);
    </script>
</body>
</html>
