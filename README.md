<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaming Platform</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <style>
        body {
    font-family: Arial, sans-serif;
    background-color: #111;
    color: #eee;
    padding: 20px;
}

.search-container {
    margin-bottom: 20px;
}

input[type="text"] {
    padding: 10px;
    width: 70%;
    font-size: 16px;
    border: none;
    border-radius: 4px;
    margin-right: 10px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    background-color: #444;
    color: #eee;
    transition: background-color 0.2s;
}

button:hover {
    background-color: #555;
}

.game-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 10px;
    padding: 10px;
    background-color: #222;
    border-radius: 5px;
}

.game-image {
    width: 60px;
    height: 60px;
    margin-right: 10px;
}

.game-details {
    flex: 1;
}

.game-download-link {
    color: #00f;
    text-decoration: none;
}

    </style>
    <center><div class="search-container">
        <input type="text" id="searchBar" placeholder="Search for Apps...">
        <button onclick="searchGames()">CLICK</button>
    </div>

    <div id="gamesList" class="games-list">
        <!-- Games will be populated here -->
    </div>

    <script src="script.js"></script>
    <script>
        const games = [
    { name: "FREE FIRE INDIA 🇮🇳", imageUrl: "minimalist-logo-free-fire-banner-wisbgb2gy1oej2io.jpg", downloadLink: "https://modcombo.io/free-fire-india.html" },
    { name: "(BATTLE GROUND MOBILE INDIA 🇮🇳)BGMI", imageUrl: "BGMI_Official_Logo.jpg", downloadLink: "https://battlegrounds-mobile-india.en.uptodown.com/android/download" },
      { name: "PUBG MOBILE LITE", imageUrl: "pubg_mobile_lite_google_play_1533881298207.jpg", downloadLink: "https://pubg-mobile-lite.en.uptodown.com/android/download" },
        { name: "INSTAGRAM", imageUrl: "instagram-1581266_640.jpg", downloadLink: "https://instagram.en.uptodown.com/android/download" },
          { name: "SNAPCHAT", imageUrl: "8321386493d27b75389b6265d9fffdca.jpg", downloadLink: "https://snapchat.en.uptodown.com/android" },
            { name: "FLIPKART", imageUrl: "png-transparent-flipkart-logo-computer-icons-encapsulated-postscript-others-service-logo-business-thumbnail.png", downloadLink: "https://flipkart.en.softonic.com/android/download?ex=RAMP-1391.3" },
               { name: "AMAZON", imageUrl: "png-clipart-logo-amazon-com-brand-flipkart-others-text-orange-thumbnail.png", downloadLink: "https://amazon-shopping.en.uptodown.com/android/download" },
                  { name: "WHATSHAPP", imageUrl: "1384023.png", downloadLink: "https://www.whatsapp.com/android" },
                    { name: "DOMINO'S PIZZA", imageUrl: "09ba9064-bd51-49ae-bec0-e6ab2144024a.jpg", downloadLink: "https://dominos-pizza-group-ltd-domino.en.uptodown.com/android" },
                       { name: "TRUECALLER", imageUrl: "truecaller app ads-ms-nvcpwzqkca.jpg", downloadLink: "https://www.truecaller.com/" },
                          { name: "TWITTER", imageUrl: "twitter-icon-circle-black-logo-35827D553B-seeklogo.com.png", downloadLink: "https://twitter.en.uptodown.com/android/download" },
                            { name: "JM TOOLS", imageUrl: "jm tools apk.png", downloadLink: "https://www.google.com/amp/s/m.apkpure.com/jm-tools-pro-gfx-for-any-games/app.rizqi.jmtools/amp" },
                               { name: "JAVA SCRIPT PROGRAMMING LANGUAGE", imageUrl: "kisspng-javascript-programmer-logo-programming-language-program-logo-5b407df7636075.6807421015309532074071.jpg", downloadLink: "https://java-programming.en.uptodown.com/android" },
                                   { name: "PHP PROGRAMMING LANGUAGE", imageUrl: "1975.png", downloadLink: "https://apkpure.com/learn-php-programming/php.coding.programming.learn.web.website.development/amp" },
                                      { name: "PYTHON PROGRAMING LANGUAGE", imageUrl: "a26c4b485716a585073da2af4328a8cd.jpg", downloadLink: "https://python-3.en.uptodown.com/android" },
                                        { name: "C++ PROGRAMMING LANGUAGE", imageUrl: "Top-Uses-Of-C.jpg", downloadLink: "https://developerinsider.co/download-turbo-c-for-windows-7-8-8-1-and-windows-10-32-64-bit-full-screen/amp/" },
                                          { name: "C PROGRAMMING LANGUAGE", imageUrl: "715b59c8c7545d9dafb1a04111edde40.jpg", downloadLink: "https://c-free.en.softonic.com/?ex=RAMP-1391.3" },
                                            { name: "BACKGROUND REMOVER", imageUrl: "erasebg_34674_logo_1648806396_pdvef.jpg", downloadLink: "https://apkloo.com/remove-bg-mod/" },
                                              { name: "INDIAN VPN", imageUrl: "07zgBPVEQjBd62zqeZfZ7p1-1..v1652886589.jpg", downloadLink: "https://india-vpn.en.uptodown.com/android" },
                                                { name: "ZOMATO", imageUrl: "zomato-logo-zomato-icon-free-free-vector (1).jpg", downloadLink: "https://zomato.en.uptodown.com/android/download" },
                                                   { name: "DIGI LOCKER", imageUrl: "92777e3bb33a18a9a34188664d32349a.png", downloadLink: "https://www.digilocker.gov.in/" },
                                                     { name: "SPOTIFY MUSIC", imageUrl: "icon3@2x.png", downloadLink: "https://www.spotify.com/us/download/android/" },
                                                       { name: "RTO GUJARAT", imageUrl: "360_F_520186124_7t0xUSwsRQXU9u0l7ccVrTl46FRcJMdA.jpg", downloadLink: "https://rto-vehicle-information-vahan.en.softonic.com/android?ex=RAMP-1391.3" },  
    { name: "GIT HUB", imageUrl: "GitHub-logo.png", downloadLink: "https://github-android.en.uptodown.com/android" },     
          { name: "IMAGE TO PDF MAKER", imageUrl: "638_pdf_icon.jpg", downloadLink: "https://www.ilovepdf.com/jpg_to_pdf" },
              { name: "ZARCHIVER", imageUrl: "1a0611cc-b86e-4550-8d6b-7ec4f7ad8646.jpg", downloadLink: "https://zarchiver.en.uptodown.com/android" },                    
                   { name: "MAPPLE MAP INDIA 🇮🇳", imageUrl: "mappls-og.png", downloadLink: "https://www.google.com/amp/s/apkpure.com/mappls-mapmyindia-maps-safety/com.mmi.maps/amp" },
                     { name: "FAM PAY", imageUrl: "fampayLogo-1634713756429.png", downloadLink: "https://filehippo.com/android/download_fampay-upi-card-for-teens/" },
                         { name: "PHONE PAY", imageUrl: "2acfb6fb41f7fcb82c3230afdecff714.jpg", downloadLink: "https://www.phonepe.com/app-download/" },
                           { name: "GOOGLE PAY", imageUrl: "black-google-pay-logotype-white-background-logo-mobile-payment-system-electronic-wallet-contactless-nfc-android-operating-system-gpay-editorial_661108-8063.jpg", downloadLink: "https://google-pay-tez.en.uptodown.com/android/download" },
                                 { name: "PAYTM", imageUrl: "pt_main.jpg", downloadLink: "https://paytm.com/download-paytm-app" },
                                    { name: "SWIGGY", imageUrl: "swiggy-black2725.jpg", downloadLink: "https://swiggy.en.uptodown.com/android" },
                                          { name: "SOLO VPN", imageUrl: "ea29a8a3488969315a93d6911d6e9bf0.jpg", downloadLink: "https://solo-vpn.en.uptodown.com/android/download" },     
                                             { name: "KINE MASTER", imageUrl: "Kine_Master-512.png", downloadLink: "https://apkmodget.com/apps/kinemaster-mod-apk-without-watermark-free-1-latest/" },                  
                                 
    // Add more games as needed
];


function searchGames() {
    const searchTerm = document.getElementById('searchBar').value.toLowerCase();
    const gamesList = document.getElementById('gamesList');

    gamesList.innerHTML = ''; // Clear the list

    for (const game of games) {
        if (game.name.toLowerCase().includes(searchTerm)) {
            gamesList.innerHTML += `
                <div class="game-item">
                    <img src="${game.imageUrl}" alt="${game.name}" class="game-image">
                    <div class="game-details">
                        ${game.name}
                    </div>
                    <a href="${game.downloadLink}" class="game-download-link">Download</a>
                </div>
            `;
        }
    }
}

    </script>
</body>
</html>
