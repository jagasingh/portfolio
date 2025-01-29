HTML Code

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to my Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="hero">
        <h1>Hi, I'm <span>Jagadhish</span></h1>
        <p>Aspiring Data Analyst | Software Developer</p>
        <img src="c:\Users\Dinesh kumar S\OneDrive\Pictures\WhatsApp Image 2024-07-12 at 12.49.54_493e0aca.jpg" alt="">
        <style>
             img{
            width: 100px ;
            border-radius: 50px;
        }
        </style>
    
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <main>
        <section id="about" class="about">
            <h2>About Me</h2>
            <p>After starting my career as a civil engineer, I discovered my passion for technology and problem-solving, which led me to pursue a transition into software development.
                Through my engineering background, I honed my analytical and problem-solving abilities. I've complemented this with coding skills, completing certifications in Python, SQl.
                I'm eager to contribute as a software developer, leveraging my skills to solve real-world challenges and grow in this dynamic industry.</p>
        </section>

        <section id="skills" class="skills">
            <h2>Skills</h2>
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
                <li>Python</li>
                <li>SQL</li>
                <li>microsoft</li>
            </ul>
        </section>

        <section id="projects" class="projects">
            <h2>Projects</h2>
            <div class="project">
                <h3>Project 1</h3>
                <p>Description of the project.</p>
                <a href="https://github.com/your-project-link" target="_blank">View on GitHub</a>
            </div>
            <div class="project">
                <h3>Project 2</h3>
                <p>Description of the project.</p>
                <a href="https://github.com/your-project-link" target="_blank">View on GitHub</a>
            </div>
        </section>

        <section id="contact" class="contact">
            <h2>Contact</h2>
            <form action="https://formspree.io/f/YOUR_ENDPOINT" method="POST">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Your Message" required></textarea>
                <button type="submit">Send</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Your Name. All rights reserved.</p>
    </footer>
</body>
</html>


---




/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* General Styles */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}

header.hero {
    background: #007BFF;
    color: white;
    text-align: center;
    padding: 50px 20px;
}

header.hero h1 span {
    color: #FFD700;
}

nav ul {
    display: flex;
    justify-content: center;
    list-style: none;
    background: #333;
    padding: 10px;
}

nav ul li {
    margin: 0 10px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

nav ul li a:hover {
    text-decoration: underline;
}

main {
    padding: 20px;
}

section {
    margin: 20px 0;
}

h2 {
    color: #007BFF;
    margin-bottom: 10px;
}

/* Skills Section */
.skills ul {
    list-style: none;
    display: flex;
    gap: 10px;
}

.skills ul li {
    background: #f4f4f4;
    padding: 10px 20px;
    border-radius: 5px;
}

/* Projects Section */
.projects .project {
    border: 1px solid #ddd;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 5px;
}

.projects .project h3 {
    margin-bottom: 5px;
}

.projects .project a {
    color: #007BFF;
    text-decoration: none;
}

.projects .project a:hover {
    text-decoration: underline;
}

/* Contact Section */
.contact form {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.contact input,
.contact textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.contact button {
    background: #007BFF;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 5px;
}

.contact button:hover {
    background: #0056b3;
}

/* Footer */
footer {
    text-align: center;
    background: #333;
    color: white;
    padding: 10px 0;
    margin-top: 20px;
}
/* Fade-In Animation */
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Apply Animation to All Sections */
section {
    opacity: 0; /* Start invisible */
    animation: fadeIn 1s ease-in-out forwards; /* Triggers fade-in */
}

/* Add Delays for Staggered Effect */
#about {
    animation-delay: 0.3s;
}

#skills {
    animation-delay: 0.6s;
}

#projects {
    animation-delay: 0.9s;
}

#contact {
    animation-delay: 1.2s;
}
/* Button Hover Effect */
button, a {
    transition: transform 0.2s ease, background-color 0.2s ease;
}

button:hover, a:hover {
    transform: scale(1.1); /* Slightly enlarge */
    background-color: #0056b3; /* Change color for buttons */
}

/* Optional: Add Shadow on Hover */
button:hover {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
nav ul li a {
    position: relative;
    transition: color 0.3s ease;
}

nav ul li a::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background: var(--primary-color);
    transition: width 0.3s ease;
}

nav ul li a:hover::after {
    width: 100%; /* Underline slides across the link */
}
@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-10px);
    }
    60% {
        transform: translateY(-5px);
    }
}

button {
    animation: bounce 2s infinite;
}
/* Hidden State Before Scroll */
section {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.8s ease, transform 0.8s ease;
}
