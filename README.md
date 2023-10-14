# Assignment01
<!DOCTYPE html>
<html>
  <head>
    <title>{{title}}</title>
    <link rel='stylesheet' href='/stylesheets/style.css' />
  </head>
 


<body>
    <div class="container">

        <!-- Navigation Bar -->
<nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
        <a class="navbar-brand" href="#"><img class="logo" src="images/coding.png" alt="logo"></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#home">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#about">About Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#service">Service</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contact">Contact Us</a>
                </li>
                {{#if isLoggedIn}}
                <!-- User is logged in -->
                <li class="nav-item dropdown">
                    <a class="mb-1 nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                        data-bs-toggle="dropdown" aria-expanded="false">
                        <img src="images/coding.png" class="user_icon" alt="profile-icon">
                        {{ username }}
                    </a>
                    <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <li><a class="dropdown-item" href="#">Logout</a></li>
                    </ul>
                </li>
                {{else}}
                <!-- User is not logged in -->
                <button type="button" class="btn btn-outline-primary ms-2" data-bs-toggle="modal"
                    data-bs-target="#exampleModal">Sign up</button>
                {{/if}}
            </ul>
        </div>
    </div>
</nav>
