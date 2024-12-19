

<!doctype html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Darshana Education |<?php echo $pageName; ?></title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">    
    <link rel="icon" type="image/png" href="Black%20and%20Blue%20Initials%20Creative%20Logo%20(1).png" sizes="32x32">
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="bootstrap-5.3.3-dist/css">
    <link rel="stylesheet" href="bootstrap-5.3.3-dist/js">
    <link href="https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,100..900;1,100..900&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link rel="stylesheet" href="https://learnwithammaar.com/includes/css/style.css">
    <link rel="stylesheet" href="https://learnwithammaar.com/includes/css/buttons.css">
    <style>

        /* Light and dark theme colors */
        :root {
            --bg-color-dark: #343a40;
            --text-color-dark: #ffffff;
            --bg-color-light: #ffffff;
            --text-color-light: #000000;
        }

        body.dark-mode {
            background-color: var(--bg-color-dark);
            color: var(--text-color-dark);
        }

        body.light-mode {
            background-color: var(--bg-color-light);
            color: var(--text-color-light);
            
        }

        .profile-container {
          text-align: left;
          margin: 50px auto;
        }
        .profile-photo {
          width: 150px;
          height: 150px;
          border-radius: 50%;
          object-fit: cover;
          cursor: pointer; /* Makes the image clickable */
        }
        input[type="file"] {
          display: none; /* Hides the file input */
        }
  
    </style>
</head>
<?php
function checkActive($correctName, $currentName)
{

    if ($correctName == $currentName) {
        echo 'active';
    }
}
?>

<body class="dark-mode">
    <nav class="navbar navbar-expand-lg bg-dark sticky-top bg-body-tertiary" data-bs-theme="dark">
        <div class="container-fluid">
            <div class="nav-left d-flex align-items-center">
                <a class="navbar-brand d-flex align-items-center" href="home.php">
                    <img src="Black%20and%20Blue%20Initials%20Creative%20Logo%20(1).png" alt="logo" width="50" height="50" class="d-inline-block align-text-top">
                    <span class="ms-2">Darshana Education</span>
                </a>
            </div>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav w-100 d-flex justify-content-between align-items-center">
                    <?php if (isset($_SESSION['user'])) { ?>
                        <div class="d-flex justify-content-center w-100">
                            <li class="nav-item">
                                <a class="nav-link <?php checkActive("Home Page", $pageName); ?>"
                                 href="home.php">Home</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link <?php checkActive("Class Page", $pageName); ?>"
                                    href="class.php">Class</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link <?php checkActive("Contect Page", $pageName); ?>"
                                    href="contectus.php">Contect Us</a>
                            </li>
                        </div>

                        <div class="d-flex justify-content-center mx-8">                            
                            <form class="d-flex" action="search.php" method="GET" role="search">
                                <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                                <button class="btn btn-outline-success" type="submit">Search</button>
                            </form>                           
                        </div>

                        <div class="d-flex align-items-center">
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    Theme 
                                </a>
                                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <li><a class="dropdown-item" href="#" onclick="setDarkMode()">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-moon-stars-fill" viewBox="0 0 16 16">
                                            <path d="M6 .278a.77.77 0 0 1 .08.858 7.2 7.2 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277q.792-.001 1.533-.16a.79.79 0 0 1 .81.316.73.73 0 0 1-.031.893A8.35 8.35 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.75.75 0 0 1 6 .278"/>
                                            <path d="M10.794 3.148a.217.217 0 0 1 .412 0l.387 1.162c.173.518.579.924 1.097 1.097l1.162.387a.217.217 0 0 1 0 .412l-1.162.387a1.73 1.73 0 0 0-1.097 1.097l-.387 1.162a.217.217 0 0 1-.412 0l-.387-1.162A1.73 1.73 0 0 0 9.31 6.593l-1.162-.387a.217.217 0 0 1 0-.412l1.162-.387a1.73 1.73 0 0 0 1.097-1.097zM13.863.099a.145.145 0 0 1 .274 0l.258.774c.115.346.386.617.732.732l.774.258a.145.145 0 0 1 0 .274l-.774.258a1.16 1.16 0 0 0-.732.732l-.258.774a.145.145 0 0 1-.274 0l-.258-.774a1.16 1.16 0 0 0-.732-.732l-.774-.258a.145.145 0 0 1 0-.274l.774-.258c.346-.115.617-.386.732-.732z"/>
                                        </svg>
                                         Dark</a></li>
                                    <li><a class="dropdown-item" href="#" onclick="setLightMode()">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-brightness-high-fill" viewBox="0 0 16 16">
                                            <path d="M12 8a4 4 0 1 1-8 0 4 4 0 0 1 8 0M8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0m0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13m8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5M3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8m10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0m-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0m9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707M4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708"/>
                                        </svg>
                                         Light </a></li>
                                    <li><a class="dropdown-item" href="#" onclick="setAutoMode('auto')">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-circle-half" viewBox="0 0 16 16">
                                            <path d="M8 15A7 7 0 1 0 8 1zm0 1A8 8 0 1 1 8 0a8 8 0 0 1 0 16"/>
                                        </svg>
                                         Auto</a></li>
                                </ul>
                            </li>

                            <div class="profile-dropdown">
                                <img src="Untitled%20design.png" alt="Profile" class="profile-icon">
                                <div class="dropdown-content">
                                    <a href="profile.php">My Profile</a>
                                    <a href="logout.php">Logout</a>
                                </div>
                            </div>
                        </div>

                    <?php } else { ?>
                        <div class="d-flex justify-content-center mx-8"> 
                            <li class="nav-item">
                                <a class="nav-link <?php checkActive("Login Page", $pageName); ?>" href="index.php">Sign in</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link <?php checkActive("Register Page", $pageName); ?>"
                                    href="register.php">Register</a>
                            </li>
                        </div>    
                    <?php } ?>
                </ul>
            </div>


        </div>
    </nav>
    