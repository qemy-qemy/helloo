<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Secure Login</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        .loading-spinner {
            display: none;
            margin: 10px auto;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 4px solid transparent;
            border-top: 4px solid blue;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .error {
            color: red;
        }
        .success {
            color: green;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Login</h2>
        <form id="loginForm" onsubmit="return handleLogin(event)">
            <input type="text" id="loginUsername" placeholder="Username" required><br><br>
            <input type="password" id="loginPassword" placeholder="Password" required><br><br>
            <button type="submit">Login</button>
            <div class="loading-spinner" id="loadingSpinner"></div>
        </form>
        <div id="message"></div>
    </div>

  
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="shotcut icon" type="x-icon" href="images.jpeg" >
    <link rel="stylesheet" href="home.css">
    <script type="module" src="home.js" defer></script>
    <title>Chea Mugenzi.I</title>
    <style>
       
    </style>
</head>
<body>
    
    <div class="container">
       
        <nav class="animate-fade-in">
            <div class="logo">Chez Mugenzi.I</div>
            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#features">Product</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
               
            </div>
        </nav>

        <section class="hero animate-fade-in">
            <h1>Manage product for your business</h1>
            <p>manage Customers , Product Etc...</p>
            <div class="gradient-box">
                <img src="image.png" style="height: 8rem; " >
                <h2>Only<span>Mugenzi</span>Enter </h2>
                <button style="margin-top: 2rem; padding: 1rem 2rem; border: none; border-radius: 0.5rem; background: blue; color: white; cursor: pointer; " class="enter">
                   <a href="owner.html" style="text-decoration: none; color: white; font-size: 16px; " class="enter" > Enter</a>
                </button>
            </div>
        </section>

        <section class="features">
          <a href="customer keeper.html" style="text-decoration: none; color: white;">  <div class="feature-card animate-fade-in">
                <h3>Customer's Page</h3>
                <p> user enter when He/She is going to add Customer</p>
            </div>
            <a href="#" style="text-decoration: none; color: white;">  <div class="feature-card animate-fade-in">
                <h3>Work page</h3>
                <p>user enter when He/She is going to make Comand</p>
            </div></a>
            <a href="#" style="text-decoration: none; color: white;"> <div class="feature-card animate-fade-in">
                <h3>Product</h3>
                <p>user enter when He/She is going to add product</p>
            </div></a>
        </section>
    </div>
    <img src="chez-removebg-preview.png" class="chez">
    <div class="menu" onclick="toggleMenu()">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="settings-menu" id="settingsMenu">
            <ul>
               
                    <div class="nav-links" style="font-size: 1rem;     
                    display: inline;
                    ">
                <li> <a href="#home" style="text-decoration: none; color: #fff;">Home</a></li>
                <li>  <a href="#features" style="text-decoration: none; color: #fff;">Product</a></li>
                <li> <a href="#home" style="text-decoration: none; color: #fff;">About</a></li>
            </div>
        </nav>
                <a href="#contact"><button onclick="handleLogout()" style="margin-bottom: -15px;">log out</button></a>
            
            </ul>
        </div>
    </div>

    <script>
        function handleLogout() {
            localStorage.removeItem("loggedIn"); // Clear login status
            window.location.href = "login.html"; // Redirect to login page
        }

        // Redirect if not logged in
        window.onload = function () {
            if (localStorage.getItem("loggedIn") !== "true") {
                window.location.href = "login.html";
            }
        };
        function toggleMenu() {
            const menu = document.getElementById("settingsMenu");
            menu.style.display = menu.style.display === "block" ? "none" : "block";
        }
        
        document.addEventListener("click", function(event) {
            const menu = document.getElementById("settingsMenu");
            const menuIcon = document.querySelector(".menu");
            if (!menu.contains(event.target) && !menuIcon.contains(event.target)) {
                menu.style.display = "none";
            }
        });
    </script>
    
</body>
</html>
