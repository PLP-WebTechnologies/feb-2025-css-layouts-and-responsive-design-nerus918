# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox and Grid</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Navigation Bar -->
  <header>
    <nav>
      <div class="logo">MyWebsite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Main Content -->
  <main>
    <section class="hero">
      <h1>Welcome to My Website</h1>
      <p>Your journey to success starts here.</p>
      <button>Get Started</button>
    </section>

    <section class="features">
      <div class="feature">
        <h2>Feature 1</h2>
        <p>Description of feature 1.</p>
      </div>
      <div class="feature">
        <h2>Feature 2</h2>
        <p>Description of feature 2.</p>
      </div>
      <div class="feature">
        <h2>Feature 3</h2>
        <p>Description of feature 3.</p>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MyWebsite. All rights reserved.</p>
  </footer>

</body>
</html>
/* General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f5f5f5;
}

/* Navigation Bar */
header {
  background-color: #333;
  color: white;
  padding: 1rem;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
}

.nav-links {
  display: flex;
  list-style-type: none;
}

.nav-links li {
  margin-left: 1.5rem;
}

.nav-links li a {
  color: white;
  text-decoration: none;
  font-size: 1.1rem;
}

.nav-links li a:hover {
  text-decoration: underline;
}

/* Main Content */
main {
  padding: 2rem;
}

/* Hero Section */
.hero {
  background-color: #007bff;
  color: white;
  text-align: center;
  padding: 4rem;
  border-radius: 8px;
  margin-bottom: 2rem;
}

.hero h1 {
  font-size: 2.5rem;
}

.hero p {
  font-size: 1.2rem;
  margin: 1rem 0;
}

button {
  padding: 1rem 2rem;
  font-size: 1rem;
  background-color: #f1f1f1;
  color: #333;
  border: none;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background-color: #ddd;
}

/* Features Section using CSS Grid */
.features {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 2rem;
}

.feature {
  background-color: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.feature h2 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.feature p {
  font-size: 1rem;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}

/* Media Queries for Responsiveness */

/* Tablet (max-width: 1024px) */
@media (max-width: 1024px) {
  .nav-links {
    flex-direction: row;
  }

  .hero h1 {
    font-size: 2rem;
  }

  .features {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Mobile (max-width: 768px) */
@media (max-width: 768px) {
  header {
    padding: 1rem;
  }

  nav {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    margin-top: 1rem;
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links li {
    margin-left: 0;
    margin-bottom: 0.5rem;
  }

  .hero h1 {
    font-size: 1.8rem;
  }

  .hero p {
    font-size: 1rem;
  }

  .features {
    grid-template-columns: 1fr;
  }
}

/* Small Mobile (max-width: 480px) */
@media (max-width: 480px) {
  .hero {
    padding: 2rem 1rem;
  }

  button {
    width: 100%;
    padding: 1rem;
  }

  footer {
    font-size: 0.9rem;
  }
}

