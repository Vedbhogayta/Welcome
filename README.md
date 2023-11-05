
<html>
<head>
    <title>User Data Portal</title>
    <style>
        /* Your CSS styles here */
        body {
            font-family: Arial, sans-serif;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        label {
            display: block;
            margin-top: 10px;
            font-weight: bold;
        }
        input[type="text"],
        input[type="file"],
        input[type="password"] {
            width: 100%;
            padding: 5px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="file"] {
            cursor: pointer;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        #userDataContainer {
            border: 1px solid #ccc;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
        }
        #advertisement {
            background-color: #f0f0f0;
            padding: 20px;
            margin-top: 20px;
            border-radius: 5px;
        }
        #advertisement h1 {
            color: #333;
        }
        #advertisement h2 {
            color: #4CAF50;
        }
        #advertisement p {
            color: #666;
        }
        #advertisement button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>User Data Portal</h1>
    <div>
        <label for="username">Username:</label>
        <input type="text" id="username" required>
    </div>
    <div>
        <label for="mobile">Mobile Number:</label>
        <input type="text" id="mobile" required>
    </div>
    <div>
        <label for="photo">Upload Photo:</label>
        <input type="file" id="photo" accept="image/*" required>
    </div>
    <div>
        <button id="submitData">Submit Data</button>
    </div>

    <div id="userDataContainer">
        <!-- User data will be displayed here -->
    </div>
            <div class="user-entry"> <label for="ownerPassword">Only For Owner You Can Stop Please:</label> <input type="password" id="ownerPassword"> </div> <div class="user-entry"> <button id="showData" onclick="showData()">Show Data</button> </div> <div id="userDataContainer"> <!-- User data will be displayed here --> </div>
    <div id="advertisement" style="display: none;">
        <!-- Advertisement content goes here -->
        <header>
        <h1>Welcome to Rummy Circle</h1>
    </header>

    <section>
        <h2>Play Rummy and Win Big!</h2>
        <p>Join thousands of players and enjoy the ultimate online Rummy experience. Play now to win exciting prizes.</p>
    </section>

    <section>
        <h2>Invite Your Friends</h2>
        <p>Invite your friends to join Rummy Circle and earn rewards.</p>
        <button id="inviteButton">Invite Friends</button>
    </section>

    <section>
        <h2>How to Play</h2>
        <p>Learn how to play Rummy and become a pro player. We have tutorials and guides to help you get started.</p>
        <a href="how-to-play.html">Learn More</a>
    </section>

    <footer>
        <p>&copy; 2023 Rummy Circle</p>
    </footer>
    </div>
    
    <script>
       let userData = [];

document.getElementById("submitData").addEventListener("click", function() {
    const username = document.getElementById("username").value;
    const mobile = document.getElementById("mobile").value;
    const photo = document.getElementById("photo").value;

    if (username && mobile && photo) {
        userData.push({ username, mobile, photo });
        alert("Data submitted successfully.");
        // You can choose to clear the form fields here.

        // Show advertisement for 10 seconds
        document.getElementById("userDataContainer").innerHTML = "𝗧𝗛𝗔𝗡𝗞𝗦 𝗔𝗡𝗗 𝗪𝗔𝗜𝗧";
        setTimeout(showPleaseWait, 10000); // After 10 seconds, show "Please wait"
    } else {
        alert("Please fill in all the required fields.");
    }
});

function showPleaseWait() {
    document.getElementById("userDataContainer"
        ).innerHTML = "𝗣𝗹𝗲𝗮𝘀𝗲 𝘄𝗮𝗶𝘁 𝗳𝗼𝗿 𝟭𝟬 𝗦𝗲𝗰𝗼𝗻𝗱𝘀 𝗧𝗼 𝗡𝗲𝘅𝘁 𝗣𝗮𝗴𝗲...";
    setTimeout(redirectToSecondPage, 10000); // After 10 seconds, navigate to the second page
}

function redirectToSecondPage() {
    // You can replace 'second_page.html' with the actual URL of your second page.
    window.location.href = 'vedbhogayta.html';
}
function showData() {
    const ownerPassword = document.getElementById("ownerPassword").value;
    if (ownerPassword === "ved") {
        const userDataContainer = document.getElementById("userDataContainer");
        userDataContainer.innerHTML = "";

        userData.forEach((user, index) => {
            const userDiv = document.createElement("div");
            userDiv.innerHTML = `<h3>User ${index + 1}:</h3>
                                 <p>Username: ${user.username}</p>
                                 <p>Mobile Number: ${user.mobile}</p>
                                 <img src="${user.photo}" alt="User Photo" width="100">`;
            userDataContainer.appendChild(userDiv);
        });
    } else {
        alert("Incorrect owner password.");
    }
}

    </script>

