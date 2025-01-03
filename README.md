<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #e8f8ff;
            color: #333;
        }

        header {
            background-color: #006994;
            color: white;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 2.8rem;
        }

        header p {
            margin: 5px 0 15px;
            font-size: 1.2rem;
        }

        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            margin: 0;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: #aed8e5;
        }

        main {
            padding: 20px;
        }

        section {
            margin-bottom: 40px;
        }

        h2 {
            color: #005075;
        }

        .project {
            background: #fff;
            border: 1px solid #ddd;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .project:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
        }

        form {
            max-width: 500px;
            margin: 0 auto;
        }

        form label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #005075;
        }

        form input, form textarea, form button {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        form button {
            background-color: #006994;
            color: white;
            font-size: 16px;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        form button:hover {
            background-color: #004c63;
        }

        footer {
            text-align: center;
            padding: 1rem 0;
            background: #004c63;
            color: white;
        }

        footer p {
            margin: 0;
        }

        .profiles {
            background-color: #fff;
            border: 1px solid #ddd;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-top: 40px;
        }

        .profiles a {
            text-decoration: none;
            color: #006994;
            font-size: 1.2rem;
        }

        .profiles a:hover {
            color: #004c63;
        }
    </style>
</head>
<body>
    <header>
        <h1>Sriya's Portfolio</h1>
        <p>Bachelors' of Technology | Student</p>
        <p id="greeting"></p>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#profiles">Profiles</a></li>
                <li><a href="#contact">Contact</a></li>
                
            </ul>
        </nav>
    </header>
    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>I am a dedicated Computer Science student specializing in Artificial Intelligence and Machine Learning. I have a strong passion for software development and problem-solving, focusing on creating practical solutions and applying AI and ML techniques to real-world challenges.</p>
        </section>
        <section id="projects">
            <h2>Projects</h2>
            <div class="project">
                <h3>Portfolio Website</h3>
                <p>A personal portfolio showcasing my skills and projects.</p>
            </div>
            <div class="project">
                <h3>Handwritten Digit and Character Recognition</h3>
                <p>Uses CNNs to predict handwritten digits and characters.</p>
            </div>
            <div class="project">
                <h3>Case Study</h3>
                <p>AI in Fertilizer use for Precision Farming.</p>
            </div>
        </section>
        <section id="profiles" class="profiles">
            <h2>My Profiles</h2>
            <p>Feel free to connect with me on LinkedIn:</p>
            <a href="https://www.linkedin.com/in/sethu-sriya-a8431a2bb" target="_blank">Sethu Sriya on LinkedIn</a>
        </section>
        <section id="contact">
            <h2>Contact Me</h2>
            <form id="contact-form">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>
                <button type="submit">Send</button>
            </form>
        </section>
        
    </main>
    <footer>
        <p>&copy; 2024 Sethu Sriya. All rights reserved.</p>
    </footer>
    <script>
        // Dynamic greeting based on time
        const greetingElement = document.getElementById('greeting');
        const currentHour = new Date().getHours();
        if (currentHour < 12) {
            greetingElement.textContent = 'Good Morning!';
        } else if (currentHour < 18) {
            greetingElement.textContent = 'Good Afternoon!';
        } else {
            greetingElement.textContent = 'Good Evening!';
        }

        // Form submission alert
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            alert(`Thank you, ${name}, for reaching out! I will get back to you soon.`);
            this.reset();
        });
    </script>
</body>
</html>
