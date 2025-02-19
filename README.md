<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TravelBloom</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Navigation Bar -->
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About Us</a></li>
        <li><a href="contact.html">Contact Us</a></li>
      </ul>
    </nav>
  </header>

  <!-- Search Bar Section -->
  <section class="search-bar">
    <input type="text" id="searchInput" placeholder="Search destinations or keywords">
    <button id="searchButton">Search</button>
  </section>

  <!-- Content Section -->
  <section class="content">
    <div class="background-image">
      <h1>Explore the World with TravelBloom</h1>
      <p>Discover hidden gems, vibrant cultures, and breathtaking destinations.</p>
      <a href="book-now.html" class="book-now-btn">Book Now</a>
    </div>

    <!-- Social Media Links -->
    <div class="social-media">
      <a href="https://facebook.com" target="_blank">Facebook</a>
      <a href="https://twitter.com" target="_blank">Twitter</a>
      <a href="https://instagram.com" target="_blank">Instagram</a>
    </div>

    <!-- Dynamic Search Results Section -->
    <div id="searchResults"></div>
  </section>
<link rel="stylesheet" href="style.css">
  <script src="javascript"></script>
</body>
</html>
/* styles.css */

/* Basic reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  /* Body and background */
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  
  header {
    background-color: #333;
    padding: 10px 0;
    text-align: center;
  }
  
  nav ul {
    list-style-type: none;
  }
  
  nav ul li {
    display: inline;
    margin: 0 15px;
  }
  
  nav ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 16px;
  }
  
  .search-bar {
    text-align: center;
    padding: 20px 0;
  }
  
  .search-bar input {
    padding: 10px;
    width: 60%;
    font-size: 16px;
  }
  
  .search-bar button {
    padding: 10px;
    font-size: 16px;
    background-color: #333;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  .content {
    position: relative;
    text-align: center;
    padding: 40px 0;
  }
  
  .background-image {
    background-image: url('image/background1.jpeg'); /* Add a background image of your choice */
    background-size: cover;
    background-position: center;
    color: white;
    padding: 100px 20px;
  }
  
  .background-image h1 {
    font-size: 3rem;
  }
  
  .background-image p {
    font-size: 1.5rem;
    margin: 20px 0;
  }
  
  .book-now-btn {
    background-color: #ff5733;
    padding: 15px 30px;
    font-size: 1rem;
    text-decoration: none;
    color: white;
    border-radius: 5px;
  }
  
  .social-media a {
    color: #333;
    text-decoration: none;
    margin: 0 15px;
    font-size: 18px;
  }
  
  #searchResults {
    margin-top: 30px;
  }
  // script.js

document.getElementById("searchButton").addEventListener("click", function() {
    const searchInput = document.getElementById("searchInput").value.toLowerCase();
    const resultsContainer = document.getElementById("searchResults");
  
    if (searchInput.trim() === "") {
      resultsContainer.innerHTML = "<p>Please enter a destination or keyword.</p>";
      return;
    }
  
    // Mock search data (You can replace this with actual search logic or API)
    const destinations = [
      "Paris",
      "New York",
      "Tokyo",
      "Sydney",
      "Rome",
      "Berlin"
    ];
  
    const filteredResults = destinations.filter(destination =>
      destination.toLowerCase().includes(searchInput)
    );
  
    if (filteredResults.length > 0) {
      resultsContainer.innerHTML = `<h2>Search Results:</h2><ul>${filteredResults.map(result => `<li>${result}</li>`).join('')}</ul>`;
    } else {
      resultsContainer.innerHTML = "<p>No results found.</p>";
    }
  });
  
