# PRODIGY-INFOTECH-LANDING-PAGE

 HTML (index.html)
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Landing Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav id="navbar">
            <div class="container">
                <a href="#" class="logo">PRODIGY INFOTECH</a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
        </nav>
    </header>

    <section id="home">
        <h1>Welcome to PRODIGY INFOTECH</h1>
        <p>Your tech solution provider.</p>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>Information about the company.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <p>Description of services.</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Contact details.</p>
    </section>

    <script src="script.js"></script>
</body>
</html>


2. CSS (styles.css)
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

header {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1000;
}

.navbar {
    background-color: #333;
    color: #fff;
    padding: 15px 0;
}

.navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.navbar .logo {
    color: #fff;
    text-decoration: none;
    font-size: 24px;
    font-weight: bold;
}

.nav-links {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}

.nav-links li {
    margin-left: 20px;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #f39c12;
}

section {
    padding: 100px 20px;
}

section h1, section h2 {
    margin-top: 0;
}

/* Scroll Effect */
.navbar.scrolled {
    background-color: #222;
}

/* Responsive Styles */
@media (max-width: 768px) {
    .navbar .container {
        flex-direction: column;
        align-items: flex-start;
    }
    .nav-links {
        flex-direction: column;
        margin-top: 10px;
    }
    .nav-links li {
        margin: 10px 0;
    }
}
3. JavaScript (script.js)
javascript
Copy code
window.addEventListener('scroll', () => {
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});
