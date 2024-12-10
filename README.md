# interndesire-project-level-1
Responsive Portfolio Website and Static Landing Page
CODE:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepak Boddula Portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            scroll-behavior: smooth;
            margin: 0;
            padding: 0;
        }
        .navbar {
            background-color: #6C63FF;
        }
        .navbar a {
            color: white !important;
            font-weight: bold;
            transition: color 0.3s;
        }
        .navbar a:hover {
            color: #574BFE;
        }
        .hero {
            background-color: #6C63FF;
            color: white;
            text-align: center;
            padding: 80px 20px;
        }
        .hero h1 {
            font-size: 3.5rem;
            font-weight: bold;
        }
        .hero p {
            font-size: 1.25rem;
            margin-bottom: 30px;
        }
        .cta-button {
            background-color: #574BFE;
            border: none;
            padding: 15px 30px;
            font-size: 1.25rem;
            color: white;
            cursor: pointer;
            text-decoration: none;
        }
        .cta-button:hover {
            background-color: #6C63FF;
        }
        .section-title {
            color: #6C63FF;
            font-weight: bold;
            text-align: center;
            margin-bottom: 30px;
        }
        .skills .badge {
            margin: 5px;
            padding: 10px 15px;
            font-size: 1rem;
        }
        .projects ul {
            list-style: none;
            padding: 0;
        }
        .projects ul li {
            background: #f8f9fa;
            margin: 10px 0;
            padding: 10px;
            border-left: 5px solid #6C63FF;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .contact-me form .form-label {
            font-weight: bold;
        }
        .btn-primary {
            background-color: #6C63FF;
            border: none;
        }
        .btn-primary:hover {
            background-color: #574BFE;
        }
        .footer {
            background-color: #6C63FF;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }
        .footer a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            transition: color 0.3s;
        }
        .footer a:hover {
            color: #574BFE;
        }
        /* Hero section responsiveness */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>

<!-- Instructions for Task 1: Responsive Portfolio Website -->
<!-- Task 1: Build a responsive personal portfolio website using HTML, CSS, and Bootstrap. -->
<!-- Include: -->
<!-- A professional homepage with an introduction and image. -->
<!-- Sections for "About Me," "Projects," "Skills," and "Contact Me." -->
<!-- Mobile-first design ensuring the layout is optimized for all screen sizes. -->
<!-- Creative design principles to make it visually appealing and functional. -->

<!-- Instructions for Task 2: Static Landing Page -->
<!-- Task 2: Create a visually attractive static landing page. -->
<!-- Ensure: -->
<!-- Use of well-structured HTML and CSS. -->
<!-- Inclusion of a header, footer, call-to-action button, and hero section. -->
<!-- Proper padding, margins, and alignment for all elements. -->
<!-- A consistent color scheme and typography throughout the page. -->

<!-- Navigation Bar -->
<nav class="navbar navbar-expand-lg navbar-dark sticky-top">
    <div class="container">
        <a class="navbar-brand" href="#">Deepak Boddula</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="#hero">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#about">About Me</a></li>
                <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
                <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
                <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
            </ul>
        </div>
    </div>
</nav>

<!-- Hero Section -->
<header class="hero" id="hero">
    <h1>Deepak Boddula</h1>
    <p>Passionate Web Developer | Clean Code Enthusiast | Problem Solver</p>
    <a href="#contact" class="cta-button">Get in Touch</a>
</header>

<!-- About Me Section -->
<section class="about-me container mt-5" id="about">
    <h2 class="section-title">About Me</h2>
    <div class="row align-items-center">
        <div class="col-md-6">
            <img src="https://i.ibb.co/5GwSBh1/Screenshot-2024-11-18-234900.png" alt="Deepak Boddula" class="img-fluid rounded">
        </div>
        <div class="col-md-6">
            <p>
                Hi, I'm Deepak Boddula, a web developer from Sree Chaitanya College of Engineering. I specialize in building responsive websites using HTML, CSS, JavaScript, and frameworks like React. I'm passionate about solving problems through technology.
            </p>
        </div>
    </div>
</section>

<!-- Skills Section -->
<section class="skills container mt-5" id="skills">
    <h2 class="section-title">Skills</h2>
    <div class="text-center">
        <span class="badge bg-primary">C</span>
        <span class="badge bg-success">C++</span>
        <span class="badge bg-warning text-dark">Python</span>
        <span class="badge bg-info">HTML</span>
        <span class="badge bg-secondary">CSS</span>
        <span class="badge bg-dark">JavaScript</span>
    </div>
</section>

<!-- Projects Section -->
<section class="projects container mt-5" id="projects">
    <h2 class="section-title">Projects</h2>
    <ul>
        <li>Responsive Portfolio Website</li>
        <li>Static Landing Page</li>
        <li>Interactive Login Form</li>
        <li>E-Commerce Website</li>
    </ul>
</section>

<!-- Contact Me Section -->
<section class="contact-me container mt-5" id="contact">
    <h2 class="section-title">Contact Me</h2>
    <form id="contactForm" onsubmit="return validateForm()">
        <div class="mb-3">
            <label for="name" class="form-label">Your Name</label>
            <input type="text" class="form-control" id="name" required>
        </div>
        <div class="mb-3">
            <label for="email" class="form-label">Your Email</label>
            <input type="email" class="form-control" id="email" required>
        </div>
        <div class="mb-3">
            <label for="message" class="form-label">Message</label>
            <textarea class="form-control" id="message" rows="4" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary w-100">Send</button>
    </form>
</section>

<!-- Footer -->
<footer class="footer">
    <p>&copy; 2024 Deepak Boddula. All Rights Reserved.</p>
    <a href="https://www.linkedin.com/in/deepak-boddula-2248ba271?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/deepakboddula" target="_blank">GitHub</a>
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.3/dist/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.min.js"></script>

<!-- Smooth Scrolling Script -->
<script>
    // Simple form validation
    function validateForm() {
        let name = document.getElementById("name").value;
        let email = document.getElementById("email").value;
        let message = document.getElementById("message").value;
        if (name == "" || email == "" || message == "") {
            alert("All fields must be filled out!");
            return false;
        }
        alert("Form submitted successfully!");
        return true;
    }
</script>
</body>
</html>
