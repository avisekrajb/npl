
Here’s the updated code that includes the requested changes:

1. **Sliding photos** in the home section.
2. **Attractive orange buttons** for the teams section.
3. **Results section** with logos and dates displayed in a square shape layout.
4. **Mini ad video** at the bottom of the page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NPL - Nepal Premier League</title>
    <style>
        /* General Styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #1c3a72;
            padding: 10px 20px;
        }
        header img {
            height: 50px;
        }
        nav {
            text-align: center;
        }
        nav button {
            background-color: #2874A6;
            color: white;
            padding: 10px 20px;
            margin: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        nav button:hover {
            background-color: #1B4F72;
        }
        .section {
            display: none;
            padding: 20px;
            background-color: white;
        }
        .section.active {
            display: block;
        }

        /* Image Slider */
        .slider {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            overflow: hidden;
        }
        .slides {
            display: flex;
            transition: transform 0.5s ease;
        }
        .slides img {
            width: 100%;
            height: 400px;
        }
        .dot-container {
            text-align: center;
            margin-top: 10px;
        }
        .dot {
            height: 15px;
            width: 15px;
            margin: 0 2px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
            cursor: pointer;
        }
        .active-dot {
            background-color: #717171;
        }

        /* Teams Section */
        .team-buttons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .team-buttons button {
            background-color: #FFA500; /* Orange color */
            color: white;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            transition: background-color 0.3s ease;
        }
        .team-buttons button:hover {
            background-color: #FF8C00; /* Darker orange on hover */
        }

        /* Player Section */
        .player-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .player-card {
            width: 150px;
            margin: 10px;
            text-align: center;
        }
        .player-card img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
        }

        /* Results Section */
        .results-list {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .result-item {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 10px;
            border: 2px solid #2874A6;
            border-radius: 10px;
            padding: 10px;
            background-color: #fff;
            width: 300px;
            box-shadow: 0 0 5px rgba(0,0,0,0.2);
        }
        .result-item img {
            width: 50px;
            height: 50px;
            margin: 0 10px;
        }
        .result-date {
            font-weight: bold;
        }

        /* ID Card Section */
        .id-form {
            margin: 20px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: 0 auto;
        }
        .id-form label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .id-form input, .id-form select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .id-form button {
            width: 100%;
            padding: 10px;
            background-color: #2874A6;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .id-card-display {
            margin-top: 20px;
            text-align: center;
        }
        .id-card {
            width: 200px;
            height: 200px;
            padding: 20px;
            border: 2px solid red;
            text-align: center;
            background-color: white;
            display: inline-block;
        }
        .id-card img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
        }

        /* Live Score Section */
        .live-score {
            position: relative;
            background-color: #ff5722;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 18px;
            margin: 10px 0;
        }
        .pin-score {
            position: fixed;
            top: 10px;
            right: 10px;
            background-color: green;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 18px;
            display: none;
            z-index: 10; /* Ensures it stays on top */
        }
        .live-buttons {
            margin-top: 10px;
        }
        .live-buttons button {
            padding: 5px 10px;
            background-color: green;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        /* Login Section */
        .login-form {
            max-width: 400px;
            margin: 20px auto;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .login-form label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .login-form select, .login-form input {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-form button {
            width: 100%;
            padding: 10px;
            background-color: #2874A6;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        /* Mini Ad Video Section */
        .video-ad {
            width: 100%;
            max-width: 600px;
            margin: 20px auto;
            display: none;
        }

        /* Social Media Links */
        .social-media {
            text-align: center;
            margin-top: 10px;
        }
        .social-media a {
            margin: 0 10px;
            text-decoration: none;
            color: #2874A6;
            font-weight: bold;
        }

        /* Copyright Section */
        .copyright {
            text-align: center;
            margin: 20px 0;
            font-size: 14px;
            color: #555;
        }
    </style>
</head>
<body>

    <!-- Header with logos -->
    <header>
        <img src="Nepal.jpg" alt="Nepal Logo">
        <nav>
            <button onclick="showSection('home')">Home</button>
            <button onclick="showSection('teams')">Teams</button>
            <button onclick="showSection('results')">Results</button>
            <button onclick="showSection('idcard')">ID Card</button>
            <button onclick="showSection('login')">Login</button>
        </nav>
        <img src="Nepal.jpg" alt="Nepal Logo">
    </header>

    <!-- Home Section with player photo slider -->
    <section id="home" class="section active">
        <div class="slider">
            <div class="slides" id="slides">
                <img src="j.jpg" alt="Player 1">
                <img src="k.jpg" alt="Player 2">
                <img

 src="l.jpg" alt="Player 3">
                <img src="m.jpg" alt="Player 4">
                <img src="n.jpg" alt="Player 5">
            </div>
            <div class="dot-container" id="dotContainer"></div>
        </div>
        <div class="live-score" id="liveScore">Live Score: NPL Match - Team A vs Team B: 150/3 (20 overs)</div>
        <div class="live-buttons">
            <button onclick="pinScore()">Pin Score</button>
            <button onclick="watchLive()">Watch Live</button>
        </div>
    </section>

    <!-- Teams Section -->
    <section id="teams" class="section">
        <h2>Teams</h2>
        <div class="team-buttons">
            <button onclick="showTeam('Biratnagar Kings')">Biratnagar Kings</button>
            <button onclick="showTeam('Pokhara Avengers')">Pokhara Avengers</button>
            <button onclick="showTeam('Chitwan Rhinos')">Chitwan Rhinos</button>
            <button onclick="showTeam('Kathmandu Gorkhas')">Kathmandu Gorkhas</button>
            <button onclick="showTeam('Karnali Yaks')">Karnali Yaks</button>
            <button onclick="showTeam('Lumbini Lions')">Lumbini Lions</button>
            <button onclick="showTeam('Sudor Paschim Royals')">Sudor Paschim Royals</button>
            <button onclick="showTeam('Janakpur Bolts')">Janakpur Bolts</button>
        </div>
        <div class="player-list" id="teamPlayers"></div>
    </section>

    <!-- Results Section -->
    <section id="results" class="section">
        <h2>Match Results</h2>
        <div class="results-list" id="resultsList"></div>
    </section>

    <!-- ID Card Section -->
    <section id="idcard" class="section">
        <form class="id-form" id="idCardForm" onsubmit="generateIdCard(event)">
            <label for="name">Name:</label>
            <input type="text" id="name" required>

            <label for="age">Age:</label>
            <input type="number" id="age" required>

            <label for="role">Role:</label>
            <input type="text" id="role" required>

            <label for="phone">Phone Number:</label>
            <input type="text" id="phone" required>

            <label for="photoUpload">Upload Photo:</label>
            <input type="file" id="photoUpload" accept="image/*" required>

            <button type="submit">Generate ID Card</button>
        </form>
        <div class="id-card-display" id="idCardDisplay"></div>
    </section>

    <!-- Login Section -->
    <section id="login" class="section">
        <form class="login-form" onsubmit="handleLogin(event)">
            <label for="loginEmail">Email:</label>
            <input type="email" id="loginEmail" required>

            <label for="loginPhone">Phone Number:</label>
            <input type="text" id="loginPhone" required>

            <label for="loginPassword">Password:</label>
            <input type="password" id="loginPassword" value="Nepal" required>

            <button type="submit">Login</button>
        </form>
    </section>

    <!-- Mini Ad Video Section -->
    <div class="video-ad" id="videoAd">
        <video controls>
            <source src="video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <!-- Social Media Links -->
    <div class="social-media">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">Instagram</a>
    </div>

    <!-- Copyright Section -->
    <div class="copyright">
        &copy; 2024 Nepal Premier League. All rights reserved.
    </div>

    <script>
        // Image Slider Logic
        let currentSlide = 0;
        const slides = document.getElementById('slides');
        const dotsContainer = document.getElementById('dotContainer');
        const images = slides.getElementsByTagName('img');

        function showSlides() {
            if (currentSlide >= images.length) {
                currentSlide = 0;
            }
            slides.style.transform = `translateX(-${currentSlide * 100}%)`;
            updateDots();
            currentSlide++;
            setTimeout(showSlides, 3000);
        }

        function updateDots() {
            dotsContainer.innerHTML = '';
            for (let i = 0; i < images.length; i++) {
                const dot = document.createElement('span');
                dot.className = 'dot';
                if (i === currentSlide) {
                    dot.classList.add('active-dot');
                }
                dot.onclick = () => {
                    currentSlide = i;
                    showSlides();
                };
                dotsContainer.appendChild(dot);
            }
        }
        showSlides();

        // Function to show selected section
        function showSection(section) {
            const sections = document.querySelectorAll('.section');
            sections.forEach(s => s.classList.remove('active'));
            document.getElementById(section).classList.add('active');

            // Call displayResults if the results section is shown
            if (section === 'results') {
                displayResults();
            }
        }

        // Function to display player team
        function showTeam(team) {
            const players = {
                "Biratnagar Kings": ["Player 1", "Player 2", "Player 3"],
                "Pokhara Avengers": ["Player 4", "Player 5", "Player 6"],
                "Chitwan Rhinos": ["Player 7", "Player 8", "Player 9"],
                "Kathmandu Gorkhas": ["Player 10", "Player 11", "Player 12"],
                "Karnali Yaks": ["Player 13", "Player 14", "Player 15"],
                "Lumbini Lions": ["Player 16", "Player 17", "Player 18"],
                "Sudor Paschim Royals": ["Player 19", "Player 20", "Player 21"],
                "Janakpur Bolts": ["Player 22", "Player 23", "Player 24"]
            };

            const playerList = document.getElementById('teamPlayers');
            playerList.innerHTML = ''; // Clear previous players
            players[team].forEach(player => {
                const playerCard = document.createElement('div');
                playerCard.className = 'player-card';
                playerCard.innerHTML = `<img src="player_photo.jpg" alt="${player}">
                                        <div>${player}</div>`;
                playerList.appendChild(playerCard);
            });
        }

        // Function to display results
        function displayResults() {
            const results = [
                { match: "Biratnagar Kings vs Pokhara Avengers", result: "Biratnagar Kings won by 10 runs", logoA: "logo1.jpg", logoB: "logo2.jpg", date: "2024-10-22" },
                { match: "Chitwan Rhinos vs Kathmandu Gorkhas", result: "Kathmandu Gorkhas won by 5 wickets", logoA: "logo3.jpg", logoB: "logo4.jpg", date: "2024-10-21" },
                { match: "Karnali Yaks vs Lumbini Lions", result: "Karnali Yaks won by 20 runs", logoA: "logo5.jpg", logoB: "logo6.jpg", date: "2024-10-20" },
                { match: "Sudor Paschim Royals vs Janakpur Bolts", result: "Sudor Paschim Royals won by 3 wickets", logoA: "logo7.jpg", logoB: "logo8.jpg", date: "2024-10-19" }
            ];

            const resultsList = document.getElementById('resultsList');
            resultsList.innerHTML = '';
            results.forEach(result => {
                const resultItem = document.createElement('div');
                resultItem.className = 'result-item';
                resultItem.innerHTML = `
                    <img src="${result.logoA}" alt="Team A">
                    <div class="result-date">${result.date}</div>
                    <img src="${result.logoB}" alt="Team B">
                    <div><strong>${result.match}</strong>: ${result.result}</div>
                `;
                resultsList.appendChild(resultItem);
            });
        }

        // Function to handle ID Card generation
        function generateIdCard(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const age = document.getElementById('age').value;
            const role = document.getElementById('role').value;
            const phone = document.getElementById('phone').value;
            const photoUpload = document.getElementById('photoUpload').files[0];
            const reader = new FileReader();
            reader.onload = function (e) {
                const idCardDisplay = document.getElementById('idCardDisplay');
                idCardDisplay.innerHTML = `
                    <div class="id-card">
                        <img src="${e.target.result}" alt="${name}">
                        <div><strong>Name:</strong> ${name}</div>
                        <

div><strong>Age:</strong> ${age}</div>
                        <div><strong>Role:</strong> ${role}</div>
                        <div><strong>Phone:</strong> ${phone}</div>
                    </div>
                `;
            };
            reader.readAsDataURL(photoUpload);
        }

        // Function to handle login
        function handleLogin(event) {
            event.preventDefault();
            const email = document.getElementById('loginEmail').value;
            const phone = document.getElementById('loginPhone').value;
            const password = document.getElementById('loginPassword').value;

            // Logic to save data can be implemented here
            console.log(`Email: ${email}, Phone: ${phone}, Password: ${password}`);
        }

        // Pin Score Functionality
        function pinScore() {
            const scoreDiv = document.getElementById('liveScore');
            scoreDiv.classList.toggle('pinned');
        }

        // Watch Live Functionality
        function watchLive() {
            alert("Watching Live Match!");
        }
    </script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }

        h2 {
            color: #333;
        }

        .section {
            padding: 20px;
            margin: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .team-buttons button {
            background-color: orange; /* Attractive button color */
            border: none;
            color: white;
            padding: 10px 15px;
            margin: 5px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .team-buttons button:hover {
            background-color: darkorange;
        }

        .results-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .result-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            border: 1px solid #ddd;
            padding: 10px;
            border-radius: 5px;
            background-color: #f9f9f9;
        }

        .result-date {
            font-weight: bold;
        }

        .video-ad {
            margin: 20px auto;
            width: 80%;
            display: flex;
            justify-content: center;
        }

        .id-card {
            border: 2px solid red; /* Attractive border for ID card */
            padding: 10px;
            text-align: center;
        }

        .pinned {
            background-color: #ffe6e6; /* Color change for pinned score */
        }

        .player-card {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    </style>
</body>
</html>
```

### Key Changes Made:
1. **Home Section**: Photos are set to slide automatically as part of the image slider functionality.
2. **Teams Section**: Buttons are styled with an attractive orange color.
3. **Results Section**: Each result item includes both team logos and the date, formatted in a square layout.
4. **Mini Ad Video**: A video ad section is included at the bottom, allowing for video display. 

Let me know if you need any more adjustments!
