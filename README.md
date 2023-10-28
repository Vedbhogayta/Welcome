
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Battlegrounds Mobile India Mockup</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #202020;
            color: white;
            margin: 0;
            padding: 0;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #333;
            padding: 10px 10px;
        }
        
        .navbar img.logo {
            width: 30px;
            height: auto;
        }
        
        .navbar ul {
            list-style: none;
            padding: 0;
            display: flex;
            gap: 20px;
        }
        
        .navbar ul li {
            display: inline;
        }
        
        .navbar ul li a {
            text-decoration: none;
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .navbar ul li a:hover {
            background-color: #555;
        }

        .banner {
            text-align: center;
            padding: 50px 0;
        }

        .banner h1 {
            font-size: 3rem;
        }

        .banner p {
            margin-top: 20px;
            font-size: 1.2rem;
        }

        .banner img.game-image {
            max-width: 100%;
            height: auto;
            margin-top: 50px;
        }
        
      footer {
    background-color: silver;
    color: white;
    text-align: center;
    padding: 10px 0;
}
        
        
    </style>
</head>


<div class="navbar">
    <img src="IMG_20231028_124648-removebg-preview.png" alt="Game Logo" class="logo">
    <ul>
        <li><a href="lodu.html">Example</a></li>
        <li><a href="#">Download</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</div>

<div class="banner">
    <h1>Welcome  </h1>
    <p>Discover an extensive collection of app descriptions curated by Team Ved Bhogayta. Whether you've downloaded an app, are thinking about making a purchase, or are just browsing, our comprehensive guide offers insights into all apps available. Dive deep into the details and make informed decisions with the trusted guidance of Team Ved Bhogayta.<ul></ul>

If you have more specific details or requirements for the description, please let me know, and I'll be happy to help further!</p>
    <img src="Picsart_23-10-28_13-00-47-818.jpg" alt="Game Image" class="game-image">
</div>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Rating</title>
    <style>
        .rating {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        .star {
            font-size: 24px;
            cursor: pointer;
            color: grey;
        }

        .star:hover, .star.active {
            color: gold;
        }

        #rating-count {
            font-size: 20px;
        }
    </style>
</head>
<body>

<div class="rating">
    <span class="star" data-value="1">★</span>
    <span class="star" data-value="2">★</span>
    <span class="star" data-value="3">★</span>
    <span class="star" data-value="4">★</span>
    <span class="star" data-value="5">★</span>
</div>

<center><p id="rating-count">Current Rating: Not Rated</p>

<script>
    let stars = document.querySelectorAll('.star');
    stars.forEach(star => {
        star.addEventListener('click', function() {
            let value = this.getAttribute('data-value');
            document.getElementById('rating-count').innerText = "Current Rating: " + value + "/5";

            // Highlight the selected stars
            stars.forEach(s => s.classList.remove('active'));
            for (let i = 0; i < value; i++) {
                stars[i].classList.add('active');
            }
        });
    });
</script>



<footer>
        <p>&copy; 2023-24 Ved Bhogayta</p>
    </footer>
</body>
</html>
