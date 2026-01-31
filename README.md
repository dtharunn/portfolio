<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Tharun | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
* {
  box-sizing: border-box;
  scroll-behavior: smooth;
}
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: all 0.8s ease;
}
.reveal.active {
  opacity: 1;
  transform: translateY(0);
}
.cursor {
  font-weight: bold;
  animation: blink 1s infinite;
}
@keyframes blink {
  0%, 50%, 100% { opacity: 1; }
  25%, 75% { opacity: 0; }
}
body {
  margin: 0;
  font-family: "Segoe UI", Arial, sans-serif;
  background: #0f172a;
  color: #e5e7eb;
}
body.light {
  background: #f4f6fb;
  color: #111827;
}
header {
  background: linear-gradient(135deg, #2563eb, #7c3aed);
  color: white;
  padding: 70px 20px;
  text-align: center;
  position: relative;
}
body.light header {
  background: linear-gradient(135deg, #3b82f6, #a78bfa);
}
.toggle-btn {
  position: absolute;
  top: 20px;
  right: 20px;
  padding: 10px 16px;
  border-radius: 20px;
  border: none;
  cursor: pointer;
  background: rgba(255,255,255,0.2);
  color: white;
}
body.light .toggle-btn {
  background: white;
  color: #111;
}
section {
  background: #111827;
  margin: 25px;
  padding: 35px;
  border-radius: 16px;
  border: 1px solid #1f2937;
  box-shadow: 0 12px 30px rgba(0,0,0,0.3);
}
body.light section {
  background: white;
  border: 1px solid #e5e7eb;
}
h2 {
  color: #60a5fa;
}
body.light h2 {
  color: #2563eb;
}
h4 {
  color: #34d399;
}
body.light h4 {
  color: #059669;
}
.tag {
  display: inline-block;
  padding: 8px 16px;
  border-radius: 20px;
  margin: 6px 6px 0 0;
  background: #1e293b;
  color: #93c5fd;
  border: 1px solid #334155;
}
.tag:hover {
  background: #2563eb;
  color: white;
  transform: translateY(-3px);
}
.github-btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 14px 28px;
  border-radius: 999px;
  text-decoration: none;
  background: linear-gradient(135deg, #111827, #1f2937);
  color: white;
}
.github-btn:hover {
  transform: translateY(-4px);
}
footer {
  text-align: center;
  padding: 20px;
  font-size: 14px;
  opacity: 0.8;
}
a {
  color: #60a5fa;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>
</head>
<body>
<header>
  <button class="toggle-btn" onclick="toggleTheme()">🌙 Mode</button>
  <h1>Hi, I'm Tharun 👋</h1>
  <p><span id="typing"></span><span class="cursor">|</span></p>
</header>
<section class="reveal">
  <h2>About Me</h2>
  <p>
    I have completed my 12th standard and I am passionate about learning programming and web development.
    I enjoy solving problems logically and improving my skills through consistent practice and self-learning.
    I am eager to explore new technologies and build simple, useful projects.
  </p>
</section>
<section class="reveal">
  <h2>Education</h2>
  <h4>🎓 Higher Secondary (12th Standard)</h4>
  <p>
    Completed 12th Standard<br>
    Developed interest in computers, logic, and problem solving.
  </p>
  <h4>📘 Self Learning</h4>
  <ul>
    <li>HTML, CSS & JavaScript fundamentals</li>
    <li>Python basics</li>
    <li>Logical and practice-based programs</li>
    <li>Mini web projects</li>
  </ul>
</section>
<section class="reveal">
  <h2>Skills</h2>
  <div class="tag">HTML</div>
  <div class="tag">CSS</div>
  <div class="tag">JavaScript (Basics)</div>
  <div class="tag">Python (Basics)</div>
  <div class="tag">Problem Solving</div>
</section>
<section class="reveal">
  <h2>Currently Learning</h2>
  <div class="tag">Advanced JavaScript</div>
  <div class="tag">C++</div>
  <div class="tag">PHP</div>
</section>
<section class="reveal">
  <h2>Projects</h2>
  <h4>✔ Personal Portfolio Website</h4>
  <p>
    A responsive personal portfolio built using HTML, CSS, and JavaScript.
    Includes animations and dark/light mode.
  </p>
  <p>
    🌐 Live:
    <a href="https://tharunportfolio.dtharun-official.workers.dev/" target="_blank">
      View Website
    </a>
  </p>
  <h4>✔ Practice Projects</h4>
  <ul>
    <li>JavaScript logic programs</li>
    <li>Loop and condition-based exercises</li>
    <li>Simple calculator programs</li>
    <li>Basic web pages</li>
  </ul>
</section>
<section class="reveal">
  <h2>GitHub</h2>
  <a class="github-btn" href="https://github.com/dtharunn" target="_blank">
    Visit My GitHub
  </a>
</section>
<section class="reveal">
  <h2>Contact</h2>
  <p>Email: <a href="mailto:dtharun.official@gmail.com">dtharun.official@gmail.com</a></p>
  <p>Location: Tamil Nadu, India</p>
</section>
<footer>
  © 2025 Tharun | Portfolio
</footer>
<script>
function toggleTheme() {
  document.body.classList.toggle("light");
}
const reveals = document.querySelectorAll(".reveal");
function revealOnScroll() {
  const height = window.innerHeight;
  reveals.forEach(el => {
    if (el.getBoundingClientRect().top < height - 100) {
      el.classList.add("active");
    }
  });
}
window.addEventListener("scroll", revealOnScroll);
revealOnScroll();
const texts = [
  "Aspiring Web Developer",
  "Self-Learner 🌱",
  "Problem Solver 🧠",
  "Learning Every Day 🚀"
];
let t = 0, c = 0;
const typing = document.getElementById("typing");
function type() {
  if (c < texts[t].length) {
    typing.textContent += texts[t][c++];
    setTimeout(type, 100);
  } else {
    setTimeout(erase, 1500);
  }
}
function erase() {
  if (c > 0) {
    typing.textContent = texts[t].substring(0, --c);
    setTimeout(erase, 60);
  } else {
    t = (t + 1) % texts.length;
    setTimeout(type, 200);
  }
}
type();
</script>
</body>
</html>
