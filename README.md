<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Delicious Bites</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>Delicious Bites</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome to Delicious Bites</h2>
    <p>Serving joy on every plate. Explore our veg, non-veg, and dessert specialties!</p>
  </section>

  <section id="menu">
    <h2>Our Menu</h2>

    <h3 class="category">🌿 Veg Dishes</h3>
    <div class="menu-grid">
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?paneer" alt="Paneer Tikka" />
        <h4>Paneer Tikka</h4>
        <p>Grilled paneer with spicy marinade, served with mint chutney.</p>
      </div>
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?veg-biryani" alt="Veg Biryani" />
        <h4>Veg Biryani</h4>
        <p>Fragrant rice with mixed vegetables and aromatic spices.</p>
      </div>
    </div>

    <h3 class="category">🍗 Non-Veg Dishes</h3>
    <div class="menu-grid">
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?chicken-curry" alt="Chicken Curry" />
        <h4>Chicken Curry</h4>
        <p>Spicy chicken curry with rich tomato gravy.</p>
      </div>
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?grilled-fish" alt="Grilled Fish" />
        <h4>Grilled Fish</h4>
        <p>Fresh fish fillet grilled with lemon and herbs.</p>
      </div>
    </div>

    <h3 class="category">🍰 Desserts</h3>
    <div class="menu-grid">
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?cheesecake" alt="Cheesecake" />
        <h4>Cheesecake</h4>
        <p>Creamy cheesecake with a graham cracker crust.</p>
      </div>
      <div class="menu-item">
        <img src="https://source.unsplash.com/300x200/?gulab-jamun" alt="Gulab Jamun" />
        <h4>Gulab Jamun</h4>
        <p>Soft dumplings soaked in rose-flavored syrup.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <form id="contact-form">
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>&copy; 2025 Delicious Bites. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #fffaf0;
  color: #333;
}

header {
  background-color: #ff6347;
  color: white;
  padding: 1rem;
  text-align: center;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

nav ul li {
  margin: 0 1rem;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

section {
  padding: 2rem;
  max-width: 1000px;
  margin: auto;
}

.category {
  margin-top: 2rem;
  color: #d9534f;
}

.menu-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-top: 1rem;
}

.menu-item {
  background-color: #fff;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.2s ease;
}

.menu-item:hover {
  transform: scale(1.03);
}

.menu-item img {
  width: 100%;
  height: 160px;
  object-fit: cover;
}

.menu-item h4 {
  margin: 0.5rem;
}

.menu-item p {
  padding: 0 0.5rem 1rem;
  font-size: 0.95rem;
  color: #555;
}

form input, form textarea {
  width: 100%;
  margin: 0.5rem 0;
  padding: 0.75rem;
  border-radius: 5px;
  border: 1px solid #ccc;
}

form button {
  background-color: #ff6347;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 0.5rem;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1rem;
}

document.getElementById('contact-form').addEventListener('submit', function (e) {
  e.preventDefault();
  alert("Thank you for contacting Delicious Bites!");
  this.reset();
});
