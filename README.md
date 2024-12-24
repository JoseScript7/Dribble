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
    <style>
        body {
            background-color: #f8f8f8;
            font-family: 'Rubik', sans-serif;
            margin-bottom: 60px;
        }
        .navbar {
            background-color: white;
            border-bottom: 1px solid #e6e6e6;
        }
        .navbar-brand {
            font-size: 1.8rem;
            font-weight: bold;
            font-family: 'Rubik', sans-serif;
        }
        .search-bar {
            width: 100%;
            border: 1px solid #e6e6e6;
            border-radius: 5px;
            padding: 10px;
        }
        .filters button {
            font-size: 0.9rem;
            margin-right: 10px;
        }
        .card img {
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.2s ease, filter 0.2s ease;
        }
        .card img:hover {
            transform: scale(1.1);
            filter: brightness(1.2);
        }
        .card-body {
            padding: 0.8rem;
        }
        .card-title {
            font-size: 1rem;
            font-weight: bold;
            margin-bottom: 0.3rem;
        }
        .card-subtitle {
            font-size: 0.8rem;
            color: gray;
        }
        .cards-grid {
            margin-top: 20px;
        }
        .card-footer {
            display: flex;
            justify-content: space-between;
            font-size: 0.8rem;
            color: gray;
            margin-top: 10px;
        }
        .card-footer .likes, .card-footer .views {
            transition: all 0.3s ease;
        }
        .card-footer .likes:hover, .card-footer .views:hover {
            color: #ff6b6b;
            cursor: pointer;
        }
        footer {
            background-color: #000;
            padding: 10px 0;
            text-align: center;
            position: fixed;
            width: 100%;
            bottom: 0;
            box-shadow: 0 -1px 5px rgba(0, 0, 0, 0.1);
            color: white;
        }
        footer p {
            margin: 0;
            font-size: 0.9rem;
        }
    </style>
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
                <input type="text" class="search-bar" placeholder="What are you looking for?">
            </div>
            <div class="filters d-flex">
                <button class="btn btn-outline-secondary">Popular</button>
                <button class="btn btn-outline-secondary">Discover</button>
                <button class="btn btn-outline-secondary">Animation</button>
                <button class="btn btn-outline-secondary">Branding</button>
                <button class="btn btn-outline-secondary">Illustration</button>
                <button class="btn btn-outline-secondary">Web Design</button>
            </div>
        </div>
    </div>

    <div class="container cards-grid">
        <div class="row g-4">
            <div class="col-md-3">
                <div class="card">
                    <img src="image1.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">Gert van Dulmen</h5>
                        <p class="card-subtitle">Design</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 100 likes</div>
                        <div class="views">👁 6.5k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image2.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">FANCY</h5>
                        <p class="card-subtitle">Illustration</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 250 likes</div>
                        <div class="views">👁 2.4k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image3.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">Bato</h5>
                        <p class="card-subtitle">Web Design</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 300 likes</div>
                        <div class="views">👁 3.1k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image4.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">Sigma</h5>
                        <p class="card-subtitle">Animation Logos</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 150 likes</div>
                        <div class="views">👁 1.8k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image5.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">Graphtheory</h5>
                        <p class="card-subtitle">Branding</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 220 likes</div>
                        <div class="views">👁 4.1k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image6.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">CoricDesign</h5>
                        <p class="card-subtitle">Illustration</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 130 likes</div>
                        <div class="views">👁 2.5k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image7.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">Mahjabin</h5>
                        <p class="card-subtitle">Web Design</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 180 likes</div>
                        <div class="views">👁 1.7k views</div>
                    </div>
                </div>
            </div>
            <div class="col-md-3">
                <div class="card">
                    <img src="image8.webp" class="card-img-top" alt="Card Image">
                    <div class="card-body">
                        <h5 class="card-title">GeekArts</h5>
                        <p class="card-subtitle">Animation</p>
                    </div>
                    <div class="card-footer">
                        <div class="likes">❤ 220 likes</div>
                        <div class="views">👁 5k views</div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>Designed and Developed by A. Ranen Joseph Solomon (24006171)</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2024-12-24 095934.png>) 
![alt text](<Screenshot 2024-12-24 095920.png>)


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
