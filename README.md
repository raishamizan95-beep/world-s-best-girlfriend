<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You 💚</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Quicksand', sans-serif;
    background: #f8e8ee;
    color: #333;
    overflow-x: hidden;
}

/* Hero Section */
.hero {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    text-align: center;
    padding: 20px;
    background: linear-gradient(to bottom, #f8e8ee, #dbe7c9);
}

/* Section Styling */
.section {
    opacity: 0;
    transform: translateY(50px);
    transition: all 1s ease;
    padding: 80px 20px;
    text-align: center;
}

.section.show {
    opacity: 1;
    transform: translateY(0);
}

.card {
    background: #fff;
    padding: 30px;
    margin: 20px auto;
    max-width: 400px;
    border-radius: 20px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    font-size: 20px;
}

/* Cute decorations */
.icon {
    font-size: 40px;
    margin: 10px;
}

/* Colors */
.pink {
    color: #ff6f91;
}

.green {
    color: #6b8e23;
}
</style>
</head>

<body>

<!-- FIRST SCREEN -->
<div class="hero">
    <p>
        i know you tak banyak menang anugerah but this is some of the anugerah yang you deserve:
    </p>
</div>

<!-- AWARDS -->
<div class="section">
    <div class="card pink">💖 best/amazing girlfriend ever</div>
</div>

<div class="section">
    <div class="card">🌸 the most beautiful girlfriend</div>
</div>

<div class="section">
    <div class="card green">🎧 the best listener</div>
</div>

<div class="section">
    <div class="card">🌿 the greatest provider</div>
</div>

<!-- Decorations -->
<div class="section">
    <div class="icon">🎸</div>
    <div class="icon">🥁</div>
    <div class="icon">🎤</div>
    <p class="pink">you are my favorite song 💕</p>
</div>

<!-- FINAL -->
<div class="section">
    <h2 class="green">thank you for everything 💚</h2>
</div>

<script>
// Scroll animation
const sections = document.querySelectorAll('.section');

window.addEventListener('scroll', () => {
    sections.forEach(section => {
        const position = section.getBoundingClientRect().top;
        const screenHeight = window.innerHeight;

        if(position < screenHeight - 100){
            section.classList.add('show');
        }
    });
});
</script>

</body>
</html>
