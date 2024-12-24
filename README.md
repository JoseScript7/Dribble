# Project Responsive Web Design using Bootstrap
## Date:23.12.2024

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@500&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        function zoomIn(event) {
            event.target.style.transform = "scale(1.1)";
            event.target.style.transition = "transform 0.2s ease-in-out";
        }

        function zoomOut(event) {
            event.target.style.transform = "scale(1)";
        }

        function likeHover(event) {
            event.target.style.color = "#FF6F61";  // Change color when mouse hovers over like icon
        }

        function likeOut(event) {
            event.target.style.color = "black";  // Revert to the original color when mouse leaves the like icon
        }

        function toggleLike(event) {
            const heartIcon = event.target;
            if (heartIcon.classList.contains("liked")) {
                heartIcon.classList.remove("liked");
                heartIcon.style.color = "black";  // Revert to original color when unliked
            } else {
                heartIcon.classList.add("liked");
                heartIcon.style.color = "#FF6F61";  // Change color to red when liked
            }
        }
    </script>
</head>
<body>
    <nav class="navbar navbar-expand-lg shadow-sm">
        <div class="container">
            <a class="navbar-brand" href="#">Dribbble</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#">Explore</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Hire a Designer</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Find Jobs</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Sign In</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Sign Up</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container mt-4">
        <div class="d-flex justify-content-between align-items-center">
            <div class="w-50">
                <input type="text" class="form-control" placeholder="What are you looking for?">
            </div>
            <div class="btn-group">
                <button class="btn btn-outline-secondary">Popular</button>
                <button class="btn btn-outline-secondary">Discover</button>
                <button class="btn btn-outline-secondary">Animation</button>
                <button class="btn btn-outline-secondary">Branding</button>
                <button class="btn btn-outline-secondary">Illustration</button>
                <button class="btn btn-outline-secondary">Web Design</button>
            </div>
        </div>
    </div>

    <div class="container mt-4">
        <div class="row g-4">
            <div class="col-md-3">
                <div class="card">
                    <img src="image1.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">Gert van Dulmen</h5>
                        <p class="card-text">Design</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 100 likes</span>
                        <span>👁 6.5k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image2.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">FANCY</h5>
                        <p class="card-text">Illustration</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 250 likes</span>
                        <span>👁 2.4k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image3.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">Bato</h5>
                        <p class="card-text">Web Design</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 300 likes</span>
                        <span>👁 3.1k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image4.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">Sigma</h5>
                        <p class="card-text">Animation Logos</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 150 likes</span>
                        <span>👁 1.8k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image5.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">Graphtheory</h5>
                        <p class="card-text">Branding</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 220 likes</span>
                        <span>👁 4.1k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image6.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">CoricDesign</h5>
                        <p class="card-text">Illustration</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 130 likes</span>
                        <span>👁 2.5k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image7.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">Mahjabin</h5>
                        <p class="card-text">Web Design</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 180 likes</span>
                        <span>👁 1.7k views</span>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image8.webp" class="card-img-top" alt="Card Image" onmousemove="zoomIn(event)" onmouseout="zoomOut(event)">
                    <div class="card-body">
                        <h5 class="card-title">GeekArts</h5>
                        <p class="card-text">Animation</p>
                    </div>
                    <div class="card-footer d-flex justify-content-between">
                        <span onclick="toggleLike(event)" onmouseover="likeHover(event)" onmouseout="likeOut(event)" style="cursor:pointer;">❤ 220 likes</span>
                        <span>👁 5k views</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer style="text-align:center; padding:20px; background-color:#f8f9fa; margin-top:20px;">
        <p>Designed and Developed by A. Ranen Joseph (24006171)</p>
    </footer>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2024-12-24 095934.png>) 
![alt text](<Screenshot 2024-12-24 095920.png>)


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
