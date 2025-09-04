<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Kristel Jessa Romasanta - Programmer Portfolio</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');

    /* Background Image with dark overlay */
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Poppins', sans-serif;
      color: #eee;
      background: 
        linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.65)),
        url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') no-repeat center center fixed;
      background-size: cover;
      overflow-x: hidden;
    }

    /* Navbar */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(0, 0, 50, 0.75);
      backdrop-filter: blur(10px);
      box-shadow: 0 2px 15px rgba(0, 0, 0, 0.5);
      display: flex;
      justify-content: center;
      padding: 15px 0;
      z-index: 1000;
    }

    nav a {
      color: #a8caff;
      text-decoration: none;
      margin: 0 25px;
      font-weight: 600;
      font-size: 1.1rem;
      transition: color 0.3s ease;
      letter-spacing: 1.2px;
    }

    nav a:hover, nav a.active {
      color: #60a5fa;
      border-bottom: 2px solid #60a5fa;
      padding-bottom: 3px;
    }

    /* Container with glassmorphism */
    .container {
      max-width: 900px;
      background: rgba(255, 255, 255, 0.15);
      margin: 100px auto 60px;
      border-radius: 20px;
      padding: 40px 60px;
      box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      color: #f0f4ff;
      min-height: 500px;
      transition: opacity 0.5s ease, transform 0.5s ease;
      position: relative;
    }

    /* Profile Picture */
    #profile-pic-section {
      text-align: center;
      margin-bottom: 40px;
    }

    #profile-pic-section img {
      width: 170px;
      height: 170px;
      border-radius: 50%;
      object-fit: cover;
      border: 4px solid rgba(96, 165, 250, 0.7);
      box-shadow: 0 4px 18px rgba(96, 165, 250, 0.7);
      transition: transform 0.3s ease;
    }

    #profile-pic-section img:hover {
      transform: scale(1.05);
      cursor: pointer;
    }

    /* Headings */
    h1, h2 {
      margin-top: 0;
      font-weight: 700;
      text-shadow: 0 2px 6px rgba(0, 0, 30, 0.7);
      letter-spacing: 1.3px;
    }

    h1 {
      font-size: 3rem;
      color: #a8caff;
    }

    h2 {
      font-size: 2rem;
      color: #60a5fa;
      border-left: 6px solid #60a5fa;
      padding-left: 12px;
      margin-bottom: 20px;
      text-transform: uppercase;
    }

    /* Paragraph */
    p {
      font-size: 1.1rem;
      line-height: 1.6;
      color: #dbe9ff;
    }

    /* Lists */
    ul {
      list-style: none;
      padding-left: 0;
    }

    ul li {
      background: rgba(96, 165, 250, 0.3);
      margin-bottom: 12px;
      padding: 12px 18px;
      border-radius: 12px;
      font-weight: 600;
      box-shadow: 0 4px 12px rgba(96, 165, 250, 0.25);
      transition: background 0.3s ease;
    }

    ul li:hover {
      background: rgba(96, 165, 250, 0.5);
      cursor: default;
    }

    /* Project card */
    .project {
      background: rgba(96, 165, 250, 0.15);
      padding: 25px 30px;
      border-radius: 20px;
      margin-bottom: 30px;
      box-shadow: 0 6px 22px rgba(96, 165, 250, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .project:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 45px rgba(96, 165, 250, 0.4);
    }

    .project-title {
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 8px;
      color: #dbe9ff;
    }

    .project-tools {
      font-style: italic;
      font-weight: 400;
      color: #a8caff;
      margin-bottom: 15px;
    }

    /* Contact */
    a {
      color: #60a5fa;
      text-decoration: none;
      font-weight: 700;
      transition: color 0.3s ease;
    }

    a:hover {
      color: #a8caff;
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 25px 10px;
      font-weight: 400;
      font-size: 0.9rem;
      color: #9bb7ff88;
      letter-spacing: 1px;
      margin-top: 60px;
    }

    /* Hide all sections except active */
    section {
      display: none;
      opacity: 0;
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      padding-top: 60px;
      transition: opacity 0.5s ease;
    }
    section.active {
      display: block;
      position: relative;
      opacity: 1;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .container {
        padding: 30px 25px;
        margin: 90px 15px 60px;
      }

      nav a {
        margin: 0 12px;
        font-size: 1rem;
      }

      h1 {
        font-size: 2.4rem;
      }

      h2 {
        font-size: 1.5rem;
        border-left: 4px solid #60a5fa;
        padding-left: 8px;
      }

      #profile-pic-section img {
        width: 140px;
        height: 140px;
      }
    }
  </style>
</head>
<body>

  <nav>
    <a href="#" class="active" data-section="about">About Me</a>
    <a href="#" data-section="skills">Skills</a>
    <a href="#" data-section="projects">Projects</a>
    <a href="#" data-section="contact">Contact</a>
  </nav>

  <div class="container">
    
    <section id="about" class="active">
      <div id="profile-pic-section">
        <img src="Untitled design.jpg" alt="Kristel Jessa Romasanta Profile Picture" />
      </div>
      <h1>Kristel Jessa Romasanta</h1>
      <p><em>Basic Programmer & Database Developer</em></p>
      <p>Visual Studio Code | HTML | CSS | JavaScript | Python | SQLite | MySQL</p>
      <h2>About Me</h2>
      <p>
        I’m a detail-oriented programmer passionate about creating efficient and user-friendly applications. 
        I specialize in basic programming and database management, delivering clean, maintainable, 
        and functional solutions tailored to your needs.
      </p>
    </section>

    <section id="skills">
      <h2>Skills</h2>
      <ul>
        <li>Programming: HTML, CSS, JavaScript, Python</li>
        <li>Database: SQLite, MySQL</li>
        <li>Tools: Visual Studio Code, Git</li>
        <li>Concepts: Clean Code, Debugging, Basic UI/UX, SQL Queries</li>
      </ul>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      
      <div class="project">
        <div class="project-title">Inventory Management System</div>
        <div class="project-tools">Tools: Python, SQLite, Visual Studio Code</div>
        <p>A simple desktop app for tracking stock, sales, and orders that saved a local business hours weekly.</p>
      </div>

      <div class="project">
        <div class="project-title">Student Record Database</div>
        <div class="project-tools">Tools: Python, SQLite</div>
        <p>A small-scale database system for easy data input, search, and report generation for a school.</p>
      </div>

      <div class="project">
        <div class="project-title">Personal Website</div>
        <div class="project-tools">Tools: HTML, CSS, JavaScript</div>
        <p>A responsive website to showcase projects and contact information, designed with clean UI principles.</p>
      </div>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:romasantakristeljessa@gmail.com">romasantakristeljessa@gmail.com</a></p>
      <p>Phone: <a href="tel:+639357533570">+63 935 753 3570</a></p>
    </section>

  </div>

  <footer>
    &copy; 2025 Kristel Jessa Romasanta — All rights reserved.
  </footer>

  <script>
    // Navigation switching logic
    const navLinks = document.querySelectorAll('nav a');
    const sections = document.querySelectorAll('.container section');

    navLinks.forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();

        // Remove active from all nav links
        navLinks.forEach(l => l.classList.remove('active'));
        // Add active to clicked nav link
        link.classList.add('active');

        const targetSection = link.getAttribute('data-section');

        // Hide all sections and show the target section
        sections.forEach(section => {
          if (section.id === targetSection) {
            section.classList.add('active');
          } else {
            section.classList.remove('active');
          }
        });

        // Scroll top inside container on switch
        document.querySelector('.container').scrollTop = 0;
      });
    });
  </script>
</body>
</html>
