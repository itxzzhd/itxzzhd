
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Self</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <div class="typing-container">
    <span id="typing-text"></span>
  </div>

  <div class="tech">
    <h1>
      <b>Hi,</b> I am <span class="efek-ngetik"></span>
    </h1>

    <p>
      <i>
        I truly interested and passionate about development and cyber security.<br>
        I love to learn new things and explore new technologies.
      </i>
    </p>
  </div>

  <script src="script.js"></script>
</body>
</html>

body {
  background-color: black;
  font-family: Arial, sans-serif;
  color: white;
  margin: 0;
  padding: 0;
}

.typing-container {
  text-align: center;
  font-size: 50px;
  font-weight: bold;
  margin-top: 40px;
  height: 80px;
}

#typing-text::after {
  content: "|";
  margin-left: 5px;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50%, 100% { opacity: 1; }
  25%, 75% { opacity: 0; }
}

.tech {
  text-align: center;
  margin-top: 40px;
}

.tech h1 {
  font-size: 32px;
}

.tech p {
  font-size: 16px;
  color: #dddddd;
}

.efek-ngetik {
  color: #00ffff;
}

const texts = ["Welcome", "સ્વાગત છે"];
let index = 0;
let charIndex = 0;
let isDeleting = false;
const speed = 100;
const delay = 1500;

const typingElement = document.getElementById("typing-text");

function typeEffect() {
  const currentText = texts[index];

  if (isDeleting) {
    typingElement.textContent = currentText.substring(0, charIndex--);
  } else {
    typingElement.textContent = currentText.substring(0, charIndex++);
  }

  if (!isDeleting && charIndex === currentText.length + 1) {
    setTimeout(() => isDeleting = true, delay);
  } else if (isDeleting && charIndex === 0) {
    isDeleting = false;
    index = (index + 1) % texts.length;
  }

  setTimeout(typeEffect, isDeleting ? speed / 2 : speed);
}

typeEffect();


