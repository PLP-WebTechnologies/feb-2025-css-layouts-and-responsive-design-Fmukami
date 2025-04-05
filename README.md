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
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Flexbox Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content Section -->
  <section class="content">
    <div class="sidebar">
      <h2>Sidebar</h2>
      <p>Some sidebar content here.</p>
    </div>

    <div class="main">
      <h1>Welcome to the Flexbox Layout</h1>
      <p>This layout adjusts based on the screen size using Flexbox and media queries.</p>
    </div>

    <div class="sidebar">
      <h2>Another Sidebar</h2>
      <p>Additional content for the sidebar.</p>
    </div>
  </section>

  <footer class="footer">
    <p>&copy; 2025 Your Company</p>
  </footer>

</body>
</html>



/* Global Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body Styling */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
}

/* Navigation Bar */
.navbar {
  background-color: #333;
  padding: 10px 0;
}

.navbar ul {
  list-style: none;
  display: flex;
  justify-content: center;
}

.navbar ul li {
  margin: 0 20px;
}

.navbar ul li a {
  color: white;
  text-decoration: none;
  font-size: 18px;
}

.navbar ul li a:hover {
  color: #4CAF50;
}

/* Main Content Section */
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 20px;
}

/* Sidebar and Main Layout */
.sidebar {
  flex: 1;
  background-color: #f4f4f4;
  padding: 20px;
  margin: 10px;
  border-radius: 8px;
}

.main {
  flex: 2;
  background-color: white;
  padding: 20px;
  margin: 10px;
  border-radius: 8px;
}

/* Footer */
.footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px 0;
  margin-top: 20px;
}

/* Media Queries */

/* For Tablets (768px and up) */
@media (max-width: 768px) {
  .content {
    flex-direction: column;
  }

  .navbar ul {
    flex-direction: column;
    align-items: center;
  }

  .navbar ul li {
    margin: 10px 0;
  }
}

/* For Mobile (480px and up) */
@media (max-width: 480px) {
  .navbar ul {
    font-size: 16px;
  }

  .sidebar,
  .main {
    margin: 5px;
    padding: 15px;
  }
}
