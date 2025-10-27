<!DOCTYPE html>
<html lang="mr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Books</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@600;800&display=swap');

:root {
--color-bg: #ffffff;
--color-text-primary: #111827;
--color-text-secondary: #4b5563;
--color-primary: #ef4444; /* vibrand warm red */
--color-primary-hover: #dc2626;
--color-accent1: #3b82f6; /* bright blue */
--color-accent1-hover: #2563eb;
--color-accent2: #10b981; /* teal */
--color-accent2-hover: #059669;
--color-card-bg-gradient: linear-gradient(135deg, #fef3c7, #fee2e2);
--color-card-bg-gradient-2: linear-gradient(135deg, #dbeafe, #bfdbfe);
--border-radius: 0.75rem;
--shadow-light: rgba(0, 0, 0, 0.07);
--transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
--max-width: 1200px;
}

/* Reset and base */
*, *::before, *::after {
box-sizing: border-box;
}
body {
margin: 0;
font-family: 'Poppins', sans-serif;
background: var(--color-bg);
color: var(--color-text-primary);
line-height: 1.5;
font-size: 18px;
min-height: 100vh;
display: flex;
flex-direction: column;
}
a {
text-decoration: none;
color: var(--color-text-primary);
transition: color var(--transition);
}
a:hover,
a:focus {
color: var(--color-primary-hover);
outline: none;
}

/* Container */
.container {
width: 90%;
max-width: var(--max-width);
margin-left: auto;
margin-right: auto;
}

/* Header */
header {
position: sticky;
top: 0;
background: var(--color-bg);
border-bottom: 1px solid #e5e7eb;
z-index: 1000;
box-shadow: 0 2px 6px var(--shadow-light);
}

nav {
display: flex;
justify-content: space-between;
align-items: center;
height: 64px;
padding: 0 1rem;
}

.logo {
font-weight: 800;
font-size: 1.5rem;
user-select: none;
color: var(--color-primary);
}

.nav-items {
display: flex;
gap: 1.5rem;
}

.nav-items a {
font-weight: 600;
font-size: 1rem;
padding: 0.25rem 0.75rem;
border-radius: var(--border-radius);
transition: background-color var(--transition), color var(--transition);
position: relative;
color: var(--color-text-primary);
}
.nav-items a::after {
content: "";
position: absolute;
bottom: 0;
left: 10%;
width: 80%;
height: 2px;
background: transparent;
transition: background-color var(--transition);
border-radius: 2px;
}
.nav-items a:hover,
.nav-items a:focus {
color: var(--color-primary);
outline: none;
}
.nav-items a:hover::after,
.nav-items a:focus::after {
background: var(--color-primary);
}

/* Hero Section */
.hero {
padding-top: 5rem;
padding-bottom: 5rem;
text-align: center;
user-select: none;
background: linear-gradient(135deg, var(--color-accent1), var(--color-accent2));
color: white;
clip-path: polygon(0 0, 100% 0, 100% 90%, 0% 100%);
}
.hero h1 {
font-weight: 800;
font-size: 3.5rem;
max-width: 700px;
margin-left: auto;
margin-right: auto;
margin-bottom: 1rem;
line-height: 1.1;
text-shadow: 0 3px 8px rgba(0,0,0,0.3);
}
@media (min-width: 768px) {
.hero h1 {
font-size: 4.75rem;
}
}
.hero p {
max-width: 520px;
margin-left: auto;
margin-right: auto;
font-weight: 600;
font-size: 1.25rem;
margin-bottom: 3rem;
text-shadow: 0 2px 6px rgba(0,0,0,0.25);
}
.btn-primary {
background-color: white;
color: var(--color-primary);
font-weight: 700;
font-size: 1.25rem;
padding: 1rem 3.25rem;
border: none;
border-radius: var(--border-radius);
cursor: pointer;
box-shadow: 0 10px 30px rgba(255 255 255 / 0.6);
transition: background-color var(--transition), transform 0.25s ease, color var(--transition);
user-select: none;
font-family: 'Poppins', sans-serif;
}
.btn-primary:hover,
.btn-primary:focus {
background-color: #f3f4f6;
color: var(--color-primary-hover);
transform: scale(1.05);
outline: none;
box-shadow: 0 12px 35px rgba(255 255 255 / 0.7);
}

/* Features Section */
section.features {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 2.5rem;
padding-top: 6rem;
padding-bottom: 6rem;
max-width: var(--max-width);
margin-left: auto;
margin-right: auto;
}

.card {
background: var(--color-bg);
border-radius: var(--border-radius);
padding: 2rem;
box-shadow: 0 8px 20px var(--shadow-light);
transition: box-shadow var(--transition), transform var(--transition);
display: flex;
flex-direction: column;
user-select: none;
border: 3px solid transparent;
}
/* Colorful gradient backgrounds for cards */
.card:nth-child(odd) {
background: var(--color-card-bg-gradient);
border-image: linear-gradient(135deg, var(--color-primary), var(--color-accent2)) 1;
}
.card:nth-child(even) {
background: var(--color-card-bg-gradient-2);
border-image: linear-gradient(135deg, var(--color-accent1), var(--color-primary)) 1;
}
.card:hover,
.card:focus-within {
box-shadow: 0 15px 40px rgba(0,0,0,0.15);
transform: translateY(-8px);
outline: none;
border-color: var(--color-primary);
}
.card h2 {
margin-top: 0;
margin-bottom: 1rem;
font-weight: 800;
font-size: 1.6rem;
color: var(--color-primary);
text-shadow: 0 1px 2px rgba(0,0,0,0.1);
}
.card p {
flex-grow: 1;
font-weight: 600;
color: var(--color-text-primary);
font-size: 1rem;
line-height: 1.6;
}
.price {
font-size: 2.25rem;
font-weight: 900;
margin-top: 1.75rem;
color: var(--color-primary);
user-select: text;
text-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

/* Additional Sections */
section.about,
section.contact {
padding-top: 6rem;
padding-bottom: 6rem;
text-align: center;
max-width: var(--max-width);
margin-left: auto;
margin-right: auto;
user-select: none;
}
section.about h2,
section.contact h2 {
font-weight: 800;
font-size: 2.25rem;
margin-bottom: 1rem;
color: var(--color-primary);
letter-spacing: 0.02em;
text-shadow: 0 1px 2px rgba(0,0,0,0.1);
}
section.about p,
section.contact p {
max-width: 620px;
margin-left: auto;
margin-right: auto;
font-size: 1.1rem;
font-weight: 600;
color: var(--color-text-primary);
line-height: 1.7;
}
section.contact p.email {
font-weight: 800;
color: var(--color-primary);
margin-top: 1rem;
font-size: 1.25rem;
user-select: text;
letter-spacing: 0.03em;
}

/* Footer */
footer {
text-align: center;
padding: 2rem 1rem;
font-size: 0.9rem;
color: var(--color-text-secondary);
border-top: 1px solid #e5e7eb;
user-select: none;
font-weight: 600;
background: #f9fafb;
letter-spacing: 0.02em;
}

/* Responsive Hero text scaling */
@media (max-width: 480px) {
.hero h1 {
font-size: 2.75rem;
}
.hero p {
font-size: 1.125rem;
}
.btn-primary {
font-size: 1.125rem;
padding: 0.85rem 2.25rem;
}
}
</style>
</head>
<body>
<header>
<nav class="container" aria-label="मुख्य नेव्हिगेशन">
<div class="logo" tabindex="0">FREE PDF BOOKS</div>
<div class="nav-items">
<a href="index.html" tabindex="0">Home</a>
<a href="Nabout.html" tabindex="0">About</a>
<a href="NContact.html" tabindex="0">Contact</a>
</div>
</nav>
</header>

<main>
<section class="hero" id="home" role="banner" aria-label="PDF पुस्तक विक्री परिचय">
<h1>Download Free Books</h1>
<p>डिजिटल स्वरूपात सुलभ वाचनासाठी प्रीमियम PDF पुस्तक मिळवा. शिक्षणाला गती द्या, आजच गेट करा!</p>
<button class="btn-primary" id="buyBtn" aria-label="पुस्तक खरेदी करा">आता खरेदी करा</button>
</section>

<section class="features" aria-label="पुस्तक वैशिष्ट्ये">

<article class="card" tabindex="0" aria-labelledby="productTitle">
  <h2 id="productTitle">"Rich Dad Poor Dad"</h2>

  <img src="IMG_20250608_122345.JPG" alt="JavaScript PDF पुस्तक" style="max-width: 100%; border-radius: 12px; margin-bottom: 1rem;" />

  <p>JavaScript</p>
  <div class="price" aria-label="किंमत">₹299</div>

  <a href="Rich Dad Poor Dad ( PDFDrive ).pdf" download class="btn-primary" style="margin-top: 1rem; display: inline-block;">
    PDF डाउनलोड करा
  </a>
</article>

<article class="card" tabindex="0" aria-labelledby="productTitle">
  <h2 id="productTitle">"Rich Dad Poor Dad"</h2>

  <img src="IMG_20250608_122345.JPG" alt="JavaScript PDF पुस्तक" style="max-width: 100%; border-radius: 12px; margin-bottom: 1rem;" />

  <p>JavaScript</p>
  <div class="price" aria-label="किंमत">₹299</div>

  <a href="Rich Dad Poor Dad ( PDFDrive ).pdf" download class="btn-primary" style="margin-top: 1rem; display: inline-block;">
    PDF डाउनलोड करा
  </a>
</article>

<article class="card" tabindex="0" aria-labelledby="featuresTitle">
<h2 id="featuresTitle">मुख्य वैशिष्ट्ये</h2>
<p>• पूर्ण डिजिटल PDF<br>• सोपे आणि प्रभावी उदाहरणे<br>• कोणत्याही उपकरणावर वाचनासाठी उपयुक्त<br>• आत्म-अभ्यासासाठी उत्तम सामग्री</p>
</article>

<article class="card" tabindex="0" aria-labelledby="secureTitle">
<h2 id="secureTitle">सुरक्षित खरेदी</h2>
<p>विविध सुरक्षित पेमेंट पर्याय उपलब्ध आहेत. तुमच्या माहितीची गोपनीयता आमच्यासाठी महत्त्वाची आहे.</p>
</article>
</section>

<section class="about" id="about" aria-label="आमच्याबद्दल">
<h2>आमच्याबद्दल</h2>
<p>आम्ही दर्जेदार PDF पुस्तके विक्री करतो जे तुमच्या शिक्षणाला पुढे नेण्यासाठी उपयुक्त ठरतात. आमचा उद्देश्य तुमच्या ज्ञानाला अधिक सुलभ करणे आहे.</p>
</section>

<section class="contact" id="contact" aria-label="संपर्क करा">
<h2>संपर्क करा</h2>
<p>तुमचे प्रश्न किंवा सूचना असल्यास खाली दिलेल्या ईमेलवर संपर्क करा:</p>
<p class="email">email@example.com</p>
</section>
</main>

<footer>
© 2024 PDF पुस्तक विक्री. सर्व हक्क राखीव.
</footer>

<script>
document.getElementById('buyBtn').addEventListener('click', function() {
alert('तुमच्या खरेदीसाठी धन्यवाद! पुढील सूचना ईमेलवर पाठवण्यात येतील.');
});
</script>
</body>
</html>
