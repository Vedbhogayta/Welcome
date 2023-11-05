
<html>
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <style>
        /* styles.css */
body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: silver;
}

.warning-container {
    text-align: center;
}

.warning-logo {
    background-image: url('warning-icon.png');
    background-size: contain;
    width: 100px;
    height: 150px;
    margin: 0 auto 20px;
}

.warning-message {
    color: red;
    font-size: 45px;
    font-weight: bold;
    text-shadow: 0 0 10px rgba(255, 0, 0, 0.8);
}

.timer {
    font-size: 63px;
    margin: 20px 0;
}

button {
    padding: 10px 20px;
    height: 40px;
    background-color: blue;
    color: #fff;
    border: none;
    cursor: pointer;
    font-size: 18px;
    display: none;
}

button:hover {
    background-color: blue;
}

    </style>
    <div class="warning-container">
        <div class="warning-logo"></div>
        <h1 class="warning-message">Please Enable Desktop Mode in Your Browser Then Click To Continue</h1>
        <div id="timer" class="timer">5</div>
        <button id="continue-button" class="hidden">Continue</button>
    </div>

    <script>
        // script.js
document.addEventListener("DOMContentLoaded", function () {
    let countdown = 10;

    const timerElement = document.getElementById("timer");
    const continueButton = document.getElementById("continue-button");

    const timerInterval = setInterval(function () {
        countdown--;
        timerElement.textContent = countdown;
        if (countdown === 0) {
            clearInterval(timerInterval);
            continueButton.style.display = "block";
        }
    }, 1000);

    continueButton.addEventListener("click", function () {
        window.location.href = "secondPage.html";
    });
});

    </script>
