<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.5">
    <title>Cooperative Muslim Association</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #333;
            background-color: #968c8a;
            transition: background-color 0.3s, color 0.3s;
        }

        body.dark-mode {
            background-color: #121212;
            color: #e0e0e0;
        }

        /* Header Section */
        header {
            background-color: #2c3e50;
            color: #fff;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            animation: fadeInDown 1s ease-in-out;
        }

        header .logo img {
            height: 50px;
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        nav ul li {
            margin-left: 20px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #3498db;
        }

        .theme-toggle {
            background-color: #3498db;
            color: #110e0e;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 1em;
            transition: background-color 0.3s, transform 0.3s;
        }

        .theme-toggle:hover {
            background-color: #2980b9;
            transform: scale(1.05);
        }

        /* Banner Section */
        .banner {
            position: relative;
            text-align: center;
            animation: fadeIn 2s ease-in-out;
        }

        .banner img {
            width: 100%;
            height: auto;
        }

        .banner-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
            animation: zoomIn 1.5s ease-in-out;
        }

        .banner-text h1 {
            margin: 0;
            font-size: 2.5em;
        }

        .banner-text p {
            margin: 10px 0 0;
            font-size: 1.2em;
        }

        /* Sections */
        section {
            padding: 40px 20px;
            animation: fadeInUp 1s ease-in-out;
        }

        h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #2c3e50;
            animation: fadeIn 1.5s ease-in-out;
        }

        body.dark-mode h2 {
            color: #e0e0e0;
        }

        .service-list, .event-list, .teachings-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }

        .service-item, .event-item, .teaching-item {
            background-color: #f4f4f4;
            padding: 20px;
            margin: 10px;
            border-radius: 10px;
            width: 30%;
            text-align: center;
            transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
        }

        body.dark-mode .service-item, body.dark-mode .event-item, body.dark-mode .teaching-item {
            background-color: #1e1e1e;
            color: #e0e0e0;
        }

        .service-item:hover, .event-item:hover, .teaching-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        /* Quran Section */
        .quran-section {
            text-align: center;
        }

        .quran-embed {
            width: 100%;
            height: 600px;
            border: none;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        /* Footer Section */
        footer {
            background-color: #2c3e50;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            margin-top: 20px;
            animation: fadeInUp 1s ease-in-out;
        }

        body.dark-mode footer {
            background-color: #1c1c1c;
        }

        /* Upload Section */
        .upload-section {
            text-align: center;
            margin-top: 20px;
        }

        .upload-section input[type="file"] {
            display: none;
        }

        .upload-section label {
            background-color: #3498db;
            color: #fff;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .upload-section label:hover {
            background-color: #2980b9;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes zoomIn {
            from { opacity: 0; transform: translate(-50%, -50%) scale(0.5); }
            to { opacity: 1; transform: translate(-50%, -50%) scale(1); }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="logo">
            <img src="images/logo.png" alt="Muslim Association Logo">
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#events">Events</a></li>
                <li><a href="#teachings">Teachings</a></li>
                <li><a href="#quran">Read Quran</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        <button class="theme-toggle" onclick="toggleTheme()">🌙 Dark Mode</button>
    </header>

    <!-- Banner Section -->
    <section id="home" class="banner">
        <div class="upload-section">
            <label for="banner-upload">Upload Banner</label>
            <input type="file" id="banner-upload" accept="image/*" onchange="uploadBanner(event)">
        </div>
        <img id="banner-image" src="images/banner.jpg" alt="Banner Image">
        <div class="banner-text">
            <h1>Cooperative University of Kenya Muslim Association</h1>
            <p>Welcome to the Cooperative University of Kenya Muslim Association</p>
            <p>Strengthening the community through faith, unity, and service.</p>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="about">
        <h2>About Us</h2>
        <p>The Cooperative University Muslim Association is dedicated to fostering a strong, supportive, and inclusive Muslim community. We provide educational programs, charitable services, and community events to help individuals and families thrive.</p>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <h2>Our Services</h2>
        <div class="service-list">
            <div class="service-item">
                <h3>Educational Programs</h3>
                <p>We offer Quran classes, Islamic studies, and youth mentorship programs.</p>
            </div>
            <div class="service-item">
                <h3>Ramadan Activities</h3>
                <p>Join us for Taraweeh prayers, Iftar gatherings, and Quran recitation sessions during Ramadan.</p>
            </div>
            <div class="service-item">
                <h3>Community Events</h3>
                <p>Organizing Eid celebrations, lectures, and family gatherings.</p>
            </div>
        </div>
    </section>

    <!-- Events Section -->
    <section id="events" class="events">
        <h2>Upcoming Events</h2>
        <div class="event-list">
            <div class="event-item">
                <h3>Eid al-Fitr Celebration</h3>
                <p>Date: May 12, 2024</p>
                <p>Location: Community Center</p>
            </div>
            <div class="event-item">
                <h3>Islamic Lecture Series</h3>
                <p>Date: June 1, 2024</p>
                <p>Location: Masjid Al-Noor</p>
            </div>
        </div>
    </section>

    <!-- Teachings Section -->
    <section id="teachings" class="teachings">
        <h2>Islamic Teachings</h2>
        <div class="teachings-list">
            <div class="teaching-item">
                <h3>Five Pillars of Islam</h3>
                <p>Shahada, Salah, Zakat, Sawm, and Hajj are the foundation of a Muslim's faith and practice.</p>
            </div>
            <div class="teaching-item">
                <h3>Quranic Studies</h3>
                <p>Learn the Quran with proper Tajweed and understand its teachings.</p>
            </div>
            <div class="teaching-item">
                <h3>Hadith and Sunnah</h3>
                <p>Study the sayings and actions of Prophet Muhammad (PBUH) here is an example;
                    Hadith
The Prophet Muhammad (ﷺ) said:

"When the month of Ramadan begins, the gates of Paradise are opened, the gates of Hell are closed, and the devils are chained.
                </p>
            </div>
        </div>
    </section>

    <!-- Quran Section -->
    <section id="quran" class="quran-section">
        <h2>Read Quran</h2>
        <iframe
            class="quran-embed"
            src="https://quran.com"
            allowfullscreen
        ></iframe>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>If you have any questions or would like to get involved, please reach out to us:</p>
        <ul>
            <li>Email: hassan24.abdighar@student.cuk.ac.ke</li>
            <li>Phone: 0725177467</li>
            <li>Address: Masjid Al-Noor, Nairobi, Karen</li>
        </ul>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2023 Cooperative Muslim Association. All rights reserved.</p>
    </footer>

    <script>
        // Theme Toggle
        function toggleTheme() {
            const body = document.body;
            body.classList.toggle('dark-mode');
            const themeToggle = document.querySelector('.theme-toggle');
            if (body.classList.contains('dark-mode')) {
                themeToggle.textContent = '☀️ Light Mode';
            } else {
                themeToggle.textContent = '🌙 Dark Mode';
            }
        }

        // Upload Banner Functionality
        function uploadBanner(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function (e) {
                    const bannerImage = document.getElementById('banner-image');
                    bannerImage.src = e.target.result;
                };
                reader.readAsDataURL(file);
            }
        }
    </script>
</body>
</html>
