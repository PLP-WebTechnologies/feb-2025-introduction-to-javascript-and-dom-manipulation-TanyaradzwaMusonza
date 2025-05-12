# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive Page</title>
  <link rel="stylesheet" href="style.css" />
  <script defer src="script.js"></script>
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to My Interactive Page</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projects</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <p id="info-text">Click the buttons below to interact with this content.</p>
      <button id="change-text">Change Text</button>
      <button id="change-style">Change Style</button>
      <button id="toggle-element">Toggle Element</button>
    </section>

    <aside id="extra-box">
      <p>This box can be hidden or shown.</p>
    </aside>
  </main>

  <footer>
    <p>&copy; 2025 MySite</p>
  </footer>
</body>
</html>
// Change text content
document.getElementById('change-text').addEventListener('click', () => {
  document.getElementById('info-text').textContent = "The text has been changed dynamically!";
});

// Modify CSS styles
document.getElementById('change-style').addEventListener('click', () => {
  const title = document.getElementById('main-title');
  title.style.color = 'darkred';
  title.style.fontSize = '2.5em';
  title.style.textAlign = 'center';
});

// Add/Remove an element
document.getElementById('toggle-element').addEventListener('click', () => {
  const box = document.getElementById('extra-box');
  if (box.style.display === 'none') {
    box.style.display = 'block';
  } else {
    box.style.display = 'none';
  }
});

