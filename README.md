<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For You 💌</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="hero">
  <h1>scroll down slowly 🌸</h1>
</div>

<section class="hidden">
  <h2>
    i know you tak banyak menang anugerah but this is some of the anugerah yang you deserve:
  </h2>
</section>

<section class="hidden award">
  <p>🏆 best/amazing girlfriend ever</p>
</section>

<section class="hidden award">
  <p>🌷 the most beautiful girlfriend</p>
</section>

<section class="hidden award">
  <p>🎧 the best listener</p>
</section>

<section class="hidden award">
  <p>🎸 the greatest provider</p>
</section>

<section class="hidden">
  <img src="img/her.jpg" class="photo">
</section>

<div class="decorations">
  🎸 🎤 🥁 🎶 🎸 🎤 🥁
</div>

<script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  font-family: 'Courier New', monospace;
  background: #fff7f9;
  color: #333;
  text-align: center;
}

.hero {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 24px;
}

section {
  margin: 100px 20px;
  font-size: 20px;
}

.award {
  background: #ffe4ec;
  padding: 20px;
  border-radius: 20px;
  width: fit-content;
  margin: 40px auto;
}

.photo {
  width: 250px;
  border-radius: 20px;
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

.decorations {
  font-size: 30px;
  margin: 100px 0;
}

/* animation */
.hidden {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.8s ease;
}

.show {
  opacity: 1;
  transform: translateY(0);
}
const hiddenElements = document.querySelectorAll('.hidden');

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('show');
    }
  });
});

hiddenElements.forEach(el => observer.observe(el));
