<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>lavi（らゔぃ）</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Kiwi+Maru&display=swap" rel="stylesheet">
</head>
<body>
  <header>
    <h1 class="logo">らゔぃ</h1>
    <nav>
      <ul class="menu">
<nav>
  <ul class="menu">
    <li><a href="#">トップ</a></li>
    <li><a href="#">商品一覧</a></li>
    <li><a href="#">ブランドについて</a></li>
    <li><a href="#">お問い合わせ</a></li>
    <li><a href="#">カート</a></li>
  </ul>
</nav>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero">
      <img src="your-image.jpg" alt="フィルム風トップ画像" />
      <p class="catch">ふるいのに、新しい。</p>
    </section>

    <section class="social">
      <h2>れんけいSNS</h2>
      <!-- Instagram埋め込み or TikTokリンクなど -->
      <div class="insta-placeholder">Instagram表示スペース</div>
      <div class="tiktok-placeholder">TikTok表示スペース</div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 lavi. All rights reserved.</p>
  </footer>
</body>
</html>
body {
  margin: 0;
  font-family: 'Kiwi Maru', serif;
  background-color: #fff;
  color: #222;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  border-bottom: 1px solid #ccc;
}

.logo {
  font-size: 2rem;
  letter-spacing: 0.1em;
}

.menu {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}

.menu a {
  text-decoration: none;
  color: #222;
  font-weight: bold;
  font-size: 1rem;
}

.hero {
  text-align: center;
  padding: 2rem 1rem;
}

.hero img {
  width: 100%;
  max-height: 500px;
  object-fit: cover;
  filter: grayscale(100%) contrast(90%) brightness(95%);
}

.catch {
  font-size: 1.5rem;
  margin-top: 1rem;
  font-weight: bold;
}

.social {
  padding: 2rem;
  text-align: center;
}

footer {
  text-align: center;
  padding: 1rem;
  background-color: #f5f5f5;
  font-size: 0.9rem;
  color: #666;
}
<section class="fade-in-target">
  <h2>おすすめ商品</h2>
  <p>古着の魅力、ぎゅっと詰まってます。</p>
</section>

<section class="fade-in-target">
  <img src="film-photo.jpg" alt="フィルム風画像" />
</section>
.fade-in-target {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s ease-out;
}

.fade-in-target.active {
  opacity: 1;
  transform: translateY(0);
}
<script>
  const fadeElements = document.querySelectorAll('.fade-in-target');

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('active');
      }
    });
  }, {
    threshold: 0.1
  });

  fadeElements.forEach(el => observer.observe(el));
</script>
