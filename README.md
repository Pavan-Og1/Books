# Books
Best books for improving life style
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BookX Store</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

body {
  background: #0f172a;
  color: white;
}

/* HEADER */
header {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background: #020617;
}

.logo {
  color: #38bdf8;
}

nav a {
  margin-left: 15px;
  color: white;
  text-decoration: none;
}

/* HERO */
.hero {
  height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: linear-gradient(135deg, #1e293b, #020617);
}

.hero h2 {
  font-size: 35px;
  animation: fadeIn 1.5s ease;
}

.hero p {
  margin: 15px 0;
}

.hero button {
  padding: 10px 20px;
  border: none;
  background: #38bdf8;
  color: black;
  cursor: pointer;
  border-radius: 5px;
  transition: 0.3s;
}

.hero button:hover {
  transform: scale(1.1);
}

/* BOOKS */
.books {
  padding: 40px;
  text-align: center;
}

.book-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.book-card {
  background: #1e293b;
  padding: 15px;
  border-radius: 10px;
  width: 200px;
  opacity: 0;
  transform: translateY(50px);
  transition: 0.6s;
}

.book-card img {
  width: 100%;
}

.book-card:hover {
  transform: translateY(-10px);
}

.book-card button {
  margin-top: 10px;
  padding: 8px;
  border: none;
  background: #38bdf8;
  cursor: pointer;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 20px;
  background: #020617;
}

/* ANIMATION */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
</head>

<body>

<header>
  <h1 class="logo">📚 BookX</h1>
  <nav>
    <a href="#">Home</a>
    <a href="#books">Books</a>
  </nav>
</header>

<section class="hero">
  <div>
    <h2>Sell Books Like a Pro</h2>
    <p>Knowledge • Money • Success</p>
    <button onclick="scrollToBooks()">Shop Now</button>
  </div>
</section>

<section id="books" class="books">
  <h2>Popular Books</h2>

  <div class="book-container">

    <div class="book-card">
      <img src="https://via.placeholder.com/200x300">
      <h3>Rich Mindset</h3>
      <p>₹299</p>
      <button>Buy</button>
    </div>

    <div class="book-card">
      <img src="https://via.placeholder.com/200x300">
      <h3>Stock Market Guide</h3>
      <p>₹399</p>
      <button>Buy</button>
    </div>

    <div class="book-card">
      <img src="https://via.placeholder.com/200x300">
      <h3>Success Blueprint</h3>
      <p>₹349</p>
      <button>Buy</button>
    </div>

  </div>
</section>

<footer>
  <p>© 2026 BookX</p>
</footer>

<script>
function scrollToBooks() {
  document.getElementById("books").scrollIntoView({ behavior: "smooth" });
}

window.addEventListener("scroll", () => {
  const cards = document.querySelectorAll(".book-card");

  cards.forEach(card => {
    const position = card.getBoundingClientRect().top;
    const screenHeight = window.innerHeight;

    if (position < screenHeight - 50) {
      card.style.opacity = 1;
      card.style.transform = "translateY(0)";
    }
  });
});
</script>

</body>
</html>
