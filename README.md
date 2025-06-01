<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>charity:water - Responsive & Animated</title>
  <style>
    html {
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Avenir', 'Proxima Nova', sans-serif;
      background: #f4f7f6;
      color: #333;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #FFC907;
      padding: 1.5rem;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }
    .logo { font-size: 2rem; font-weight: 700; color: #000; }
    nav a {
      margin: 0 1rem;
      color: #000;
      text-decoration: none;
      font-weight: 500;
    }
    .hero {
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1600596542812-4f3c02d55ba1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
      padding: 7rem 1.5rem;
      text-align: center;
      color: white;
      opacity: 0;
      transform: translateY(30px);
      transition: all 1s ease;
    }
    .section {
      padding: 5rem 1.5rem;
      max-width: 1200px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      transition: all 1s ease;
    }
    .about, .donate {
      background-color: #8BD1CB;
      border-radius: 15px;
      padding: 4rem 3rem;
      text-align: center;
      color: #000;
    }
    .gallery-section {
      text-align: center;
      margin-bottom: 2rem;
    }
    .gallery-section h2 {
      font-size: 2.5rem;
      margin-bottom: 2rem;
    }
    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      margin-top: 2rem;
    }
    .gallery-item {
      overflow: hidden;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .gallery-item img {
      width: 100%;
      max-width: 370px;
      transition: transform 0.5s ease;
      display: block;
    }
    .gallery-item:hover img {
      transform: scale(1.1);
    }
    .gallery-item:hover {
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }
    .donate button {
      margin-top: 2rem;
      padding: 1rem 2rem;
      font-size: 1.2rem;
      background-color: #F5402C;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .donate button:hover {
      background-color: #D9311C;
    }
    footer {
      background-color: #159A48;
      color: white;
      padding: 3rem 1rem;
      text-align: center;
      margin-top: 5rem;
    }
    @media(max-width: 768px) {
      .hero h1, .about h2, .gallery-section h2, .donate h2 {
        font-size: 2rem;
      }
      .gallery {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const sections = document.querySelectorAll('.section, .hero');
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = 1;
            entry.target.style.transform = 'translateY(0)';
          }
        });
      }, { threshold: 0.1 });
      sections.forEach(section => observer.observe(section));
    });
  </script>
</head>
<body>
  <header>
    <div class="logo">charity:water</div>
    <nav>
      <a href="#">Home</a>
      <a href="#projects">Projects</a>
      <a href="#donate">Donate</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Bring Clean Water to Communities</h1>
    <p>Join us in solving the global water crisis. Every drop counts, and you can make a difference today.</p>
  </section>

  <div class="section about">
    <h2>Why Water?</h2>
    <p>Clean water changes everything. It improves health, empowers women, boosts education, and transforms communities. Help us bring hope to millions by supporting sustainable clean water solutions worldwide.</p>
  </div>

  <div class="section gallery-section">
    <h2>Read about our Water Projects</h2>
    <div class="gallery">
      <div class="gallery-item">
        <img src="https://www.pushblack.us/sites/default/files/styles/article_feature_image/public/field/image/hydrationr.png?itok=h5rCRcWD" alt="Hydration Image">
      </div>
      <div class="gallery-item">
        <img src="https://images.squarespace-cdn.com/content/v1/5b43751b4611a0c5d193da69/1611674134039-062LSQL2GMU1ZDT3WNAW/COVER+STORY+%28HOME+%26+CLICK+THRU+TOP%29.jpg" alt="Cover Story Drinking Water">
      </div>
    </div>
  </div>

  <div class="section donate">
    <h2>Make a Donation</h2>
    <p>Your contribution helps us bring clean and safe drinking water to communities in need. Every dollar matters and brings hope to someone’s life.</p>
    <button>Donate Now</button>
  </div>

  <footer>
    <p>Contact us: info@charitywater.org | (123) 456-7890</p>
    <p>
      <a href="#">Facebook</a> |
      <a href="#">Twitter</a> |
      <a href="#">Instagram</a>
    </p>
  </footer>
</body>
</html>
