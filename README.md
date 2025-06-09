# Abinetic Artificial Intelligence

ICT171 Assignment 2 – Cloud Server Project Documentation

Project Information

**Project Title: Abinetic Artificial Intelligence**

- Student Name: Abin Ajan Mathew

- Student ID: 35573777

- Server Public IP: 52.77.173.228

- Domain Name: abinetic.online

- Domain Provider: Namecheap

- Video Explainer Link:

- Github Link:https://github.com/binboi40/ICT171-Assignment-2/edit/main/README.md


TOTAL COST OF OWNERSHIP (TCO)

EC2 - $O(per year)
NAMECHEAP(DOMAIN) - $1.75(per year)
STORAGE(8GB) - $9.60(per year)
TOTAL - $11.35(per year)


Project Description

Abinetic Artificial Intelligence is an upcoming smart AI system that is mainly aimed for helping people and businesses work 10x faster and smarter. For this, we use the most advanced machine learning to automate tasks, make predictions and to operate across all domains like healthcare, education, customer service and more. Our main focus is on the ethical AI, continuous learning and real-world applicability.

Server Setup Instructions

1. Launch EC2 instance (Ubuntu 22.04)

2. SSH into the server:

ssh -i "your-key.pem" ubuntu@52.77.173.228

3. Update packages:

sudo apt update && sudo apt upgrade -y

4. Install Apache:

sudo apt install apache2 -y

5. Link domain via Namecheap DNS:

- Set A Record for abinetic.online to 52.77.173.228

6. Optional: Install Certbot for HTTPS (Let's Encrypt)

Connection to server through SSH:


ssh -i "abin.pem"


SSL/TLS Configuration:




Script Used:

INDEX.HTML

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Abinetic AI Portal</title>

<!-- Google Fonts -->

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">

<!-- Tailwind CSS -->

<script src="https://cdn.tailwindcss.com"></script>

<!-- FontAwesome -->

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>

body { font-family: 'Inter', sans-serif; }

.section-bg { background: rgba(15,23,42,0.8); backdrop-filter: blur(8px); }

</style>

</head>

<body class="bg-gray-900 text-white transition-colors duration-300">


<!-- Dark/Light Toggle -->

<button id="theme-toggle" class="fixed top-4 right-4 z-50 bg-gray-800 p-2 rounded-full text-ai-neon hover:bg-gray-700">

<i id="theme-icon" class="fas fa-moon"></i>

</button>


<!-- Header -->

<header class="fixed w-full bg-black/70 backdrop-blur-md z-40">

<!-- ... navigation remains ... -->

</header>


<main class="pt-20">

<!-- Other sections: hero, project, dashboard, tools, vpn -->


<!-- Login Section -->

<section id="login" class="py-20 section-bg">

<div class="max-w-md mx-auto px-6">

<div class="bg-black/60 p-8 rounded-xl shadow-lg">

<h3 class="text-3xl font-bold text-cyan-400 mb-6 text-center">Sign In</h3>

<form id="loginForm" class="space-y-5">

<input type="email" id="email" placeholder="Email" required class="w-full px-4 py-2 rounded bg-gray-700 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-cyan-400 text-white" />

<input type="password" id="password" placeholder="Password" required class="w-full px-4 py-2 rounded bg-gray-700 border border-gray-600 focus:outline-none focus:ring-2 focus:ring-cyan-400 text-white" />

<button type="submit" class="w-full py-3 bg-cyan-400 text-black font-bold rounded-lg hover:bg-cyan-500 transition">Login</button>

</form>

</div>

</div>

</section>

</main>


<footer class="bg-black/70 text-center text-gray-400 py-6">

<p>&copy; 2025 Abinetic AI. All rights reserved.</p>

<p>Server IP: 52.77.173.228 | Student: Abin Ajan Mathew (ID: 35573777)</p>

</footer>


<!-- Scripts -->

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>

// Dark/Light and Nav toggles unchanged...


// Login Redirect to Separate Dashboard Page

document.getElementById('loginForm').addEventListener('submit', function(e) {

e.preventDefault();

const email = document.getElementById('email').value;

const password = document.getElementById('password').value;

if (email && password) {

// Redirect to dashboard.html

window.location.href = 'dashboard.html';

} else {

alert('Please enter valid credentials.');

}

});

</script>

</body>

</html>























DASHBOARD.HTML

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Abinetic AI Portal</title>


<!-- Google Fonts -->

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">


<!-- Tailwind CSS -->

<script src="https://cdn.tailwindcss.com"></script>


<!-- FontAwesome Icons -->

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">


<!-- Particles.js for background animation -->

<script src="https://cdn.jsdelivr.net/npm/particles.js"></script>


<style>

body {

font-family: 'Inter', sans-serif;

background-color: #0f172a;

color: #fff;

}

.section-bg {

background-color: rgba(15, 23, 42, 0.8);

backdrop-filter: blur(8px);

}

.neon {

text-shadow:

0 0 4px rgba(56, 189, 248, 0.7),

0 0 8px rgba(56, 189, 248, 0.5);

}

#particles-js {

position: fixed;

top: 0;

left: 0;

width: 100%;

height: 100%;

z-index: -1;

}

</style>

</head>

<body>


<div id="particles-js"></div>


<header class="fixed top-0 w-full bg-black/40 backdrop-blur-md z-50">

<div class="container mx-auto flex items-center justify-between py-4 px-6">

<h1 class="text-2xl font-bold text-cyan-400 neon">Abinetic AI</h1>

<nav class="hidden md:flex space-x-8">

<a href="#home" class="hover:text-cyan-300 transition">Home</a>

<a href="#project" class="hover:text-cyan-300 transition">About</a>

<a href="#dashboard" class="hover:text-cyan-300 transition">Description</a>

<a href="#tools" class="hover:text-cyan-300 transition">Tools</a>

<a href="#contact" class="hover:text-cyan-300 transition">Contact</a>

</nav>

<button id="nav-toggle" aria-label="Toggle navigation" class="md:hidden text-cyan-400">

<i class="fas fa-bars fa-lg"></i>

</button>

</div>

<div id="nav-menu" class="hidden md:hidden bg-black/80">

<a href="#home" class="block py-3 px-6 hover:bg-gray-800">Home</a>

<a href="#project" class="block py-3 px-6 hover:bg-gray-800">About</a>

<a href="#dashboard" class="block py-3 px-6 hover:bg-gray-800">Description</a>

<a href="#tools" class="block py-3 px-6 hover:bg-gray-800">Tools</a>

<a href="#contact" class="block py-3 px-6 hover:bg-gray-800">Contact</a>

</div>

</header>


<main class="pt-24">


<!-- Hero -->

<section id="home" class="flex items-center justify-center h-screen text-center px-6">

<div class="bg-black/60 p-8 rounded-2xl shadow-xl border border-cyan-500 max-w-3xl">

<h2 class="text-5xl md:text-6xl font-bold text-cyan-400 neon mb-4">Abinetic Artificial Intelligence</h2>

<p class="text-lg md:text-xl text-gray-200 mb-6">

Empowering you with <span class="font-semibold neon">10× faster</span> insights through cutting-edge AI.

</p>

<div class="space-x-4">

<a href="#dashboard" class="px-6 py-3 bg-gradient-to-r from-cyan-400 to-blue-500 text-black rounded-full shadow hover:scale-105 transition">

View Description

</a>

<a href="#tools" class="px-6 py-3 border border-cyan-400 rounded-full hover:bg-cyan-500 transition">

AI Tools

</a>

</div>

</div>

</section>


<!-- About -->

<section id="project" class="py-20 section-bg">

<div class="max-w-4xl mx-auto text-center px-6">

<h3 class="text-3xl md:text-4xl font-bold text-cyan-400 neon mb-4">About Abinetic AI</h3>

<p class="text-gray-300 text-lg md:text-xl">

A smart AI platform automating data analysis, predictions, and decision-making for healthcare, finance, education, and beyond.

</p>

</div>

</section>


<!-- Description -->

<section id="dashboard" class="py-20 bg-gradient-to-b from-gray-900 via-black to-gray-900">

<div class="max-w-5xl mx-auto text-center px-6">

<h3 class="text-3xl md:text-4xl font-bold text-cyan-400 neon mb-6">My Project Description</h3>

<p class="text-gray-300 leading-relaxed text-lg md:text-xl">

Abinetic Artificial Intelligence offers a huge advantage for every individuals and businesses who are looking to enhance their productivity and decision-making skills. By shortening the machine learning and deep learning technologies, Abinetic AI automates routine tasks, understands hard datas very efficiently and creates insightful predictions that allows each and every users to work smarter and faster. Its speciality is that it adapts to every situation, like if it is related to medical, educational, or even data analysis situations, it gives us options and even ideas on what our needs are and helps us to complete our tasks before in hand, which will help save a lot more time and less errors.

</p>

</div>

</section>


<!-- Tools -->

<section id="tools" class="py-20 section-bg">

<div class="max-w-5xl mx-auto text-center px-6">

<h3 class="text-3xl md:text-4xl font-bold text-cyan-400 neon mb-6">Explore AI Tools</h3>

<div class="grid gap-8 grid-cols-1 md:grid-cols-3">

<!-- Tool 1: Model Trainer -->

<div class="bg-black/60 border border-cyan-500 p-6 rounded-2xl hover:bg-black/70 transition">

<i class="fas fa-brain text-4xl text-cyan-400 neon mb-4"></i>

<h4 class="text-xl font-semibold text-white mb-2">Model Trainer</h4>

<p class="text-gray-300 mb-4">Train custom ML models with our intuitive interface.</p>

<a href="model-trainer.html" class="inline-block px-4 py-2 bg-cyan-500 text-black font-semibold rounded hover:bg-cyan-400 transition">

Launch Trainer

</a>

</div>


<!-- Tool 2: Data Analyzer -->

<div class="bg-black/60 border border-cyan-500 p-6 rounded-2xl hover:bg-black/70 transition">

<i class="fas fa-chart-pie text-4xl text-cyan-400 neon mb-4"></i>

<h4 class="text-xl font-semibold text-white mb-2">Data Analyzer</h4>

<p class="text-gray-300 mb-4">Upload CSVs and visualize insights in seconds.</p>

<a href="data-analyzer.html" class="inline-block px-4 py-2 bg-cyan-500 text-black font-semibold rounded hover:bg-cyan-400 transition">

Launch Analyzer

</a>

</div>


<!-- Tool 3: Chatbot -->

<div class="bg-black/60 border border-cyan-500 p-6 rounded-2xl hover:bg-black/70 transition">

<i class="fas fa-robot text-4xl text-cyan-400 neon mb-4"></i>

<h4 class="text-xl font-semibold text-white mb-2">Chatbot</h4>

<p class="text-gray-300 mb-4">Interact with our AI for instant support and insights.</p>

<a href="chatbot.html" class="inline-block px-4 py-2 bg-cyan-500 text-black font-semibold rounded hover:bg-cyan-400 transition">

Launch Chatbot

</a>

</div>

</div>

</div>

</section>


<!-- Contact -->

<section id="contact" class="py-20 section-bg">

<div class="max-w-3xl mx-auto text-center px-6">

<h3 class="text-3xl md:text-4xl font-bold text-cyan-400 neon mb-4">Contact & Support</h3>

<p class="text-gray-300 mb-6">

Have questions or need assistance? Fill out the form below and we'll get back to you.

</p>

<form action="https://formspree.io/f/yourFormID" method="POST" class="space-y-4">

<input type="text" name="name" placeholder="Your Name" required class="w-full px-4 py-2 rounded bg-gray-700 border border-gray-600 focus:ring-cyan-400 text-white" />

<input type="email" name="email" placeholder="Your Email" required class="w-full px-4 py-2 rounded bg-gray-700 border border-gray-600 focus:ring-cyan-400 text-white" />

<textarea name="message" rows="4" placeholder="Your Message" required class="w-full px-4 py-2 rounded bg-gray-700 border border-gray-600 focus:ring-cyan-400 text-white"></textarea>

<button type="submit" class="w-full py-3 bg-gradient-to-r from-cyan-400 to-blue-500 text-black font-bold rounded-full hover:scale-105 transition">

Send Message

</button>

</form>

</div>

</section>

</main>


<!-- Footer -->

<footer class="bg-black/40 text-center text-gray-400 py-6">

<div class="container mx-auto px-6">

<p>&copy; 2025 Abinetic AI. All rights reserved.</p>

<p>Student: Abin Ajan Mathew (ID: 35573777)</p>

</div>

</footer>


<script>

particlesJS.load('particles-js', 'https://cdn.jsdelivr.net/gh/VincentGarreau/particles.js/particles.json', () => {});

document.getElementById('nav-toggle').addEventListener('click', () => {

document.getElementById('nav-menu').classList.toggle('hidden');

});

</script>

</body>

</html>


To access the tools section:

Tool 1: 

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8" />

<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Abinetic AI Chatbot</title>


<!-- Tailwind CSS -->

<script src="https://cdn.tailwindcss.com"></script>


<!-- Font and Styling -->

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">

<style>

body {

font-family: 'Inter', sans-serif;

background-color: #0f172a;

color: #ffffff;

}

</style>

</head>

<body class="min-h-screen flex flex-col">


<!-- Header -->

<header class="bg-black/70 px-6 py-4 shadow-md flex justify-between items-center">

<h1 class="text-2xl font-bold text-cyan-400">Abinetic Chatbot</h1>

<a href="dashboard.html" class="text-cyan-300 hover:underline">← Back to Dashboard</a>

</header>


<!-- Main Content -->

<main class="flex-grow p-6 flex justify-center items-center">

<div class="bg-black/40 border border-cyan-500 rounded-xl w-full max-w-3xl p-6">

<h2 class="text-2xl font-semibold text-cyan-300 mb-4">Ask me anything!</h2>


<!-- Chat Window -->

<div class="bg-gray-900 p-4 rounded-lg h-64 overflow-y-auto mb-4" id="chat-window">

<div class="text-gray-400 text-sm">🤖 Hello! I'm Abinetic AI. How can I help you today?</div>

</div>


<!-- Input -->

<form id="chat-form" class="flex">

<input id="user-input" type="text" placeholder="Type your message..." required

class="flex-grow px-4 py-2 bg-gray-800 border border-gray-600 rounded-l focus:outline-none text-white">

<button type="submit"

class="px-6 py-2 bg-cyan-500 text-black font-semibold rounded-r hover:bg-cyan-400 transition">

Send

</button>

</form>

</div>

</main>


<!-- Footer -->

<footer class="bg-black/80 text-center text-gray-400 py-4">

<p>&copy; 2025 Abinetic AI. Powered by GPT. Student: Abin Ajan Mathew</p>

</footer>


<!-- Basic Chatbot JS -->

<script>

const form = document.getElementById('chat-form');

const input = document.getElementById('user-input');

const chatWindow = document.getElementById('chat-window');


form.addEventListener('submit', function (e) {

e.preventDefault();

const userMsg = input.value.trim();

if (!userMsg) return;


// Append user message

chatWindow.innerHTML += `<div class="text-right text-cyan-300 mb-2">You: ${userMsg}</div>`;


// Simulate AI response

setTimeout(() => {

const response = "I'm just a demo. The real AI engine will be integrated soon!";

chatWindow.innerHTML += `<div class="text-left text-gray-400 mb-2">🤖 ${response}</div>`;

chatWindow.scrollTop = chatWindow.scrollHeight;

}, 500);


input.value = '';

chatWindow.scrollTop = chatWindow.scrollHeight;

});

</script>

</body>

</html>


Tool 2

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8" />

<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Model Trainer | Abinetic AI</title>


<!-- Tailwind CSS -->

<script src="https://cdn.tailwindcss.com"></script>


<!-- Font and Styling -->

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">

<style>

body {

font-family: 'Inter', sans-serif;

background-color: #0f172a;

color: #ffffff;

}

</style>

</head>

<body class="min-h-screen flex flex-col">


<!-- Header -->

<header class="bg-black/70 px-6 py-4 shadow-md flex justify-between items-center">

<h1 class="text-2xl font-bold text-cyan-400">Model Trainer</h1>

<a href="dashboard.html" class="text-cyan-300 hover:underline">← Back to Dashboard</a>

</header>


<!-- Main Content -->

<main class="flex-grow p-6 flex justify-center items-center">

<div class="bg-black/40 border border-cyan-500 rounded-xl w-full max-w-3xl p-6">

<h2 class="text-2xl font-semibold text-cyan-300 mb-4">Upload your dataset and train a model</h2>


<form id="train-form" class="space-y-4">

<input type="file" class="w-full bg-gray-800 border border-gray-600 text-white p-2 rounded" required />


<select class="w-full bg-gray-800 border border-gray-600 text-white p-2 rounded">

<option>Linear Regression</option>

<option>Random Forest</option>

<option>Logistic Regression</option>

</select>


<input type="number" placeholder="Epochs (e.g. 10)" class="w-full bg-gray-800 border border-gray-600 text-white p-2 rounded" />


<button type="submit" class="w-full bg-cyan-500 text-black font-semibold py-2 rounded hover:bg-cyan-400 transition">

Train Model

</button>

</form>


<div id="train-result" class="mt-6 text-cyan-300 hidden">

✅ Model trained successfully! Accuracy: <strong>91.2%</strong>

</div>

</div>

</main>


<!-- Footer -->

<footer class="bg-black/80 text-center text-gray-400 py-4">

<p>&copy; 2025 Abinetic AI. Powered by GPT. Student: Abin Ajan Mathew</p>

</footer>


<!-- JS -->

<script>

document.getElementById('train-form').addEventListener('submit', function (e) {

e.preventDefault();

setTimeout(() => {

document.getElementById('train-result').classList.remove('hidden');

}, 800);

});

</script>

</body>

</html>









Tool 3

<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8" />

<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<title>Abinetic Data Analyzer</title>


<!-- Google Fonts -->

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet" />


<!-- Tailwind CSS -->

<script src="https://cdn.tailwindcss.com"></script>


<!-- FontAwesome -->

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">


<style>

body {

font-family: 'Inter', sans-serif;

background-color: #0f172a;

color: #ffffff;

}

.neon {

text-shadow: 0 0 8px #22d3ee, 0 0 16px #0ea5e9;

}

.section-bg {

background-color: rgba(15, 23, 42, 0.85);

backdrop-filter: blur(6px);

}

</style>

</head>

<body class="min-h-screen flex flex-col justify-between">


<header class="bg-black/40 backdrop-blur-md p-6 shadow-md">

<div class="max-w-6xl mx-auto flex justify-between items-center">

<h1 class="text-2xl font-bold text-cyan-400 neon">Abinetic AI</h1>

<nav class="space-x-6 hidden md:flex">

<a href="index.html" class="hover:text-cyan-300">Home</a>

<a href="#features" class="hover:text-cyan-300">Features</a>

<a href="#upload" class="hover:text-cyan-300">Upload</a>

<a href="#output" class="hover:text-cyan-300">Output</a>

</nav>

</div>

</header>


<main class="flex-grow">

<section class="py-16 text-center px-6">

<h2 class="text-4xl font-bold text-cyan-400 neon mb-4">Data Analyzer</h2>

<p class="text-lg text-gray-300 max-w-2xl mx-auto">

Upload your CSV data and get quick insights like statistics, column analysis, and basic summaries.

</p>

</section>


<!-- Upload Section -->

<section id="upload" class="py-12 section-bg px-6">

<div class="max-w-xl mx-auto text-center">

<h3 class="text-2xl font-semibold text-cyan-300 mb-4">Upload CSV File</h3>

<form id="data-form">

<input type="file" accept=".csv" class="mb-4 w-full p-2 text-black rounded" required />

<button type="submit" class="w-full py-3 bg-cyan-400 text-black font-bold rounded hover:bg-cyan-300 transition">Analyze</button>

</form>

</div>

</section>


<!-- Output Section -->

<section id="output" class="py-12 px-6">

<div class="max-w-4xl mx-auto">

<h3 class="text-2xl font-semibold text-cyan-300 mb-6 text-center">Analysis Output</h3>

<div id="results" class="bg-gray-800 p-6 rounded shadow text-gray-100 min-h-[150px]">

<p class="text-gray-400 italic">Upload a CSV file to see results here...</p>

</div>

</div>

</section>

</main>


<footer class="bg-black/40 text-center py-6 text-gray-400">

<p>&copy; 2025 Abinetic AI | Tool 3 – Data Analyzer</p>

<p>Student: Abin Ajan Mathew (ID: 35573777)</p>

</footer>


<!-- Script -->

<script>

document.getElementById('data-form').addEventListener('submit', function(e) {

e.preventDefault();

const fileInput = e.target.querySelector('input[type="file"]');

const file = fileInput.files[0];


if (!file || !file.name.endsWith('.csv')) {

alert("Please upload a valid CSV file.");

return;

}


const reader = new FileReader();

reader.onload = function(e) {

const text = e.target.result;

const lines = text.split('\n');

const headers = lines[0].split(',');

const rowCount = lines.length - 1;

const colCount = headers.length;


const resultHTML = `

<p><strong>File Name:</strong> ${file.name}</p>

<p><strong>Rows:</strong> ${rowCount}</p>

<p><strong>Columns:</strong> ${colCount}</p>

<p><strong>Columns Detected:</strong> ${headers.join(', ')}</p>

`;

document.getElementById('results').innerHTML = resultHTML;

};

reader.readAsText(file);

});

</script>


</body>

</html>

Summary

This documentation and its associated files are part of the Abinetic AI server project developed for ICT171. The project demonstrates skills in Linux server configuration, DNS management, and scripting. All setup files and code are maintained in a structured format for future replication or troubleshooting.


